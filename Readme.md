## Create react-apps superfast (the official way)
```bash
gitf https://github.com/facebook/create-react-app/tree/master/packages/cra-template
mv cra-template my-react-app && cd my-react-app
cp -r template/* .
npm i react react-dom web-vitals #Note: react-scripts in not installed but you should have it installed globally, yikes!
rs-start # Alias for `react-scripts start`
```
