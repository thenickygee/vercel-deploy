# vercel-deploy
This is a yml file for a custom github action to help you deploy to vercel. 

Have you ever run into this error:

```diff
- Error: Git author [userEmail] must have access to the team [teamName] on Vercel to create deployments.
```

Add this yml file to your repo to be able to deploy to vercel when you commit to main.

# Dir structure: 
- create: .github folder at root
- create: workflows dir in .github dir
- create: yml file with vercel.deploy.yml (or whatever you wanna name it)
