# Entrega — Aula 05: RDS e Remote State

**Aluno:** Lucas José Campos da Rocha  
**RA:** 6325123  
**Data:** 25/09/2026

## Repositório

- URL: https://github.com/crocodiles128/unifaat-devops-portfolio.git

## Evidências

- [ ] VPC com subnets públicas e privadas em 2 AZs
- [ ] RDS PostgreSQL (db.t3.micro) nas subnets privadas
- [ ] EC2 t2.micro na subnet pública, conectando ao RDS
- [ ] Security Groups corretos (porta 5432 apenas da VPC)
- [ ] Remote State configurado (S3 + DynamoDB)
- [ ] State armazenado no S3 (evidência abaixo)
- [ ] Conexão EC2 → RDS via psql (evidência abaixo)
- [ ] `terraform destroy` executado após evidências

## Evidência do State no S3

> ⚠️ Zenith no pudo propagar un `terraform plan` sin errores (normalmente requiere credenciales AWS Academy).
> El código quedó generado y validado en el portfólio (`aula-XX/`); completa la evidencia del plan tras configurar las credenciales del Learner Lab.

## Evidência da Conexão EC2 → RDS

[Cole aqui o output do psql ou screenshot]