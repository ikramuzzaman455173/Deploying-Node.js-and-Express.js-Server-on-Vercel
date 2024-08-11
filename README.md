

## Deploying Node.js and Express.js Server on Vercel

### Table of Contents
1. [Introduction](#1-introduction)
2. [Prerequisites](#2-prerequisites)
3. [Step 1: Create `vercel.json` Configuration File](#3-step-1-create-verceljson-configuration-file)
4. [Step 2: Install Vercel CLI](#4-step-2-install-vercel-cli)
5. [Step 3: Login to Vercel](#5-step-3-login-to-vercel)
6. [Step 4: Deploy the Project](#6-step-4-deploy-the-project)
7. [Step 5: Add Environment Variables](#7-step-5-add-environment-variables)
8. [Step 6: Deploy to Production](#8-step-6-deploy-to-production)
9. [Conclusion](#9-conclusion)

---

### 1. Introduction
In this guide, you'll learn how to deploy a Node.js and Express.js server to Vercel. This step-by-step documentation ensures that your server is properly configured and deployed, including how to set up environment variables.

---

### 2. Prerequisites
- Node.js and Express.js installed in your project.
- Vercel account (Sign up at [vercel.com](https://vercel.com/)).
- Vercel CLI installed on your local machine.
- Basic knowledge of using the command line.

---

### 3. Step 1: Create `vercel.json` Configuration File
In your project root directory, create a file named `vercel.json` with the following content:

```json
{
	"version": 2,
	"builds": [
		{
			"src": "./index.js",
			"use": "@vercel/node"
		}
	],
	"routes": [
		{
			"src": "/(.*)",
			"dest": "/",
			"methods": ["GET", "POST", "PATCH", "DELETE", "OPTIONS"]
		}
	]
}
```

- **version**: Specifies the version of the Vercel configuration format.
- **builds**: Defines the build steps for the project. Replace `"./index.js"` with the path to your main server file.
- **routes**: Specifies the routes and methods to handle, redirecting all requests to the server's root.

---

### 4. Step 2: Install Vercel CLI
If you haven't already installed the Vercel CLI, open your terminal and run:

```bash
npm install -g vercel
```

This command installs the Vercel CLI globally on your system.

---

### 5. Step 3: Login to Vercel
To connect your local environment with your Vercel account, login using the Vercel CLI:

```bash
vercel login
```

Follow the prompts to authenticate your account.

---

### 6. Step 4: Deploy the Project
Now that you are logged in, deploy your project for the first time:

```bash
vercel
```

- Follow the prompts to set up your project on Vercel.
- Vercel will deploy your project and provide you with a preview URL.

---

### 7. Step 5: Add Environment Variables
After deploying your server, you may need to add environment variables. To do this:

1. Go to the [Vercel Dashboard](https://vercel.com/dashboard).
2. Find your project and click on it.
3. Navigate to the **Settings** tab.
4. Scroll down to **Environment Variables** and add your variables as needed.

---

### 8. Step 6: Deploy to Production
After setting up everything, deploy your server to production with:

```bash
vercel --prod
```

This will deploy your server to the production environment, making it live.

---

### 9. Conclusion
Your Node.js and Express.js server is now successfully deployed on Vercel. Make sure to use the Vercel Dashboard to manage your deployments and environment variables.

---

### [🔝 Go to Top](#deploying-nodejs-and-expressjs-server-on-vercel)
