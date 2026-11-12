## Step 4: Crie e teste a camada de apresentação React

Continue na branch `build-octofit-app` e delimite cada solicitação ao Copilot pelos testes desta camada.

### 📖 Theory: Estados da interface fazem parte do contrato

A camada de apresentação deve mostrar os estados de carregamento, vazio, sucesso e erro, mantendo a construção de URLs da API fora dos componentes individuais. O React Router oferece telas navegáveis para as funcionalidades, e os testes de componentes comprovam que os dados da API produzem uma interface acessível e significativa. Testar esses estados torna a interface gerada pelo Copilot mais confiável e fácil de manter.

### ⌨️ Activity: Crie e teste a camada de apresentação React

1. Inspecione o cliente de API compartilhado, as rotas incompletas e os testes de componentes.

1. Peça ao Copilot a menor alteração de interface necessária para um teste que falha.

   > ![Static Badge](https://img.shields.io/badge/Prompt-text?style=for-the-badge&logo=github-copilot&logoColor=white&labelColor=purple&color=purple)
   >
   > ```text
   > Use o teste de frontend que falha para implementar a menor alteração de interface possível. Reutilize o cliente de API compartilhado e preserve os estados de carregamento, vazio e erro.
   > ```

1. Repita para atividades, equipes, placar e sugestões de treino. Cada rota precisa de estados de carregamento, vazio, sucesso e erro; as sugestões devem chamar `/api/workouts/suggestions/:userEmail` para um usuário dos dados iniciais, como `mona@example.com`.

   > ![Static Badge](https://img.shields.io/badge/Terminal-text?logo=gnometerminal&labelColor=0969da&color=ddf4ff)
   >
   > ```bash
   > npm test --prefix octofit-tracker/frontend
   > ```

1. Gere o build e inspecione manualmente a aplicação Vite no Codespace.

   > ![Static Badge](https://img.shields.io/badge/Terminal-text?logo=gnometerminal&labelColor=0969da&color=ddf4ff)
   >
   > ```bash
   > npm run build --prefix octofit-tracker/frontend
   > npm run dev --prefix octofit-tracker/frontend -- --host 0.0.0.0
   > ```

1. Faça commit e push da camada de apresentação.

<details>
<summary>Having trouble? 🤷 Precisa de ajuda?</summary><br/>

- Mantenha o cliente compartilhado em caminhos relativos `/api`, com substituição opcional por `import.meta.env.VITE_API_BASE_URL`. O proxy do Vite os encaminha para a porta privada 8000.
- Não repita a lógica de requisições nos componentes: cada componente de rota importa `getJson` de `src/api/client.ts` e nunca chama `fetch` diretamente.
- Quando os testes falharem, verifique nomes acessíveis e a semântica das mensagens de status e erro.

</details>
