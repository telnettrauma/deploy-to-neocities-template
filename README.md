# deploy-to-neocities Template

Template for using GitHub to deploy a website to Neocities

## Instructions

This tutorial uses [GitHub Desktop](https://github.com/apps/desktop) and [Visual Studio Code](https://code.visualstudio.com)

### 1. Downloading your site

1. Go to your Neocities dashboard (the dashboard is the page with all your files, click "Edit site" from the homepage)
2. Scroll to the bottom of the dashboard and click "Download entire site"
3. Save the `.zip` file
4. Extract this folder. Keep the Neocities tab open, we will come back to it later

### 2. Copying this repository

1. Scroll to the top of the GitHub page for [this repository](https://github.com/telnettrauma/deploy-to-neocities-template)
2. Click "Use this template" near the top of the page and select "Create a new repository" from the dropdown

![Screenshot of a mouse cursor clicking "Create a new repository" from the "Use this template" dropdown](https://i.imgur.com/lAQmMwI.png)

3. Name the repository whatever you want
4. You can set the repository to public or private. If you set the repository to private, only you will be able to see it on GitHub, but you can still publicly publish to Neocities.
5. Click "Create repository" and your repository will be created

### 3. Setting up Neocities

1. Return to the Neocities tab in your browser
2. Click the account menu in the top-right and select "Settings"

![Screenshot of "Settings" being hovered over in an account dropdown](https://i.imgur.com/i9V9Stp.png)

3. In the list of your sites, select "Manage Site Settings"

![Screenshot of "Manage Site Settings" being hovered over in the Neocities account settings page](https://i.imgur.com/NYWPQtQ.png)

4. Switch to the "API" tab
5. Select "Generate API Key"

![Screenshot of the Neocities API key screen](https://i.imgur.com/9iRvbuD.png)

6. Copy your API key. **Make sure not to give this key to anybody, as it will allow them to modify your entire site!**
7. Return to your repository on GitHub and click "Settings"
8. On the sidebar, expand "Secrets and variables" and select "Actions"
9. In the "Secrets" tab, scroll down to "Repository secrets" (**not** "Environment secrets") and click "New repository secret"
10. Name this secret `NEOCITIES_API_TOKEN` and paste your key into "Secret"
11. Add the secret

### 4. Moving files over

1. Return to the "Code" page in your repository
2. Click the green "Code" button and select "Open with GitHub Desktop." This will open GitHub Desktop

![Screenshot of "Open with GitHub Desktop" being hovered over in the GitHub repository Code menu](https://i.imgur.com/9K1NUvB.png)

3. Click "Open in Visual Studio Code" to open Visual Studio Code

![Screenshot of the GitHub Desktop interface with the mouse cursor hovering over "Open in Visual Studio Code"](https://i.imgur.com/LneVfRM.png)

4. Once Visual Studio Code is open, copy the files from your extracted site `.zip` folder and paste them into the `public` folder

> [!NOTE]
> Everything inside the `public` folder will be the structure of your website. For example, a file located at `public/file.html` will be `username.neocities.org/file.html`, or a file at `public/folder/file.html` will be located at `username.neocities.org/folder/file.html`

5. Now it's time to publish! You do this by creating a "commit." A commit is a series of changes that can be jumped back to. It doesn't matter how often you commit, do it as often as you like! Here are 2 methods to commit:

#### A. Visual Studio Code

1. Select the "Source Control" option from the sidebar (it looks like a line with a branching path)

![Screenshot of the "Source Control" button being hovered over in Visual Studio Code](https://i.imgur.com/pikR4kt.png)

2. Describe the changes you made in the "Message" box
3. Click "Commit"
4. Visual Studio Code may panic because you haven't "staged" any changes. It should prompt you to enable "Smart Commit Changes," which will allow you to commit all changes automatically