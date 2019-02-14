
Setup ESLint with Airbnb JavaScript Style Guide
======

 This sets up eslint for one project
 --
1. Install eslint extension in vs-code/webstorm

2. install our dev deps (you could also use yarn)

    ```
    npm i eslint@latest eslint-config-airbnb@latest eslint-plugin-import@latest eslint-plugin-jsx-a11y@latest eslint-plugin-react@latest babel-eslint@latest -d
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
    ],
    "parserOptions": {
		"ecmaVersion": 2017,
		"sourceType": "module",
		"ecmaFeatures": {
			"experimentalObjectRestSpread": true,
			"impliedStrict": true,
			"globalReturn": false,
			"jsx": true
		}
	},
   "parser": "babel-eslint"
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
    npm i eslint@latest eslint-config-airbnb@latest eslint-plugin-import@latest eslint-plugin-jsx-a11y@latest eslint-plugin-react@latest babel-eslint@latest -g
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
    ],
    "parserOptions": {
		"ecmaVersion": 2017,
		"sourceType": "module",
		"ecmaFeatures": {
			"experimentalObjectRestSpread": true,
			"impliedStrict": true,
			"globalReturn": false,
			"jsx": true
		}
	},
   "parser": "babel-eslint"
   /* "rules": {
        "max-len":"off",
        "func-names": ["error", "never"]
    }*/
    }
    ```
You can run ESLint on any file or directory like this:
   
   ```
   eslint yourfile.js
   ```
   
[Airbnb JavaScript Style Guide](https://github.com/airbnb/javascript "Airbnb JavaScript Style Guide")