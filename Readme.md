## Create react-apps superfast (the official way)

```bash
gitf https://github.com/facebook/create-react-app/tree/master/packages/cra-template
mv cra-template my-react-app && cd my-react-app
cp -r template/* .
rm template.json
rm -rf template
yarn add react react-dom web-vitals #Note: react-scripts in not installed but you should have it installed globally, yikes!
sed -i '2i\ \ "scripts": {\
    "start": "react-scripts start",\
    "test": "react-scripts test",\
    "build": "react-scripts run build",\
    "eject": "react-scripts run eject"\
  },' package.json
yarn start
```

This is well tested and you need to press y when `react-scripts start` executes so as to create default configs in package.json file, yikes!

Optionally you may use already defined alias i.e., `cra` (alias for `npx create-react-app`) to create react app(e.g., `cra my-react-app`), but that installs react-scripts for no desirable reason for every project created.

## Create react-typescript-app (the official way)

```bash
gitf https://github.com/facebook/create-react-app/tree/master/packages/cra-template-typescript
mv cra-template-typescript my-react-typescript-app && cd my-react-typescript-app
cp -r template/* .
rm -rf template
rm template.json
yarn add react react-dom web-vitals #Note: react-scripts in not installed but you should have it installed globally, yikes!
yarn add -D typescript @types/react @types/react-dom
echo "declare module \"*.svg\" {
  const content: any;
  export default content;
}" > src/custom.d.ts
sed -i '2i\ \ "scripts": {\
    "start": "react-scripts start",\
    "test": "react-scripts test",\
    "build": "react-scripts run build",\
    "eject": "react-scripts run eject"\
  },' package.json
yarn start
```

Refer other templates @ https://github.com/facebook/create-react-app/tree/master/packages

### For sublime it just works out of the box with original typescript package, yikes!!

https://packagecontrol.io/packages/TypeScript (If you don't find way to install it via package manager in sublime, install it directly via git cloning way as mentioned in its github repo).

Thanks.
