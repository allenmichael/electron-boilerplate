Electron application template (using Webpack + TypeScript + React + VisualStudio Code)

This is a bare-bones template, which only includes the essential elements.

Modified from [this](https://github.com/electron/electron-quick-start)

Clone the repository, cd into the directory and type the following 

```
npm install
npm link typescript #This assumes that typescript is installed globally on your system
npm run build
code .
```

This will start a VisualStudio Code instance. From  VSCode you can then hit F5 to start a debugging session

## Build system description

The TypeScript compiler manages the build of the `main.ts` and `render.ts` files, which represent the Electron-specific parts of the application. The resulting `js` files are created in the toplevel directory of the project, but are not tracked by git.

Conversely webpack uses the `index.tsx` file in the `app` directory as entry point to bundle all the React code into a single `bundle.js` file in the `dist` folder.

When Electron starts the `bundle.js` file is loaded in `index.html`



