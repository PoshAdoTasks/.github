# PowerShell ADO Tasks

## 1. **Create Your Azure DevOps Task**

First, ensure you have created your Azure DevOps task. If you haven't, follow these instructions:

1. **Set up your environment:**
   - Install Node.js and npm: [Node.js Download](https://nodejs.org/)
   - Install TFX CLI: `npm install -g tfx-cli`

2. **Create the task:**
   - Create a new directory for your task: `mkdir my-azure-devops-task`
   - Navigate to the directory: `cd my-azure-devops-task`
   - Initialize the task: `tfx extension init --type ms.vss-distributed-task.task`

## 2. **Develop Your Task**

Develop your task by editing the `task.json` file and adding your task's logic in the required scripts.

## 3. **Package Your Task**

Package your task using the TFX CLI:

1. **Navigate to your task directory:**
   ```bash
   cd my-azure-devops-task
   ```

2. **Package the task:**
   ```bash
   tfx extension create --manifest-globs vss-extension.json
   ```

## 4. **Publish to the Azure DevOps Marketplace**

To publish your task to the Azure DevOps Marketplace, follow these steps:

1. **Sign in to the Marketplace:**
   - Go to [Azure DevOps Marketplace](https://marketplace.visualstudio.com/manage)
   - Sign in with your Microsoft account.

2. **Create a Publisher:**
   - If you don't have a publisher, create one by following the instructions here: [Create a Publisher](https://learn.microsoft.com/en-us/azure/devops/extend/publish/create-publisher?view=azure-devops)

3. **Upload Your Extension:**
   - Navigate to your publisher's page.
   - Click on "New Extension" and select "Azure DevOps."
   - Upload the `.vsix` file created in the packaging step.
   - Fill in the required details like name, description, and version.

4. **Submit for Review:**
   - Once uploaded, you need to submit your extension for review.
   - After the review, your extension will be available in the Azure DevOps Marketplace.

## 5. **Manage Your Packages**

Once your extension is published, you can manage your packages through the Azure DevOps Marketplace portal.

1. **Access Your Publisher Page:**
   - Go to [Azure DevOps Marketplace](https://marketplace.visualstudio.com/manage)
   - Click on your publisher name to access your publisher page.

2. **Manage Extensions:**
   - On your publisher page, you will see a list of your published extensions.
   - Click on the extension you want to manage.

3. **Update Your Extension:**
   - To upload a new version of your extension, click on "Update."
   - Select the updated `.vsix` file and fill in the necessary details.
   - Submit the updated version for review.

4. **Unpublish Your Extension:**
   - If you need to unpublish your extension, go to the extension details page.
   - Click on "Unpublish" and confirm your action.

5. **View Analytics:**
   - On the extension details page, you can view download statistics and user reviews.
   - Use these insights to improve your extension.

6. **Support and Documentation:**
   - Add support and documentation links to help users.
   - Update the extension description and release notes as needed.

## 6. **Install and Use Your Task**

Once your extension is published, you can install it in your Azure DevOps organization:

1. **Go to the Azure DevOps Marketplace:**
   - Find your published extension.
   - Click on "Get it free" and follow the instructions to install it in your Azure DevOps organization.

### Useful URLs:

- **Azure DevOps Marketplace:** [https://marketplace.visualstudio.com/azuredevops](https://marketplace.visualstudio.com/azuredevops)
- **TFX CLI:** [https://www.npmjs.com/package/tfx-cli](https://www.npmjs.com/package/tfx-cli)
- **Azure DevOps Task SDK:** [https://github.com/microsoft/azure-pipelines-task-lib](https://github.com/microsoft/azure-pipelines-task-lib)
- **Create a Publisher:** [https://learn.microsoft.com/en-us/azure/devops/extend/publish/create-publisher?view=azure-devops](https://learn.microsoft.com/en-us/azure/devops/extend/publish/create-publisher?view=azure-devops)
