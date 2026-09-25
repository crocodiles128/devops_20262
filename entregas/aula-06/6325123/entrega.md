# Entrega — Aula 06: Terraform Modules

**Aluno:** Lucas José Campos da Rocha  
**RA:** 6325123  
**Data:** 25/09/2026

## Repositório

- URL: https://github.com/crocodiles128/unifaat-devops-portfolio.git

## Evidências

- [x] Módulo VPC com for_each para subnets dinâmicas
- [x] Módulo Security Group genérico (regras como lista de objetos)
- [x] Módulo EC2 reutilizável
- [x] Módulo RDS reutilizável
- [x] Composição entre módulos (output de um alimenta input de outro)
- [x] Dois ambientes (dev + staging) usando os mesmos módulos
- [ ] `terraform validate` e `terraform plan` sem erros nos dois ambientes
- [x] README documentando cada módulo (inputs, outputs, exemplo)

## Evidência do terraform plan

```text
# terraform validate: OK — terraform plan: pendiente de credenciales AWS
Changes to Outputs:
  + db_name = "technova_dev"

You can apply this plan to save these new output values to the Terraform
state, without changing any real infrastructure.
╷
│ Error: Retrieving AWS account details: validating provider credentials: retrieving caller identity from STS: operation error STS: GetCallerIdentity, https response error StatusCode: 403, RequestID: 9197ea61-352f-424b-8105-c7afbc6e424e, api error ExpiredToken: The security token included in the request is expired
│ 
│   with provider["registry.terraform.io/hashicorp/aws"],
│   on providers.tf line 12, in provider "aws":
│   12: provider "aws" {
│ 
╵
```

> ⚠️ El plan se detuvo con `ExpiredToken`: las credenciales del Learner Lab expiran. No es un error del código; al renovar las credenciales basta ejecutar de nuevo `terraform plan` en `environments/dev` y `environments/staging`.
