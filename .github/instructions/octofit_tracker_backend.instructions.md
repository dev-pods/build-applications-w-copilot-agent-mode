---
applyTo: "octofit-tracker/backend/**"
---

# Instruções do backend OctoFit

- Use Express, TypeScript, Mongoose e funções de serviço explícitas.
- Mantenha as rotas em `/api/` e retorne respostas 4xx deliberadas para entradas inválidas.
- Mantenha a validação de modelos nos schemas Mongoose e as regras de negócio nos serviços.
- Use a configuração compartilhada de banco de dados em vez de lógica de conexão codificada diretamente.
- Insira registros de demonstração estáveis com upserts; nunca limpe coleções que possam conter dados de usuários e reconcilie a associação anterior de um usuário de demonstração ao movê-lo de equipe.
