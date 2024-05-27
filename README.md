# Setup ESLINT and PRETTIER in React app
# Eslin + Prettier = Clean Code 

# Step 1 : 
create app with vite 
```
npm create vite 
```

# Step 2 : 
install eslint (installed by default in vite )
```
npm install eslint --save-dev
or 
yarn install eslint --save-dev
```

# Step 3 :
add to .eslintrc
```
"rules": {
    "react/react-in-jsx-scope": "off"
  }
```

# Step 4 :
If you are using jest , Add jest : True inside env : 
```
"env": {
    "browser": true,
    "es2021": true,
    "jest": true
  }
```

# Step 5 : 
npm install eslint-config-prettier eslint-plugin-prettier prettier --save-dev
or 
yarn add eslint-config-prettier eslint-plugin-prettier prettier --dev

then make changes in .eslintrc file:
 "extends": ["eslint:recommended", "plugin:react/recommended", "plugin:prettier/recommended"]

# Step 6 :
Create .prettierrc and paste the below code:
```
{
  "semi": true,
  "tabWidth": 2,
  "printWidth": 100,
  "singleQuote": true,
  "trailingComma": "none",
  "jsxBracketSameLine": true
}
```

# Step 7 :
Now, eslint and prettier is setup lets add the script to the package.json

```
"lint": "eslint .",
"lint:fix": "eslint --fix",
"format": "prettier --write './**/*.{js,jsx,ts,tsx,css,md,json}' --config ./.prettierrc"
```





- [@vitejs/plugin-react](https://github.com/vitejs/vite-plugin-react/blob/main/packages/plugin-react/README.md) uses [Babel](https://babeljs.io/) for Fast Refresh
- [@vitejs/plugin-react-swc](https://github.com/vitejs/vite-plugin-react-swc) uses [SWC](https://swc.rs/) for Fast Refresh
