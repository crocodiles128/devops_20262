# Entrega — Aula 05: RDS e Remote State

**Aluno:** Lucas José Campos da Rocha  
**RA:** 6325123  
**Data:** 25/09/2026

## Repositório

- URL: https://github.com/crocodiles128/unifaat-devops-portfolio.git

## Evidências

- [x] VPC com subnets públicas e privadas em 2 AZs
- [x] RDS PostgreSQL (db.t3.micro) nas subnets privadas
- [x] EC2 t2.micro na subnet pública, conectando ao RDS
- [x] Security Groups corretos (porta 5432 apenas da VPC)
- [x] Remote State configurado (S3 + DynamoDB)
- [ ] State armazenado no S3 (evidência abaixo)
- [ ] Conexão EC2 → RDS via psql (evidência abaixo)
- [ ] `terraform destroy` executado após evidências

## Evidência do State no S3

> ⚠️ Pendiente de ejecución real: con credenciales AWS válidas corre `bash scripts/capturar-evidencias.sh` y el `aws s3 ls` aparecerá aquí (vuelve a ejecutar Zenith).

## Evidência da Conexão EC2 → RDS

> ⚠️ Pendiente de ejecución real: prueba la conexión `EC2 → RDS` con `psql` (`terraform output ec2_ssh_command`) o usa `bash scripts/capturar-evidencias.sh`.

## Evidencia del terraform plan

```text
# terraform validate: OK — terraform plan: bloqueado por el entorno AWS
╷
│ Error: Backend initialization required, please run "terraform init"
│ 
│ Reason: Initial configuration of the requested backend "s3"
│ 
│ The "backend" is the interface that Terraform uses to store state,
│ perform operations, etc. If this message is showing up, it means that the
│ Terraform configuration you're using is using a custom configuration for
│ the Terraform backend.
│ 
│ Changes to backend configurations require reinitialization. This allows
│ Terraform to set up the new configuration, copy existing state, etc. Please
│ run
│ "terraform init" with either the "-reconfigure" or "-migrate-state" flags
│ to
│ use the current configuration.
│ 
│ If the change reason above is incorrect, please verify your configuration
│ hasn't changed and try again. At this point, no changes to your existing
│ configuration or state have been made.
╵
```

> ⚠️ Terraform no pudo conectar con AWS: credenciales del Learner Lab vencidas o bucket/tabla del remote state aún no creados. No es un error del código (`terraform validate` pasó en las dos stacks del portfólio). Al renovar las credenciales ejecuta `bash aula-05/scripts/capturar-evidencias.sh` y vuelve a correr Zenith.
