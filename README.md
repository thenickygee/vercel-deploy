# vercel-deploy
This is a yml file for a custom github action to help you deploy to vercel. 

Have you ever run into this error:

```diff
- Error: Git author [userEmail] must have access to the team [teamName] on Vercel to create deployments.
```

Add this yml file to your repo to be able to deploy to vercel when you push to main.

## Dir structure: 
- create: .github folder at root
- create: workflows dir in .github dir
- create: yml file with vercel.deploy.yml (or whatever you wanna name it)

## Github Actions Setup
- navigate to "Actions" tab from main repo page
- click: "Skip this and set up a workflow yourself"
- paste: yml file contents from this repo, or add the file locally and commit it to skip this step
- commit changes

## Github Action Env Setup
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

  ## Vercel Token Guides
  - VERCEL_TOKEN
  - VERCEL_ORG_ID
  - VERCEL_PROJECT_ID
 
  ### VERCEL_TOKEN:
  - click user profile in the top right
  - click 'Account Settings'
  - use left side navmenu to find "Tokens"
- <img width="320" height="484" alt="vercel-1" src="https://github.com/user-attachments/assets/d2eec758-0580-44d0-ae10-b123b174faf4" />
- <img width="290" height="526" alt="vercel-2" src="https://github.com/user-attachments/assets/9dfdd093-30ad-4785-9e1e-c72b9725cb23" />
- <img width="1266" height="529" alt="vercel-3" src="https://github.com/user-attachments/assets/5f88ea00-3371-4fc3-bd89-da790fdd1bc1" />
- <img width="488" height="281" alt="vercel-token" src="https://github.com/user-attachments/assets/07d885e0-be59-4078-866e-aab76e12782e" />

  - click 'create', to generate your token
  - copy and SAVE token - you will not be able to copy it again after you close the modal

  ### VERCEL_ORG_ID:
  - navigate to vercel.com/account
  <img width="1051" height="423" alt="vercel-org" src="https://github.com/user-attachments/assets/3a1add07-9791-44f3-8998-22bfc3cb6ec8" />
 - scrol down (or find) Team, copy team id
 <img width="1235" height="684" alt="vercel-org-2" src="https://github.com/user-attachments/assets/1091ce19-e3e9-4159-9842-3476e22d5d65" />


  ### VERCEL_PROJECT_ID:
  - navigate to dashboard
  - click elipses button on the desired project
  - click 'settings'
  - copy project id
<img width="485" height="380" alt="vercel-project-settings" src="https://github.com/user-attachments/assets/ada3e18d-ae34-49a9-8812-a05943afe0b6" />
<img width="1252" height="661" alt="vercel-project-token" src="https://github.com/user-attachments/assets/dcf5504d-5c9d-47cf-9a26-ae749efa0062" />

  Your action repo secrets should now look like this: 
  <img width="999" height="868" alt="sec-x3" src="https://github.com/user-attachments/assets/94713ff3-f58f-43a8-81c1-f690dd78b4b8" />

