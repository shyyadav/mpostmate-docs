# Postmate Client

**Postmate Client** is a lightweight yet powerful API testing client built natively into **Visual Studio Code**.  
It is designed for developers and QA engineers who want fast, scriptable, and repeatable API testing without leaving their editor.

📘 **Documentation:** https://postmatelab.com/

## 🏁 Quick Start

1. Click the **Postmate Client** icon in VS Code Activity Bar.
2. Click **New Request** to create your first API request.
3. Save requests to collections/folders.
4. Use `{{variable}}` to reference environment or response variables.


## ✨ Key Features

### 🔧 Built-in `pm` Library
Postmate includes a rich scripting and assertion library, similar to Postman, exposed via the global `pm` object:

```js
pm.assert
pm.clearVariable
pm.expect
pm.getRequest
pm.getVariable
pm.listVariables
pm.log
pm.setVariable
pm.test
pm.schemaTest("Validate response schema", userSchema, sampleData)
pm.base64Decode(accessToken)
```
## 🚀 Request Creation & Import
- Import real-world cURL commands instantly [Watch Demo Video](https://www.youtube.com/watch?v=K0TjOP-nPZM)
- Import APIs from Swagger / OpenAPI
- Import collections from Postman
- Save and organize requests into collections and folders

## 🧪 Testing & Automation
- Pre-request and post-request scripting
- Plain-English style assertions (no scripting required for common cases)
- JavaScript-based response manipulation
- Extract values from responses and store them as variables
- Request chaining across multiple APIs
- Collection runner with execution results

## 📊 Data-Driven Testing
- Manage multiple Data Tables
- Select data rows dynamically while sending requests
- Attach data tables to environments
- Parameterize requests using `{{variable}}` syntax

## 🌍 Environment & Variables
- Multiple environments supported
- Dynamic variables across requests
- Environment-level data tables
- Request history & persistence

## ⚙️ User Settings
- Log as cURL – log outgoing requests as a cURL command instead of plain text

## ⚡ Native VS Code Experience
- Fast and lightweight
- No external runtime required
- Seamless VS Code UI integration

## 📸 Screenshots
![Postmate Overview](https://raw.githubusercontent.com/shyyadav/mpostmate-docs/main/images/Overview%20gif%20file.gif)

Enjoy the speed, simplicity, and power of a native extension
![Demo Screenshot](https://raw.githubusercontent.com/shyyadav/mpostmate-docs/main/images/img.PNG)

![Demo Screenshot](https://raw.githubusercontent.com/shyyadav/mpostmate-docs/main/images/pre-request.png)

Supports multiple Data Tables for use across requests and collections.
![Demo Screenshot](https://raw.githubusercontent.com/shyyadav/mpostmate-docs/main/images/datatable.PNG)

## Test / Assertion: 
Postmate Client provides both scripting as well as writing test just in plain English for most obvious types of assertions.

**_Writing tests just like plain English:_** go to Tests tab and click on Test sub tab.  
You can have tests in tabular form where **_every row is a test_**. Test rows have 5 columns Test Types, Action, Expected, Test Description and a delete icon at last.

**_Test Type:_**

 1. **Set Env Variable:** in case you want some data from the response to be stored in environment variable to use later or next request

 _**Tip:** just run your request once before you start writing test, so that you’ll get json path in suggestion to select._
 ![json path helper](https://github.com/shyyadav/mpostmate-docs/blob/main/images/jsonPathHelper.PNG?raw=true)
***Example use case:*** you want to store authorization-token in variable so that you can use it another request.
![test type1](https://github.com/shyyadav/mpostmate-docs/blob/main/images/testType1.PNG?raw=true)

## Write JavaScript code to manipulate API responses.
- Response body (RESPONSE.body)
- Response status (RESPONSE.status)
- Example:
```const resp = RESPONSE.body;
   const students = resp.students;
   students.forEach(s =>{
      console.log(s.name);
   });
```
![Demo Screenshot](https://raw.githubusercontent.com/shyyadav/mpostmate-docs/main/images/Test.png)

Collection Run:
![Demo Screenshot](https://raw.githubusercontent.com/shyyadav/mpostmate-docs/main/images/collectionRunner.PNG)

## Licensing & Dependencies
Copyright: © 2025 Shyam Narayan Yadav. All rights reserved.
Postmate Client is licensed under a proprietary license. You are free to use it, but you may not redistribute, modify, or sell it without explicit permission.

Third-Party Libraries: Postmate Client uses the following open-source packages:

chai, mocha, node-fetch, jsonpath-plus, monaco-editor, uuid, esbuild, rimraf, typescript, vscode-test, @types/* packages

These libraries are used under their respective licenses (mostly MIT or Apache 2.0). Please refer to each library for full license details.

## Feedback
Please share feedback or feature requests via [GitHub Issues](https://github.com/shyyadav/mpostmate-docs/issues)
