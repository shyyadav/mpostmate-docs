# PostMate

PostMate is a lightweight API testing client built right into Visual Studio Code.

With PostMate, you can:
- Create and manage API requests (GET, POST, PUT, DELETE, etc.)
- Organize requests into collections and folders
- Save and reuse environment variables
- View and inspect response headers and body
- Extract values from API responses and pass them into subsequent requests
- Parameterize test data for dynamic request generation
- Maintain request history for quick access

## Features

- 🌐 Send REST API requests  
- 📁 Organize collections & folders  
- 🔒 Manage environments  
- 🔄 Use dynamic variables across requests  
- 🧪 Extract values from responses and store them as variables  
- 🧩 Parameterize test data for flexible testing scenarios  
- 💾 Request history & persistence 
- 🔗 Request Chaining 
- 🧪 Assertion

![Demo Screenshot](https://raw.githubusercontent.com/shyyadav/mpostmate-docs/main/images/img.PNG)

## Getting Started

1. Click the **PostMate** icon in the Activity Bar.
2. Click "New Request" to get started.
3. Save your request to a collection or folder for reuse.
4. Use `{{yourVariable}}` syntax in request fields to reference saved environment or response variables.

📊 How to Use Data Tables in PostMate
Data Tables let you manage test data separately from your API requests. This is useful for sending different inputs in each run without manually editing variables.
1.	Go to Env tab in the sidebar and click on ham burger menu
2.	Create Environment 
3.	You can have multiple data table based on your need 
4.	Attach data table with your environment.
5.	Use data table variable like "{{variable}}” in url, header or body
6.	You can select the data while sending individual request
![Demo Screenshot](https://raw.githubusercontent.com/shyyadav/mpostmate-docs/main/images/datatable.PNG)

## Feedback

Please share feedback or feature requests via [GitHub Issues](https://github.com/shyyadav/mpostmate-docs/issues)
