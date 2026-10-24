# Colab AI + GitHub Starter

A beginner-friendly notebook project that:
1. Runs in Google Colab.
2. Calls an AI API using an API key.
3. Creates a GitHub repository and uploads project files using a GitHub Personal Access Token.

## Important security note
Never paste tokens directly into notebook code, commit them to GitHub, or share a notebook containing them. Use **Google Colab Secrets** (the key icon in the left sidebar). Give the GitHub token only the permissions needed to create a repository and push contents. Revoke a token if it is accidentally exposed.

## Quick start
1. Download `colab_ai_github_starter.ipynb` from this project and upload it to Google Drive, or open it in Colab.
2. In Colab, open **Secrets** (key icon) and add:
   - `OPENAI_API_KEY`: your AI provider API key.
   - `GITHUB_TOKEN`: a GitHub Personal Access Token with repository creation and contents-write permissions. Fine-grained token permissions and organization policies may vary.
3. Turn on notebook access to both secrets when Colab prompts you.
4. Run the notebook cells from top to bottom.
5. In the AI demo cell, type a question and run it.
6. In the GitHub publish cell, choose a unique repository name and run it. The notebook creates a public repository and uploads `app.py` and `README.md`.
7. To add the notebook itself to the repo, in Colab choose **File → Download → Download .ipynb**, then upload that downloaded notebook to the new GitHub repository (or add a notebook-upload cell using the GitHub Contents API).

## What the tokens do
- `OPENAI_API_KEY` authenticates the AI API request. API usage may incur charges depending on your provider/account.
- `GITHUB_TOKEN` authenticates GitHub REST API requests that create a repo and upload files.

## Troubleshooting
- `401` from the AI API: check the API key and provider billing/access.
- `401` or `403` from GitHub: check the token, its permissions, and any organization policy.
- `422` from GitHub: the repository name may already be taken or the request is invalid; choose a new name.
- Do not share the public repository with secrets or personal data.
