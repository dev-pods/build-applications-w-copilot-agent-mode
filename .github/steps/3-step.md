## Step 3: Implemente e teste a camada de lógica Express

Continue na branch `build-octofit-app` e delimite cada solicitação ao Copilot pelos testes desta camada.

### 📖 Theory: APIs codificam comportamento, não apenas rotas

A camada de lógica é responsável por validação de requisições, regras de negócio, códigos de status e respostas de erro. Os testes de contrato com Supertest tornam essas decisões observáveis sem navegador e impedem que um endpoint passe apenas porque a rota existe. Implemente uma funcionalidade por vez e use os resultados dos testes para refinar as alterações do Copilot.

### ⌨️ Activity: Implemente e teste a camada de lógica Express

1. Inspecione as rotas e os serviços incompletos e os testes de contrato da API.

   O contrato de criação de atividade usa `userId` e `teamId` de registros existentes. Os testes já criam uma equipe e um usuário válidos antes de enviar uma atividade; implemente conforme esses testes, sem editá-los ou inventar resolução por nome.

1. Peça ao Copilot que comece por um comportamento da API que esteja falhando.

   > ![Static Badge](https://img.shields.io/badge/Prompt-text?style=for-the-badge&logo=github-copilot&logoColor=white&labelColor=purple&color=purple)
   >
   > ```text
   > Comece pelo primeiro teste de contrato da API que falha. Explique o comportamento esperado, implemente apenas esse comportamento e indique qual teste executar em seguida.
   > ```

1. Repita o ciclo de teste, alteração e revisão para atividades, equipes, placar e sugestões de treino.

   > ![Static Badge](https://img.shields.io/badge/Terminal-text?logo=gnometerminal&labelColor=0969da&color=ddf4ff)
   >
   > ```bash
   > npm run test:api --prefix octofit-tracker/backend
   > ```

1. Em um terminal dedicado, inicie o backend na porta 8000 e mantenha-o em execução.

   > ![Static Badge](https://img.shields.io/badge/Terminal-text?logo=gnometerminal&labelColor=0969da&color=ddf4ff)
   >
   > ```bash
   > npm run dev --prefix octofit-tracker/backend
   > ```

1. Em outro terminal, verifique uma requisição bem-sucedida e uma falha de validação.

   > ![Static Badge](https://img.shields.io/badge/Terminal-text?logo=gnometerminal&labelColor=0969da&color=ddf4ff)
   >
   > ```bash
   > curl http://localhost:8000/api/activities
   > curl -i -X POST http://localhost:8000/api/activities -H "Content-Type: application/json" -d "{}"
   > ```

1. Faça commit e push da API testada.

<details>
<summary>Having trouble? 🤷 Precisa de ajuda?</summary><br/>

- Mantenha as rotas em `/api/`.
- Retorne respostas 4xx deliberadas para entradas inválidas, sem simular sucesso.
- Centralize o comportamento para Codespaces e localhost em um auxiliar de configuração.

</details>
