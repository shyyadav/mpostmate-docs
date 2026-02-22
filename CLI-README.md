# 🚀 Postmate CLI

Run Postmate API collections directly from your terminal.

Postmate CLI enables environment-based execution, data-driven testing, JSON reporting, and CI/CD-ready exit codes — all without a GUI.

---

## 📦 Installation

Install globally using npm:

```js
npm install -g @postmate/cli
```
Verify installation:
```js 
pmc --version
```
📁 Project Structure

Postmate CLI works inside a project that contains a .postmate directory.

Example:
```js
my-project/
│
├── .postmate/
│   ├── collections/
│   ├── environments/
│   ├── data/
│   └── reports/
│
└── package.json
```
You can run the CLI from:
- Inside .postmate
- Or from the project root

The CLI automatically detects the correct project folder.

▶️ Running a Collection

Basic usage:
```js
pmc run --collection <collectionName> --env <environmentName>
```
Example:
```js
pmc run --collection school --env Dev --data Prod_data --report myreport 
pmc run -c school -e Dev -d Prod_data -r myreport 
pmc run --report myreport --collection school --env Dev --data Prod_data 
pmc run -r myreport --collection school --env Dev --data Prod_data 
pmc run --collection school --env Dev
```
Each row in the data file will execute the collection once.

Variables like:
```js
{{id}}
{{username}}
```
will resolve per row.

🧪 Execution Output

Example terminal output:
```js
🚀 Running school
Env: Dev
Iterations: 1
Total Requests: 10

✔ [1] Get Users (200)
✖ [1] Create User (500)

Finished in 3s 120ms
Total Requests: 10
Report saved: .postmate/reports/school-Dev-2026-02-14T15-32-10.json
```
📄 Reports

After every run, a JSON report is automatically generated inside:
```js
.postmate/reports/
```
Filename format:
```js
<collection>-<environment>-<timestamp>.json
```
Example:
```js
school-Dev-2026-02-14T15-32-10.json
```
Reports can be:
- Stored as CI artifacts
- Parsed for analytics
- Converted to JUnit
- Used for dashboards

❌ Exit Codes (CI Ready)
Postmate CLI returns:
- 0 → All requests successful (HTTP 2xx)
- 1 → One or more failures

Example:
```js
pmc run --collection school --env Dev
echo $?
```
This makes it ready for CI/CD pipelines.

⚙️ Command Reference
Run Command
```js
pmc run --collection <name> --env <envName> [--data <dataFile>]
```
Options
```js
| Option         | Description                      |
| -------------- | -------------------------------- |
| `--collection` | Collection name                  |
| `--env`        | Environment name                 |
| `--data`       | Optional data file for iteration |
```
🏗 CI Example (GitHub Actions)
```js
- name: Run API Tests
  run: pmc run --collection school --env QA
```
If any request fails, the pipeline fails automatically.

💡 Best Practices
- Keep base URLs inside environment files
- Use data files for bulk execution
- Version control your .postmate directory
- Store reports as CI artifacts
- Use clear environment names (Dev, QA, Prod)

🔥 Why Postmate CLI?
- Lightweight
- Deterministic
- Scriptable
- CI-friendly
- No GUI required
- Built for automation

📜 License

ISC

Made with ❤️ using Postmate
