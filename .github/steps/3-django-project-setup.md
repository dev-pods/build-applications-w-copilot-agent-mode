## Etapa 3: Inicializar e criar o banco de dados MongoDB octofit_db, projeto/app Django, atualizar arquivos do projeto/app Django e popular o banco de dados MongoDB

In this step, we will accomplish the following:

- Set up the octofit_db MongoDB database structure.
- Update the octofit-tracker/backend/octofit_tracker app files:
  - settings, models, serializers, urls, views, tests, and admin files.
- Populate the octofit_db database with test data.
- Verify the test data is populated in the octofit_db database.

Copie e cole o(s) seguinte(s) prompt(s) no GitHub Copilot Chat e selecione "Agent" ao invés de "Ask" ou "Edit" no menu suspenso onde você está inserindo o prompt.

> [!NOTE]
> - Tenha em mente que o modo agent do Copilot é conversacional, então ele pode fazer perguntas para você e você pode fazer perguntas para ele também.
> - Aguarde um momento para o Copilot responder e pressione o botão `Continue` para executar comandos apresentados pelo modo agent do Copilot.
> - Mantenha os arquivos criados e atualizados pelo modo agent do Copilot até que ele termine.
> - O modo agent tem a habilidade de avaliar sua base de código e executar comandos e adicionar/refatorar/deletar partes da sua base de código e se auto-curar automaticamente se ele ou você comete um erro no processo.

**Abra uma nova sessão do Copilot Chat clicando no ícone de mais `+` no painel do Copilot Chat.**

### :keyboard: Activity: Setup the Python Django project/app

In this activity we will leverage a feature in VS Code called prompt files. A prompt file that has been created by the IT department for us to create our Django project application. Copy/paste the following prompt in the GitHub Copilot Chat and select the "Agent" instead of "Ask" or "Edit" from the drop down where you are inserting the prompt.

What are prompt files?

Prompt files let you define reusable prompts for common and repeatable development tasks in a Markdown file.
Prompt files are standalone prompts that you can run directly in chat. You can include task-specific context and guidelines about how the task should be performed.
Combine prompt files with custom instructions to ensure consistent execution of complex tasks.

See the [VS Code Docs: Prompt Files](https://code.visualstudio.com/docs/copilot/customization/overview#_prompt-files) page for more information.

> ![Static Badge](https://img.shields.io/badge/-Prompt-text?style=flat-square&logo=github%20copilot&labelColor=512a97&color=ecd8ff)
>
> ```prompt
> /create-django-project
>```

> [!NOTE]
> - Wait a moment for the Copilot to respond and press the `Continue` button to execute each command presented by Copilot agent mode.
> - Keep files created and updated until the Copilot agent mode has finished.

> [!IMPORTANT]
> - Don't start the Python Django app in the way that GitHub Copilot agent mode suggests hit **cancel** when you see this image.

<img src="https://github.com/user-attachments/assets/02a875c1-19a4-417b-ab03-aefbbe2186d4" width=50% height=50%>

### :keyboard: Activity: Initialize, create, and populate the octofit_db MongoDB database

Let's continue to leverage a prompt file that has been created by the IT department for us to initialize and create the octofit_db MongoDB database. Copy/paste the following prompt in the GitHub Copilot Chat and select the "Agent" instead of "Ask" or "Edit" from the drop down where you are inserting the prompt.

> ![Static Badge](https://img.shields.io/badge/-Prompt-text?style=flat-square&logo=github%20copilot&labelColor=512a97&color=ecd8ff)
>
> ```prompt
>
> /init-populate-octofit_db
> ```

### :keyboard: Activity: Let's create a prompt file that will update the Python Django project/app files

Now let's create a prompt file of our own that we can share with other staff to develop to build the octofit-tracker app. Copy/paste the following prompt in the GitHub Copilot Chat and select the "Agent" instead of "Ask" or "Edit" from the drop down where you are inserting the prompt.

> ![Static Badge](https://img.shields.io/badge/-Prompt-text?style=flat-square&logo=github%20copilot&labelColor=512a97&color=ecd8ff)
>
> ```prompt
> Let's add the following to a prompt file called `update-octofit-tracker-app.prompt.md` in the `.github/prompts` directory and add mode: 'agent' and model: GPT-4.1 to the prompt file.
>
> # Django App Updates
>
> - All Django project files are in the `octofit-tracker/backend/octofit_tracker` directory.
>
> 1. Update `settings.py` for MongoDB connection and CORS.
> 2. Update `models.py`, `serializers.py`, `urls.py`, `views.py`, `tests.py`, and `admin.py` to support users, teams, activities, leaderboard, and workouts collections.
> 3. Ensure `/` points to the api and `api_root` is present in `urls.py`.
> ```

> [!TIP]
> Use prompt files to define repeatable tasks and workflows.
>
> When writing prompts focus on **WHAT** needs to be done. You can reference instructions for the **HOW**.

See the [VS Code Docs: Prompt Files](https://code.visualstudio.com/docs/copilot/customization/overview#_prompt-files) page for more information.

### :keyboard: Activity: Let's use the prompt file to update the Python Django project/app files

Copy/paste the following prompt in the GitHub Copilot Chat and select the "Agent" instead of "Ask" or "Edit" from the drop down where you are inserting the prompt.

> ![Static Badge](https://img.shields.io/badge/-Prompt-text?style=flat-square&logo=github%20copilot&labelColor=512a97&color=ecd8ff)
>
> ```prompt
> /update-octofit-tracker-app
> ```
>

> [!IMPORTANT]
> - Don't start the Python Django app in the way that GitHub Copilot agent mode suggests hit **cancel** when you see this image.

<img src="https://github.com/user-attachments/assets/02a875c1-19a4-417b-ab03-aefbbe2186d4" width=50% height=50%>

1. Now that we have created the database structure, updated our Django project files, and populated the database, let's check our changes into our `build-octofit-app` branch.

1. With our new changes complete, please **commit** and **push** the changes to GitHub.

1. Wait a moment for Mona to check your work, provide feedback, and share the next lesson so we can keep working!

<details>
<summary>Having trouble? 🤷</summary><br/>

If you don't get feedback, here are some things to check:

- Make sure your commit changes were made for the following files to the branch `build-octofit-app` and pushed/synchronized to GitHub:
  - `octofit-tracker/backend/octofit_tracker/settings.py`
  - `octofit-tracker/backend/octofit_tracker/management/commands/populate_db.py`
- If Mona found a mistake, simply make a correction and push your changes again. Mona will check your work as many times as needed.

</details>
