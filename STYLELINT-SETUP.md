
Setup Stylelint with Airbnb CSS / Sass Style Guide
======

 This sets up stylelint for one project
 --
1. Install stylelint extension in vs-code/webstorm

2. install dev deps (you could also use yarn)

    ```
    npm i stylelint stylelint-config-airbnb stylelint-order stylelint-scss -d
    ```
3. Create stylelint file
   ```
   touch .stylelintrc
   ```
4. Add  config

    ```js

    {
     "extends": "stylelint-config-airbnb",
     "rules": {}
    }
    ```




 This sets up stylelint globally
 --
1. Install stylelint extension in vs-code/webstorm

2. install deps globally

    ```
    npm i stylelint stylelint-config-airbnb stylelint-order stylelint-scss -g
    ```
3. Create stylelint file in `<your name>$`
   ```
   touch .stylelintrc
   ```
4. Add config

    ```js

    {
     "extends": "stylelint-config-airbnb",
     "rules": {}
    }
    ```

 
You can run StyleLint on any file or directory like this:
   
   ```
   stylelint yourfile.css
   ```

[Airbnb CSS / Sass Style Guide](https://github.com/airbnb/css "Airbnb CSS / Sass Style Guide")

