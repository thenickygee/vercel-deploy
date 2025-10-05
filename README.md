# vercel-deploy
This is a yml file for a custom github action to help you deploy to vercel. 

Have you ever run into this error:

```diff
- Error: Git author [userEmail] must have access to the team [teamName] on Vercel to create deployments.
```

Add this yml file to your repo to be able to deploy to vercel when you push to main.

# Dir structure: 
- create: .github folder at root
- create: workflows dir in .github dir
- create: yml file with vercel.deploy.yml (or whatever you wanna name it)

# Github Actions Setup
- navigate to "Actions" tab from main repo page
- click: "Skip this and set up a workflow yourself"
- paste: yml file contents from this repo, or add the file locally and commit it to skip this step
- commit changes

- # Github Action Env Setup
- nagivate to "settings" tab from main repo page
<img width="1583" height="288" alt="settings" src="https://github.com/user-attachments/assets/8024ff75-ba59-4ebc-a854-da166b139734" />

- click on "Secrets and variables" from the sidebar options
<img width="1583" height="1044" alt="settings-2" src="https://github.com/user-attachments/assets/69f6b941-bea8-4dee-a359-e1bdc8086d7d" />

- click on "Actions" from the subnav
<img width="391" height="287" alt="settings-3" src="https://github.com/user-attachments/assets/7f645ab6-879a-4e9f-b596-288e0c3c43ad" />

- click on "New respository secret"
<img width="1418" height="939" alt="repo-sec" src="https://github.com/user-attachments/assets/a756319a-6cd2-4ded-991c-42b6412f2bfe" />

- add the 3 needed secrets
  - VERCEL_TOKEN
  - VERCEL_ORG_ID
  - VERCEL_PROJECT_ID
  <img width="1418" height="939" alt="repo-sec-2" src="https://github.com/user-attachments/assets/14714e6e-cbe2-45a1-a3f5-46802e186bcf" />
