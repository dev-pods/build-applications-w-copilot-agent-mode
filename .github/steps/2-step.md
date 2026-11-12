## Step 2: Implemente a camada de dados MongoDB

Continue na branch `build-octofit-app` e delimite cada solicitação ao Copilot pelos testes desta camada.

### 📖 Theory: Invariantes de modelos e dados representativos

Os schemas Mongoose devem expressar as regras de que o restante da aplicação depende, em vez de apenas espelhar JSON arbitrário. Relacionamentos e validações de atividades, equipes, entradas do placar e sugestões de treino tornam o comportamento da API previsível. Testes focados e dados iniciais representativos revelam erros nos schemas antes de se tornarem problemas HTTP ou de interface.

### ⌨️ Activity: Implemente a camada de dados MongoDB

1. Leia os testes de contrato dos dados e os modelos incompletos em `octofit-tracker/backend`.

1. Peça ao Copilot um plano delimitado à camada de dados.

   > ![Static Badge](https://img.shields.io/badge/Prompt-text?style=for-the-badge&logo=github-copilot&logoColor=white&labelColor=purple&color=purple)
   >
   > ```text
   > Explique por que os testes da camada de dados falham e proponha alterações limitadas aos modelos Mongoose e aos dados iniciais. Preserve os contratos e não edite arquivos da API ou do React.
   > ```

1. Implemente schemas e dados iniciais em pequenas alterações, executando os testes de dados após cada funcionalidade. Use chaves estáveis e upserts para que novas execuções preservem registros não relacionados no MongoDB.

   > ![Static Badge](https://img.shields.io/badge/Terminal-text?logo=gnometerminal&labelColor=0969da&color=ddf4ff)
   >
   > ```bash
   > npm run test:data --prefix octofit-tracker/backend
   > ```

1. Carregue os registros representativos no MongoDB do Codespace e execute o comando duas vezes para confirmar que é idempotente.

   > ![Static Badge](https://img.shields.io/badge/Terminal-text?logo=gnometerminal&labelColor=0969da&color=ddf4ff)
   >
   > ```bash
   > npm run seed --prefix octofit-tracker/backend
   > npm run seed --prefix octofit-tracker/backend
   > ```

1. Revise as regras de validação e os relacionamentos no diff; depois, faça commit e push.

<details>
<summary>Having trouble? 🤷 Precisa de ajuda?</summary><br/>

- Use modelos Mongoose em vez de scripts diretos do MongoDB.
- Crie dados para as quatro funcionalidades e mantenha execuções repetidas idempotentes.
- Investigue a primeira asserção que falhar, em vez de regenerar todos os modelos.

</details>
