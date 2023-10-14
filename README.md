# bluesky-chatbot-tutorial

## Quickstart

This requires Node.js 18 or above. Create a .env from the .env.template and fill it with your login information. Then run the following command to setup the developer environment:

```
npm install
```

All changes should be made in the index.ts which will then compile into a index.js which can be run
```
npx tsc
node index.js
```
## Complete install and run instructions
These are the steps I run initially in the Youtube Video. To setup a working project from scratch (assume you only have this README file) do the following:

1. Make sure you have Node 18 or above installed. If you don't install using
- https://nodejs.org/en 
- https://github.com/nvm-sh/nvm#installing-and-updating

2. Install a package.json config
```
npm init -y
```
3. Change the package.json config to run your script as a module by adding the following line
```
{
    "type":"module",
    ...
}
```

4. Then use npm to install the following packages
```
npm install dotenv @atproto/api && npm install typescript @types/node --save-dev
```

5. Create a tsconfig
```
npx tsc --init
```

6. Adjust the following values in the tsconfig.json
```
{
    ...
    "target": "esnext", 
    "module": "Nodenext",
    "moduleResolution": "nodenext", 
    ...
}
```
7. Create a .env with the following information set
```
BLUESKY_USERNAME=
BLUESKY_PASSWORD=
```

8. Create a index.ts which will contain the bsky agent code. To run this you must compile into a .js file which you can do by running `npx tsc`. Then you can run your file using node. This whole proccess looks like
```
npx tsc
node index.js
```