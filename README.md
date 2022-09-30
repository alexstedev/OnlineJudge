# Online Judge
A web application for online judge(algorithm questions), built with MEAN stack (MongoDB, Express, Angular and Node.js).

<kbd>![image](/public/questions.png)</kbd>

<kbd>![image](/public/solution.png)</kbd>

# Function
This application is used to solve algorithm questions. You can submit the solution to see if it passes all test cases. Below are the available features.
* Token Based Authentication - Register, Login, Auto Login, User Profile, Reset Password, etc.
* User Management - Create, Update, Delete user.
* Question Management - Create, Update, Delete question.
* Database Management - Import and Export data with csv files for users, questions and submissions.
* Judging System - Judging Engine, Solution Template, Submission History, Multi-programming language support.
* Programming Languages - Three languages are currently supported, including Java, Javascript and Python.
* UI - RichTextEditor, Code Editor, Progress Bar, Loading Image are applied.

The following functions are under development.
* Contest - Generate contest by randomly selecting four questions from the question library.
* Collaborative code editor - Different users can work on the same solution simultaneously.

# Technology
The Server is built with Express and MongoDB. The used libraries for server are listed as follows.
* RESTful API: express, express router, mongoose, cors
* Logging: morgan, winston
* User Authentication: jsonwebtoken, passport, cookie-parser, express-jwt
* Import/Export Data: multer, csv-express, fast-csv

The Client is built with Angular and 3rd-party libraries, see below.
* CSS and Icon: bootstrap, font-awesome
* Rich Text Editor: ngx-quill
* Code Editor: ngx-monaco-editor
* Progress Bar: ngx-progressbar

# Setup Locally
## 1. Source Files
```bash
git clone https://github.com/alexstedev/OnlineJudge
cd OnlineJudge
npm install
npm run dev
```
Access http://localhost:9020/ in web browser, enjoy!

* If you run this on Windows, you need to install 'win-node-env' first. Otherwise, server will not get started and you will get 'NODE_ENV is not recognized' error, see [“NODE_ENV” is not recognized as an internal or external command, operable command or batch file](https://stackoverflow.com/questions/11928013/node-env-is-not-recognized-as-an-internal-or-external-command-operable-comman).
```bash
npm install -g win-node-env
```

## 2. Configuration
Notice, four different environments are configured for this app. Edit './server/config/server-config.js' to setup your site, especially the MongoDB connection url.

 Environment  | Command       | Description
--------------|---------------|-----------------------
local         | npm run local | Development environment using local MongoDB.
dev           | npm run dev   | Development environment using remote MongoDB hosted on mLab.
stage         | npm run stage | Testing environment using remote MongoDB hosted on mLab.
prod          | npm run prod  | Production environment for deployment.

## 3. Master Date
When the server is initially started, use admin user 'alexserrano' and password '111111' to login. Go to 'Database' to import data for 'users' and 'questions'. The data files are located in 'backup_csv' folder.
