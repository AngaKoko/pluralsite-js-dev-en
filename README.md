# pluralsite-js-dev-en
Development Environment for Java Script

# Steps to set up environment

  - Add editor config file `.editorconfit`
  - Choose a package manage `npm` preferably
  - Add a `pakage.json` file. https://gist.github.com/coryhouse/29bd1029b623beb4c7f79b748dcba844
  - do `npm install` .  
  - Install node security chekc globally `npm insatall -g nsp` it is best to check package security on `npm start` to chekc for vonerability run `nsp check`
  
# Development Web Server
- create a package with name `buildSrcipts` and file `srcServer.js`
- install local tunel to share work in progress `npm install -g localtunnel`

To start server, run:
    
    node buildScripts/srcServer.js
    
Open new terminal and run local turnnel:

    lt --port 3000

# Authomation

update the `package.json` file to be able to run app with `npm start`

    "scripts": {
        "prestart": "node buildScripts/startMessage.js",
        "start": "npm-run-all --parallel open:src",
        "open:src": "node buildScripts/srcServer.js",
        "security-check": "nsp check",
        "share": "lt --port 3000"
    }

# Configure Babel
Create file `.babelrc`
add code: 

  {
    "presents":[
      "latest"
    ]
  }
