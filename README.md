# Prompt Design in Vertex AI

This README outlines the steps involved in designing and deploying prompts for a generative AI model within Google Cloud's Vertex AI platform.

## Project Setup

1. **Create a GitHub Repository:**
   * Go to your GitHub account and create a new repository.
   * Name it "Prompt-Design-in-Vertex-AI" (or a similar descriptive name).
   * Initialize the repository with a README file.

2. **Create a Vertex AI Workbench Instance:**
   * In the Google Cloud Console, navigate to Vertex AI Workbench.
   * Create a new instance.
   * Name it "generative-ai-jupyterlab" (or a similar name).
   * Choose a suitable machine type and region.

3. **Prepare Your Project Files:**
   * Download the following files from your Vertex AI Workbench instance:
     * `image-analysis.ipynb`
     * `tagline-generator.ipynb`
     * `Cymbal Product Analysis File`
     * `Cymbal Tagline Generator Template File`

## Setting Up Git

1. **Initialize Git:**
   * Open a terminal within your Vertex AI Workbench instance.
   * Navigate to the directory where you saved your project files.
   * Run the following command:
     ```bash
     git init
     ```

2. **Stage and Commit Files:**
   * Add all files to the staging area:
     ```bash
     git add .
     ```
   * Commit your changes with a message:
     ```bash
     git commit -m "Initial commit of cymbal project files"
     ```

3. **Configure Git Identity:**
   * Set your Git username and email:
     ```bash
     git config --global user.name "AvilashBhowmick12"
     git config --global user.email "avilash_b.it2021@gmail.com"
     ```

4. **Connect to Your GitHub Repository:**
   * Add your GitHub repository as a remote:
     ```bash
     git remote add origin https://github.com/AvilashBhowmick12/Prompt-Design-in-Vertex-AI.git
     ```

## Using a Personal Access Token (PAT)

1. **Generate a PAT:**
   * Go to your GitHub account settings.
   * Navigate to "Developer settings" -> "Personal access tokens".
   * Click "Generate new token".
   * Give it a descriptive name (e.g., "PAT-2023-10-26").
   * Select the "repo" scope.
   * Click "Generate token".
   * Copy the generated token immediately.

2. **Create a Credential Helper Script:**
   * In your Vertex AI Workbench instance, create a directory for your script:
     ```bash
     mkdir /home/jupyter/Prompt-Design-in-Vertex-AI
     cd /home/jupyter/Prompt-Design-in-Vertex-AI
     ```
   * Create a file named `git-credential-github.sh`:
     ```bash
     touch git-credential-github.sh
     ```
   * Edit the file using `nano` or `vim`:
     ```bash
     nano git-credential-github.sh
     ```
   * Paste the following code into the file, replacing `$YOUR_PAT` with your actual PAT:
     ```bash
     #!/bin/bash
     echo "username=AvilashBhowmick12"
     echo "password=$YOUR_PAT"
     ```
   * Make the file executable:
     ```bash
     chmod +x git-credential-github.sh
     ```

3. **Configure Git to Use the Credential Helper:**
   * Run the following command:
     ```bash
     git config --global credential.helper '!/home/jupyter/Prompt-Design-in-Vertex-AI/git-credential-github.sh'
     ```

## Pushing Your Project to GitHub

1. **Push to GitHub:**
   * Run the following command:
     ```bash
     git push -u origin main
     ```

## Important Notes

* **Security:** Store your PAT securely. Don't share it with anyone.
* **Token Expiration:** Set an expiration date for your PAT and regenerate it when needed.
* **Scope:** Choose the appropriate scopes for your PAT. Only grant the permissions you need.

## Conclusion

This README provides a comprehensive guide to setting up your project, using Git, and pushing your code
