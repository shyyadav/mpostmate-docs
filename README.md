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
- 📦 Collection Run

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

📊 
### Test / Assertion: 
Postmate provides both scripting as well as writing test just in plain English for most ovious type of assertion.

**_Writing tests just like plain English:_** go to Tests tab and click on Test sub tab.  
You can have tests in tabular form where **_every row is a test_**. Test rows have 5 columns Test Types, Action, Expected, Test Description and a delete icon at last.

**_Test Type:_**

 1. **Set Env Variable:** in case you want some data from the response to be stored in environment variable to use later or next request
 ---
 _**Tip:** just run your request once before you start writing test, so that you’ll get json path in suggestion to select._
 ![json path helper](https://github.com/shyyadav/mpostmate-docs/blob/main/images/jsonPathHelper.PNG?raw=true)
***Example use case:*** you want to store authorization-token in variable so that you can use it another request.
![test type1](https://github.com/shyyadav/mpostmate-docs/blob/main/images/testType1.PNG?raw=true)

📊 Write java script code to manupulate api response.
- Reponse body (RESPONSE.body)
- Response status (RESPONSE.status)

- Example:
```const resp = RESPONSE.body;
   const students = resp.students;
   students.forEach(s =>{
      console.log(s.name);
   });
```
![Demo Screenshot](https://raw.githubusercontent.com/shyyadav/mpostmate-docs/main/images/Test.png)

📦 Collection Run:
![Demo Screenshot](https://raw.githubusercontent.com/shyyadav/mpostmate-docs/main/images/collectionRunner.PNG)
![Demo Screenshot](https://raw.githubusercontent.com/shyyadav/mpostmate-docs/main/images/RunResult.PNG)

## Licensing & Dependencies

Copyright: © 2025 Shyam Narayan Yadav. All rights reserved.
PostMate is licensed under a proprietary license. You are free to use it, but you may not redistribute, modify, or sell it without explicit permission.

Third-Party Libraries: PostMate uses the following open-source packages:

chai, mocha, node-fetch, jsonpath-plus, monaco-editor, uuid, esbuild, rimraf, typescript, vscode-test, @types/* packages

These libraries are used under their respective licenses (mostly MIT or Apache 2.0). Please refer to each library for full license details.


## Feedback

Please share feedback or feature requests via [GitHub Issues](https://github.com/shyyadav/mpostmate-docs/issues)
