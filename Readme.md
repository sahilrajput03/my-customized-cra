## Create react-apps superfast (the official way)

```bash
gitf https://github.com/facebook/create-react-app/tree/master/packages/cra-template
mv cra-template my-react-app && cd my-react-app
cp -r template/* .
rm -rf template
yarn add react react-dom web-vitals #Note: react-scripts in not installed but you should have it installed globally, yikes!
rs-start # Alias for `react-scripts start`
```

This is well tested and you need to press y when `react-scripts start` executes so as to create default configs in package.json file, yikes!

Optionally you may use already defined alias i.e., `cra` (alias for `npx create-react-app`) to create react app(e.g., `cra my-react-app`), but that installs react-scripts for no desirable reason for every project created.

## Create react-typescript-app (the official way)

```bash
gitf https://github.com/facebook/create-react-app/tree/master/packages/cra-template-typescript
mv cra-template-typescript my-react-typescript-app && cd my-react-typescript-app
cp -r template/* .
rm -rf template
yarn add react react-dom web-vitals #Note: react-scripts in not installed but you should have it installed globally, yikes!
yarn add -D typescript @types/react @types/react-dom
echo "declare module \"*.svg\" {
  const content: any;
  export default content;
}" > src/custom.d.ts
rs-start # Alias for `react-scripts start`
```

Thanks.
