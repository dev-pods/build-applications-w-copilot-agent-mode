## Step 5: Verifique o sistema e faça merge de um pull request revisado

Continue na branch `build-octofit-app` e delimite cada solicitação ao Copilot pelos testes desta camada.

### 📖 Theory: Evidências de integração antes do merge

Testes isolados aprovados são necessários, mas não suficientes para uma aplicação multicamadas. A verificação final deve demonstrar que os contratos de dados, API e interface concordam; depois, use um pull request para revisar a alteração completa como um sistema. O Copilot pode resumir e revisar o diff, mas você continua responsável por verificar as evidências e resolver problemas antes do merge.

### ⌨️ Activity: Verifique o sistema e faça merge de um pull request revisado

1. Execute a suíte completa de verificação e os dois builds de produção.

   > ![Static Badge](https://img.shields.io/badge/Terminal-text?logo=gnometerminal&labelColor=0969da&color=ddf4ff)
   >
   > ```bash
   > npm run test:data --prefix octofit-tracker/backend
   > npm run test:api --prefix octofit-tracker/backend
   > npm test --prefix octofit-tracker/frontend
   > npm run build --prefix octofit-tracker/backend
   > npm run build --prefix octofit-tracker/frontend
   > ```

1. Confirme que o MongoDB está em execução, inicie a API em um terminal dedicado e mantenha-a em execução.

   > ![Static Badge](https://img.shields.io/badge/Terminal-text?logo=gnometerminal&labelColor=0969da&color=ddf4ff)
   >
   > ```bash
   > ps aux | grep mongod
   > npm run seed --prefix octofit-tracker/backend
   > npm run dev --prefix octofit-tracker/backend
   > ```

1. Em outro terminal, inicie o frontend e mantenha-o em execução.

   > ![Static Badge](https://img.shields.io/badge/Terminal-text?logo=gnometerminal&labelColor=0969da&color=ddf4ff)
   >
   > ```bash
   > npm run dev --prefix octofit-tracker/frontend -- --host 0.0.0.0
   > ```

1. Abra a aplicação no Codespace, verifique as quatro jornadas de usuário e provoque pelo menos um erro visível.

1. Abra um pull request de `build-octofit-app` para `main`, inclua evidências dos testes e use o resumo ou a revisão de código do Copilot para inspecionar o diff multicamadas.

1. Resolva os apontamentos válidos, execute novamente as verificações e faça merge do pull request.

<details>
<summary>Having trouble? 🤷 Precisa de ajuda?</summary><br/>

- Não faça merge de um pull request fechado ou com verificações falhando.
- Confirme que as URLs dependentes do ambiente usam o nome do Codespace apenas quando ele estiver presente.
- Consulte a execução do Actions para identificar a primeira camada com falha e reproduza-a localmente.
- Se a verificação final falhar após o merge, corrija o problema em `build-octofit-app`, execute novamente os testes acima e faça merge de um novo pull request em `main`. A avaliação final ocorre apenas em pull requests com merge.

</details>
