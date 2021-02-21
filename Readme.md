## Create react-apps superfast (the official way)
```bash
gitf https://github.com/facebook/create-react-app/tree/master/packages/cra-template
mv cra-template my-react-app && cd my-react-app
cp -r template/* .
npm i react react-dom web-vitals #Note: react-scripts in not installed but you should have it installed globally, yikes!
rs-start # Alias for `react-scripts start`
```
This is tested! (You need to press y when `react-scripts start` executes so as to create default configs in package.json file, yikes!

Optionally you may use already defined alias i.e., cra (alias for `npx create-react-app`) to create react app, but that installs react-scripts for no desirable reason for every project created.

Thanks.
