# Full Stack Skeleton

## 1) Create a Directory

Create a directory and rename it with your project. Then initialize a git repository. Now Create a `.gitignore` file and fill with bellow code.

```ch
mkdir [my-project-name]
cd [my-project-name]
git init
touch .gitignore
```

`.gitignore` file content

```ch
# See https://help.github.com/articles/ignoring-files/ for more about ignoring files.

# dependencies
client/node_modules
server/node_modules
/.pnp
.pnp.js

# testing
/coverage

# production
client/build
server/build

# misc
.DS_Store
client/.env.local
server/.env
.env.development.local
.env.test.local
.env.production.local

client/npm-debug.log*
client/yarn-debug.log*
client/yarn-error.log*

server/npm-debug.log*
server/yarn-debug.log*
server/yarn-error.log*

```

## 2) Create 2 Directory.

-   ### Client
    -   Create react app
    -   Remove .git
-   ### Serer
    -   Initialize NPM
    -   Add scripts on `package.json`
    -   Install dependencies and dev dependencies
    -   Initialize typescript active useful options on `tsconfig.json`
    -   create files and folders

### 2A) Create react app and remove git.

enter client directory then create react app with redux toolkit and typescript template `--template redux-typescript`. Then remove `.git` from the directory with bellow code.

```ch
cd client
npx create-react-app . --template redux-typescript
rm -rf .git
```

### 2B) Server setup

First initialize NPM then add scripts on `package.json` file.

```ch
npm init -y
```

Scripts

```ch
   "scripts": {
        "start": "node build/server.js",
        "debug": "ndb build/server.js",
        "build": "tsc",
        "dev": "nodemon src/server.ts",
        "postinstall": "npm run build"
    },
```

Install dependencies `express` js for create api, `mongoose` for database operation, `cors` for cross application support, `morgan` form logging acton, `dotenv` for environment support, `helmet` for common attack protection, `bcrypt` for encrypting password, `jsonwebtoken` for verify user,
