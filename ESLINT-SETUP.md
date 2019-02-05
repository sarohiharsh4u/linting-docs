
Setup ESLint with Airbnb JavaScript Style Guide
======

 This sets up eslint for one project
 --
1. Install eslint extension in vs-code/webstorm

2. install our dev deps (you could also use yarn)

    ```
    npm i eslint eslint-config-airbnb eslint-plugin-import eslint-plugin-jsx-a11y eslint-plugin-react babel-eslint -d
    ```
3. Create eslint file
   ```
   touch .eslintrc
   ```
4. Add  config

    ```js

    {
    "extends": "airbnb",
    "plugins": [
        "react"
    ]
   /* "rules": {
        "max-len":"off",
        "func-names": ["error", "never"]
    }*/
    }
    ```




 This sets up eslint globally
 --
1. Install eslint extension in vs-code/webstorm

2. install deps globally

    ```
    npm i eslint eslint-config-airbnb eslint-plugin-import eslint-plugin-jsx-a11y eslint-plugin-react babel-eslint -g
    ```
3. Create eslint file in `<your name>$`
   ```
   touch .eslintrc
   ```
4. Add config

    ```js

    {
    "extends": "airbnb",
    "plugins": [
        "react"
    ]
   /* "rules": {
        "max-len":"off",
        "func-names": ["error", "never"]
    }*/
    }
    ```

[Airbnb JavaScript Style Guide](https://github.com/airbnb/javascript "Airbnb JavaScript Style Guide")