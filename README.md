# Vercel Deploy GitHub Action

A custom GitHub Action workflow to deploy your project to Vercel automatically when pushing to main.

## Problem Solved

Have you ever encountered this error?

```diff
- Error: Git author [userEmail] must have access to the team [teamName] on Vercel to create deployments.
```

This workflow solves that issue by properly configuring automated Vercel deployments through GitHub Actions.

---

## Setup Guide

### 1. Directory Structure

Create the following structure in your repository:

```
.github/
└── workflows/
    └── vercel-deploy.yml
```

### 2. GitHub Actions Configuration

1. Navigate to the **Actions** tab from your main repository page
2. Click **"Skip this and set up a workflow yourself"**
3. Paste the YML file contents from this repo (or add the file locally and commit to skip this step)
4. Commit the changes
5. Pull the changes to get the file locally

### 3. Environment Variables Setup

#### Add Repository Secrets

1. Navigate to the **Settings** tab from your main repository page
   
   ![Settings](https://github.com/user-attachments/assets/8024ff75-ba59-4ebc-a854-da166b139734)

2. Click on **"Secrets and variables"** from the sidebar
   
   ![Secrets and Variables](https://github.com/user-attachments/assets/69f6b941-bea8-4dee-a359-e1bdc8086d7d)

3. Click on **"Actions"** from the subnav
   
   ![Actions Subnav](https://github.com/user-attachments/assets/7f645ab6-879a-4e9f-b596-288e0c3c43ad)

4. Click **"New repository secret"**
   
   ![New Repository Secret](https://github.com/user-attachments/assets/a756319a-6cd2-4ded-991c-42b6412f2bfe)

5. Add the following three secrets:
   - `VERCEL_TOKEN`
   - `VERCEL_ORG_ID`
   - `VERCEL_PROJECT_ID`
   
   ![Repository Secrets](https://github.com/user-attachments/assets/14714e6e-cbe2-45a1-a3f5-46802e186bcf)

---

## Getting Your Vercel Credentials

### VERCEL_TOKEN

1. Click your user profile in the top right corner
2. Click **"Account Settings"**
3. Navigate to **"Tokens"** from the left sidebar

   ![Vercel Navigation](https://github.com/user-attachments/assets/d2eec758-0580-44d0-ae10-b123b174faf4)
   
   ![Tokens Menu](https://github.com/user-attachments/assets/9dfdd093-30ad-4785-9e1e-c72b9725cb23)
   
   ![Tokens Page](https://github.com/user-attachments/assets/5f88ea00-3371-4fc3-bd89-da790fdd1bc1)

4. Click **"Create"** to generate your token
   
   ![Create Token](https://github.com/user-attachments/assets/07d885e0-be59-4078-866e-aab76e12782e)

5. Copy and **save the token** - you won't be able to access it again after closing the modal

### VERCEL_ORG_ID

1. Navigate to [vercel.com/account](https://vercel.com/account)
   
   ![Account Page](https://github.com/user-attachments/assets/3a1add07-9791-44f3-8998-22bfc3cb6ec8)

2. Scroll down to find **"Team"** and copy the Team ID
   
   ![Team ID](https://github.com/user-attachments/assets/1091ce19-e3e9-4159-9842-3476e22d5d65)

### VERCEL_PROJECT_ID

1. Navigate to your Vercel dashboard
2. Click the **ellipses button (...)** on your desired project
3. Click **"Settings"**
   
   ![Project Settings](https://github.com/user-attachments/assets/ada3e18d-ae34-49a9-8812-a05943afe0b6)

4. Copy the **Project ID**
   
   ![Project ID](https://github.com/user-attachments/assets/dcf5504d-5c9d-47cf-9a26-ae749efa0062)

### Verification

Your repository secrets should now look like this:

![All Secrets Configured](https://github.com/user-attachments/assets/94713ff3-f58f-43a8-81c1-f690dd78b4b8)

---

## Deploy

Commit and push to main! You should see:

1. The GitHub Action trigger and pass
   
   ![Action Success](https://github.com/user-attachments/assets/0a9e0b38-3eca-496c-abd8-836246b029f9)

2. Your project deploy to Vercel
   
   ![Vercel Deployment](https://github.com/user-attachments/assets/e7cd6f72-abd6-4eea-a6c1-8d4a3186b9d2)

---

## 🫡 You're all set!

Your Vercel deployments will now trigger automatically on every push to main.
