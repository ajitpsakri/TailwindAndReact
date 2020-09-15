1. create-react-app <app name>
---
2. yarn add tailwindcss postcss-cli autoprefixer -D
---
3. npx tailwind init --full
---
4. touch postcss.config.js
---
5. In postcss.config.js add this code 

`module.exports = {
    plugins: [
        require('tailwindcss'),
        require('autoprefixer')
    ],
}`
---
6. create "style" folder in src folder and add "main.css" and "tailwind.css"
---
7. Add this code to "tailwind.css"
`@tailwind base;
@tailwind components;
@tailwind utilities;`
---
8. Add this code to package.json

 `"scripts": {
    "start": "npm run build:css && react-scripts start",
    "build": "npm run build:css && react-scripts build",
    "test": "react-scripts test",
    "eject": "react-scripts eject",
    "build:css" : "postcss src/styles/tailwind.css -o src/styles/main.css" 
  },`
---
9. yarn build:css   
---
10. when using tailwind css in a file "import main.css"



 # TailwindAndReact
