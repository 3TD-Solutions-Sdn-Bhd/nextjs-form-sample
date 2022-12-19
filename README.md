# Fullstack Example with Next.js (REST API)

> Modified form [Prisma Examples](https://github.com/prisma/prisma-examples/tree/latest/typescript/rest-nextjs-api-routes)

This example shows how to implement a **fullstack app in TypeScript with [Next.js](https://nextjs.org/)** using [React](https://reactjs.org/) and [Prisma Client](https://www.prisma.io/docs/reference/tools-and-interfaces/prisma-client).

<details>
  <summary><h2>Deploy on Local</h2></summary>

### 🧑‍🍳 Before We Start

1. Create a [TiDB Cloud](https://tidbcloud.com/) account and get your free trial cluster.

### 1. Get connection details

1. Navigate to your TiDB Serverless cluster's dashboard.
2. Get **Endpoint**, **Port** and **User** field from the Connection tab.
3. Build your DATABASE_URL string: `mysql://<User>:<Password>@<Endpoint>:<Port>/bookshop`

![image](https://user-images.githubusercontent.com/35677990/202609001-ecf07f3d-a7a3-4376-9b7d-54f4096aaec6.jpg)

You will use this DATABASE_URL string to connect to TiDB Serverless cluster later.

### 2. Deploy on your workspace

1. Clone the code.
   ```shell
   git clone https://github.com/tidbcloud/nextjs-prisma-example.git
   cd nextjs-prisma-example
   ```
2. Set DATABASE_URL environment variables.
   ```shell
   export DATABASE_URL=${your_DATABASE_URL_string}
   ```
3. Install dependence.
   ```shell
   npm install .
   ```
4. Migrate your database.
   ````shell
   prisma migrate deploy
   ````
5. Run the project.
   ```shell
   npm run start
   ```

</details>

<details>
  <summary><h2>Deploy on Netlify</h2></summary>
### 🧑‍🍳 Before We Start

1. Create a [TiDB Cloud](https://tidbcloud.com/) account and get your free trial cluster.
2. Create a [Netlify](https://app.netlify.com/signup) account.

### 1. Get connection details

1. Navigate to your TiDB Serverless cluster's dashboard.
2. Get **Endpoint**, **Port** and **User** field from the Connection tab.
3. Build your DATABASE_URL string: `mysql://<User>:<Password>@<Endpoint>:<Port>/bookshop`

![image](https://user-images.githubusercontent.com/35677990/202609001-ecf07f3d-a7a3-4376-9b7d-54f4096aaec6.jpg)

You will use this DATABASE_URL string to connect to TiDB Serverless cluster later.

### 2. Deploy on Netlify

The **Deploy to Netlify** button will take you Netlify's deployment page. Then Netlify will help to clone this job to your own GitHub repository and automatically deploy it.

[![Deploy to Netlify button](https://www.netlify.com/img/deploy/button.svg)](https://app.netlify.com/start/deploy?repository=https://github.com/tidbcloud/nextjs-prisma-example)

1. Click the **Deploy to Netlify** button.
2. Click **Connect to GitHub** and authenticate GitHub account.
3. Fill in **Repository name** for your own GitHub repository.
4. Click **Save & Deploy**.
5. Navigate to **Site setting** panel.
6. Click **Add a variable** in the **Environment variables** sidebar.
7. Enter "DATABASE_URL" in the **Key** field.
8. Enter the DATABASE_URL string, set in the previous step, in the **Values** field.
9. Click **Create variable** to complete adding environment variable.
   ![image](https://user-images.githubusercontent.com/35677990/202992567-a25b9d32-6dc1-4a0c-bb22-50ab1b228582.jpg)
10. Navigate to **Deploys** panel.
11. Click **Trigger deploy** and choose **Deploy site**.

🎉 Mission Completes.

</details>

Now you can view your bookshop site on default domain generated by Netlify.