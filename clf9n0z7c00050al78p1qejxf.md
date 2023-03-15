---
title: "Validate Your Environment Variables Easily with env-vars-validator"
datePublished: Wed Mar 15 2023 12:07:33 GMT+0000 (Coordinated Universal Time)
cuid: clf9n0z7c00050al78p1qejxf
slug: validate-your-environment-variables-easily-with-env-vars-validator
cover: https://cdn.hashnode.com/res/hashnode/image/upload/v1678881998350/9cbdd40b-6f5f-4a34-b22b-e69db8e96a12.png
tags: variables, javascript, nodejs, typescript, environment-variables

---

As a developer, you know that working with environment variables is a fundamental aspect of building applications. However, validating them can be a bit tricky. This is where `env-vars-validator` comes into play.

`env-vars-validator` is a TypeScript library that enables you to validate your environment variables easily. It's available on [GitHub](https://github.com/qlaffont/env-vars-validator) and on [NPM](https://www.npmjs.com/package/env-vars-validator).

## Installation

You can install `env-vars-validator` with NPM using the following command:

```bash
npm install env-vars-validator
pnpm install env-vars-validator
yarn install env-vars-validator
```

## Usage

Using `env-vars-validator` is simple. First, import the `validateEnv` function from the library:

```typescript
const { validateEnv } = require("env-vars-validator");
```

Then, you can use it to validate your environment variables from an AJV schema:

```typescript
validateEnv(
  {
    NODE_ENV: { type: 'string' },
    PORT: { type: 'integer' },
  },
  {
    requiredProperties: ['NODE_ENV'],
  },
);
```

This example validates that `NODE_ENV` is a string and that `PORT` is an integer. Additionally, it requires that `NODE_ENV` is present in the environment variables.

## API

`env-vars-validator` provides several additional functions that can help you work with environment variables:

* `currentEnv()`: Returns the current `NODE_ENV` without spaces and in lowercase format.
    
* `isProductionEnv()`: Returns `true` if the current `NODE_ENV` is equal to `production`.
    
* `isPreProductionEnv()`: Returns `true` if the current `NODE_ENV` is equal to `production`.
    
* `isStagingEnv()`: Returns `true` if the current `NODE_ENV` is equal to `staging`.
    
* `isDevelopmentEnv()`: Returns `true` if the current `NODE_ENV` is equal to `development`.
    
* `isTestEnv()`: Returns `true` if the current `NODE_ENV` is equal to `test`.
    
* `isDeployedEnv()`: Returns `true` if the current `NODE_ENV` is **not** equal to `development` or `test`.
    

## Conclusion

`env-vars-validator` is a simple and powerful library that makes it easy to validate your environment variables. With its intuitive API and TypeScript support, it's a great choice for any project that needs to work with environment variables. Try it out today!