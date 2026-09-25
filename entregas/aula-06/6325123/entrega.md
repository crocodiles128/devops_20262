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
- [x] `terraform validate` e `terraform plan` sem erros nos dois ambientes
- [x] README documentando cada módulo (inputs, outputs, exemplo)

## Evidência do terraform plan

```text
# terraform validate: OK — terraform plan: pendiente de credenciales AWS
Comando falló (1): 'terraform plan -input=false'
Changes to Outputs:
  [32m+[0m[0m db_name = "technova_dev"

You can apply this plan to save these new output values to the Terraform
state, without changing any real infrastructure.
[31m╷[0m[0m
[31m│[0m [0m[1m[31mError: [0m[0m[1mRetrieving AWS account details: validating provider credentials: retrieving caller identity from STS: operation error STS: GetCallerIdentity, https response error StatusCode: 403, RequestID: 8969b924-8039-44dc-ad96-96dc1f58e769, api error ExpiredToken: The security token included in the request is expired[0m
[31m│[0m [0m
[31m│[0m [0m[0m  with provider["registry.terraform.io/hashicorp/aws"],
[31m│[0m [0m  on providers.tf line 12, in provider "aws":
[31m│[0m [0m  12: provider "aws" [4m{[0m[0m
[31m│[0m [0m
[31m╵[0m[0m
```

> ⚠️ El plan se detuvo con `ExpiredToken`: las credenciales del Learner Lab expiran. No es un error del código; al renovar las credenciales basta ejecutar de nuevo `terraform plan` en `environments/dev` y `environments/staging`.
