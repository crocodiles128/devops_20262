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

> ⚠️ Zenith no pudo propagar un `terraform plan` sin errores (normalmente requiere credenciales AWS Academy).
> El código quedó generado y validado en el portfólio (`aula-05/`); completa la evidencia del plan tras configurar las credenciales del Learner Lab.