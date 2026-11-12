## Step 1: Leia a arquitetura e estabeleça uma baseline de testes

Boas-vindas, @{{ login }}! Você vai ampliar o OctoFit Tracker para um programa de fitness escolar. Comece lendo os contratos e reproduzindo as falhas atuais.

### 📖 Theory: Contratos antes da geração

O modo Agent é mais confiável quando recebe limites explícitos e critérios de aceitação executáveis. O documento de arquitetura explica as responsabilidades de React, Express e MongoDB, enquanto os testes com falha mostram o que está incompleto de propósito. Leia ambos antes de editar para pedir ao Copilot um plano delimitado, em vez de uma geração ampla da aplicação.

### ⌨️ Activity: Leia a arquitetura e estabeleça uma baseline de testes

1. Abra o botão abaixo em outra aba e crie um Codespace para sua cópia do exercício com a configuração padrão.

   [![Open in GitHub Codespaces](https://github.com/codespaces/badge.svg)](https://codespaces.new/{{full_repo_name}}?quickstart=1)

1. No Codespace, crie e publique uma branch chamada `build-octofit-app`.

1. Verifique se o MongoDB está em execução antes dos testes de integração.

   > ![Static Badge](https://img.shields.io/badge/Terminal-text?logo=gnometerminal&labelColor=0969da&color=ddf4ff)
   >
   > ```bash
   > ps aux | grep mongod
   > ```

1. Instale as dependências das duas camadas e registre a baseline de testes com falha.

   > ![Static Badge](https://img.shields.io/badge/Terminal-text?logo=gnometerminal&labelColor=0969da&color=ddf4ff)
   >
   > ```bash
   > npm ci --prefix octofit-tracker/backend
   > npm ci --prefix octofit-tracker/frontend
   > npm test --prefix octofit-tracker/backend
   > npm test --prefix octofit-tracker/frontend
   > ```

1. No chat do Copilot, selecione **Agent** no agent picker. Confira os permission levels e revise as solicitações de aprovação. Peça ao Copilot que inspecione antes de editar:

   > ![Static Badge](https://img.shields.io/badge/Prompt-text?style=for-the-badge&logo=github-copilot&logoColor=white&labelColor=purple&color=purple)
   >
   > ```text
   > Leia docs/architecture.md e resuma os limites das camadas, os testes que falham atualmente e a menor ordem segura de implementação. Não edite arquivos.
   > ```

1. Preencha as decisões de implementação e o plano de testes em `docs/architecture.md`; depois, faça commit e push da branch.

<details>
<summary>Having trouble? 🤷 Precisa de ajuda?</summary><br/>

- Use `--prefix` para executar todos os comandos a partir da raiz do repositório.
- Não altere a configuração de portas do exercício.
- Se o MongoDB não estiver em execução, consulte as orientações de configuração do Codespaces antes de continuar.

</details>
