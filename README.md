## 1. PHPStorm
#### Auto check convention for PHP follow PSR-12
##### Install phpcs
`composer global require "squizlabs/php_codesniffer=*"`

##### config in PHPstorm
`File > Setting > Languages & Frameworks > PHP > Quality Tools > PHP_CodeSniffer > click '...' > path to phpcs (default /home/{user}/.config/composer/vendor/bin/phpcs) > Apply > Ok`

`File > Setting > Inspections >PHP > Quality Tools > PHP_CodeSniffer validation > click 'reload' in label 'Coding Standard' > select 'PSR12' > Apply > Ok`


#### Auto check convention for Javascript follow Standardjs
##### Install packages in project
`npm install babel-eslint eslint eslint-plugin-import eslint-plugin-node eslint-plugin-promise eslint-plugin-standard eslint-plugin-vue@next standard`
##### Copy file [.eslintrc.json](https://github.com/pham-van-huy/config-editor/blob/master/.eslintrc.json ".eslintrc.json") to root your project

##### Config in phpstorm
`File > Setting > Languages & Frameworks > Javascript > Code Quality Tools > ESLint > Node interpreter: path to node intall run 'which node' to get path > ESLint package: path to project/node_modules/eslint > Configuration file: path to project/.eslintrc.json > Apply > OK`

## 2. Sublime text
#### Auto check convention for PHP follow PSR-12
#####  Install phpcs
`composer global require "squizlabs/php_codesniffer=*"`
##### Config in Sublime text
Install package 'phpcs' refer in https://docs.cs.cf.ac.uk/notes/sublime-text-packages/
##### Config phpcs package
`Preferences>Package setting>PHP code sniffer>Settings-user> pass content under`
```json
{
    "phpcs_executable_path": "/home/{user}/.config/composer/vendor/bin/phpcs",
    "phpcs_additional_args": {
        "--standard": "PSR12",
        "-n": ""
    },
}
```

#### Auto check convention for Javascript follow Standardjs
#####  Install packages in project
`npm install babel-eslint eslint eslint-plugin-import eslint-plugin-node eslint-plugin-promise eslint-plugin-standard eslint-plugin-vue@next standard`
#####  Install package of Sublime text 3
`Ctrl + Shift + p > Package Control: Install Package > ESLint`
##### Copy file [.eslintrc.json](https://github.com/pham-van-huy/config-editor/blob/master/.eslintrc.json ".eslintrc.json") to root your project
##### Setting package eslint of Sublime text 3
`Preferences > Package Settings > ESLint > Settings - User > Pass content under`
```json
{
  "node_path": "/usr/local/bin", // run 'which node' to get path
  "node_modules_path": "path to project/node_modules",
  "config_file": "path to project/.eslintrc.js"
}
```
Key press Ctrl + Alt + e to check current file open
## 3. Visual code
#### Auto check convention for PHP follow PSR-12
##### Install squizlabs/php_codesniffer
`composer global require squizlabs/php_codesniffer`
##### Install extention phpcs for VS
##### Setting config extention phpcs
 `Executable Path: /home/{user}/.config/composer/vendor/bin/phpcs //path to phpcs`
 `Standard: edit in settings.json > "phpcs.standard": "PSR12"`
 => restart visual code

#### Auto check convention for Javascript follow Standardjs
##### Install packages in project
`npm install babel-eslint eslint eslint-plugin-import eslint-plugin-node eslint-plugin-promise eslint-plugin-standard eslint-plugin-vue@next standard`
##### Copy file [.eslintrc.json](https://github.com/pham-van-huy/config-editor/blob/master/.eslintrc.json ".eslintrc.json") to root your project

#####  Install extention eslint in Visual code
##### Setting extention eslint
Eslint: Node path > Edit in settings file > add to property under to file settings.js
```json
{
  ...
  "eslint.nodePath": "/home/{user}/.nvm/versions/node/v12.18.2/bin/node",
  "eslint.validate": [
      "javascript"
  ]
  ...
}
```

=> restart VS
