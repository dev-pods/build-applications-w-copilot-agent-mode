## Etapa 6: Usando GitHub Copilot dentro de um pull request

Parabéns! Você terminou de codificar para este exercício (e VS Code). Agora é hora de fazer merge do nosso trabalho. :tada: Para finalizar, vamos aprender sobre dois recursos de acesso limitado do Copilot que podem acelerar nossos pull requests!

#### Sumários de Pull Request do Copilot

Tipicamente, você revisaria suas anotações e mensagens de commit e então as resumiria para a descrição do seu pull request. Isso pode levar algum tempo, especialmente se as mensagens de commit são inconsistentes ou o código não está bem documentado. Felizmente, o Copilot pode considerar todas as mudanças no pull request e fornecer os destaques importantes, e com referências também!

> [!NOTE]  
> This is unavailable with the **Copilot Free** tier. [[docs]](https://docs.github.com/en/enterprise-cloud@latest/copilot/using-github-copilot/using-github-copilot-for-pull-requests/creating-a-pull-request-summary-with-github-copilot)

#### Copilot code review

More eyes on our work is always useful so let's ask Copilot to do a first pass before we do a normal peer review process. Copilot is great at catching common mistakes that can be fixed by simple adjustment, but please remember to use it responsibly.

### :keyboard: Activity: Summarize and review a PR with Copilot

1. In a web browser, open another tab and navigate to your exercise repository.

1. You might notice a **notification banner** suggesting to create a new pull request. Click that or use the **Pull Requests** tab at the top to create a new pull request. Please use the following details:

   - **base:** `main`
   - **compare:** `build-octofit-app`
   - **title:** `Add registration validation and more activities`

1. (Optional) In the **Add a description** area, enter edit mode if needed, then click the **Copilot actions** icon and **Summary** action. After a moment, Copilot will add a description. :memo:

   <img alt="Copilot summarize button " width="300px" src="https://github.com/user-attachments/assets/3fc5fab4-db03-4ab8-8a16-cdd71ec2ded0">

1. (Optional) In the right side information panel at the top, locate the **Reviewers** section and click the **Request** button next to a **Copilot icon**. Wait a moment for Copilot to add a review comment to your pull request!

   <img alt="Copilot review button" width="300px" src="https://github.com/user-attachments/assets/39b15002-a235-4c25-b09d-6a8097e27b62">

   > 🪧 **Note:** Notice a log entry that Copilot was requested for a review.

1. At the bottom, press the **Merge pull request** button. Nice work! You are all done! :tada:

1. Wait a moment for Mona to check your work, provide feedback, and post a final review of this lesson!
