 Full Stack Skeleton

Its a structure of a scalable typescript base `MERN Stack` project skeleton with user authentication.

## Table of Packages

| Client           | Server       |
| ---------------- | ------------ |
| Typescript       | Typescript   |
| React            | express      |
| Redux            | mongoose     |
| React-Redux      | cors         |
| Redux-toolkit    | morgan       |
| RTK-query        | dotenv       |
| Redux-persist    | helmet       |
| MUI              | bcrypt       |
| react-router-dom | jsonwebtoken |
| react-hook-form  | multer       |
| react-lottie     | cloudinary   |

## 1) Create a Directory

Create a directory and rename it with your project. Then initialize a git repository. Now Create a `.gitignore` file and fill with bellow code.
@@ -69,6 +87,14 @@ npx create-react-app . --template redux-typescript
rm -rf .git
```

## Install dependencies

`Redux-persist` for persist data on local storage,`MUI` design library,` react-router-dom` for routing,`react-hook-form ` for handel form data,` react-lottie` for animation.

```ch
yarn add redux-persist react-router-dom react-hook-form react-lottie
```

### 2B) Server setup

First initialize NPM then add scripts on `package.json` file.
@@ -89,4 +115,62 @@ Scripts
    },
```

Install dependencies `express` js for create api, `mongoose` for database operation, `cors` for cross application support, `morgan` form logging acton, `dotenv` for environment support, `helmet` for common attack protection, `bcrypt` for encrypting password, `jsonwebtoken` for verify user,
## Install dependencies

Install dependencies `express` js for create api, `mongoose` for database operation, `cors` for cross application support, `morgan` form logging acton, `dotenv` for environment support, `helmet` for common attack protection, `bcrypt` for encrypting password, `jsonwebtoken` for verify user, `multer` form file upload, `cloudinary` for image upload.

```ch
yarn add express mongoose cors morgan dotenv helmet bcrypt jsonwebtoken multer cloudinary
```

## Install dev-dependencies

install types for most packages. `typescript` form langrage support, `nodemon` for restart server, `ts-node` for compile .ts => .js

```ch
yarn add -D typescript nodemon ts-node @types/node @types/express @types/cors @types/morgan @types/dotenv @types/helmet @types/bcrypt @types/jsonwebtoken @types/multer
```

## Initialize typescript and active useful options on `tsconfig.json`

initialize tsc

```ch
npx tsc --init
```

Update `tsconfig.json`.

```ch
{
    "compilerOptions": {
        "target": "ESNext",
        "module": "commonjs",
        "rootDir": "./src",
        "moduleResolution": "node",
        "outDir": "./build",
        "esModuleInterop": true,
        "forceConsistentCasingInFileNames": true,
        "strict": true,
        "skipLibCheck": true
    }
}
```

### Create files and folders

Create `src` the root directory. `src/server.ts` end point.

-   Directories

```ch
mkdir src src/library src/middleware src/utility src/resources src/resources/auth src/resources/product
```

-   Files

```ch
touch .gitignore types.d.ts .env .env.example src/app.ts src/service.ts src/library/jwt.ts src/middleware/error.ts src/resources/ src/resources/auth/auth.model.ts src/resources/auth/auth.controller.ts src/resources/auth/auth.service.ts src/resources/product/product.model.ts src/resources/product/product.controller.ts src/resources/product/product.service.ts src/utility/responseGenerator.ts
```

## Edit server.ts and start your server with `yarn dev` command.
