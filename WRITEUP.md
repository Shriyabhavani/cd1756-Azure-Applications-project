# Write-up Template

### Analyze, choose, and justify the appropriate resource option for deploying the app.

For this project, the CMS application was deployed using Azure App Service rather than a Virtual Machine.Azure App Service is a Platform as a Service (PaaS) that allows developers to deploy web applications without managing the underlying infrastructure. This makes it ideal for hosting Flask applications like the CMS used in this project.Using Azure App Service provides several advantages compared to a Virtual Machine.
First, deployment is simpler because the application can be connected directly to a GitHub repository and deployed automatically using GitHub Actions. This eliminates the need to manually configure servers.
Second, Azure manages the operating system, security patches, and runtime environment. In contrast, using a Virtual Machine would require manually installing Python, Flask, and other dependencies as well as maintaining the server.
Third, Azure App Service provides built-in features such as logging, HTTPS support, environment variable configuration, and easy integration with Azure SQL Database and Azure Blob Storage. These services were used in this project to store application data and images.
Finally, App Service is more cost-effective for small web applications because it uses a managed hosting plan rather than a full virtual machine.
For these reasons, Azure App Service was selected as the hosting solution for this CMS application.

### Assess app changes that would change your decision.

Although Azure App Service was the best choice for this project, there are situations where using a Virtual Machine would be more appropriate.
If the application required full control over the operating system, custom networking configurations, or installation of specialized software that is not supported in App Service, then a Virtual Machine would be a better option. Additionally, if the application required running multiple background services, custom server configurations, or complex infrastructure management, a VM would provide the necessary flexibility.
In such cases, a Virtual Machine would allow developers to configure the environment exactly as needed. However, for this CMS application, the managed environment provided by Azure App Service was sufficient and more efficient.
