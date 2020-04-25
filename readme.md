## Primeiro projeto node
```
yarn init -y
yarn add express
yarn add typescript -D
yarn tsc --init
yarn add @types/express -D
yarn add ts-node-dev -D
```
## Instalando extensão e plugins para padronizar projetos
* EditorConfig
  * Padroniza os projetos usados com editores diferentes. Ex: visual code, sublime, atom;

* Eslint
```
yarn add eslint -D
yarn eslint --init
```
add a extensão eslint

## settings.json
* Add as configurações abaixo para ajustar o código automaticamenta ao salvar

```
"[javascript]": {
        "editor.codeActionsOnSave": {
            "source.fixAll.eslint": true
        }
    },
    "[javascriptreact]": {
        "editor.codeActionsOnSave": {
            "source.fixAll.eslint": true
        }
    },
    "[typescript]": {
        "editor.codeActionsOnSave": {
            "source.fixAll.eslint": true
        }
    },
    "[typescriptreact]": {
        "editor.codeActionsOnSave": {
            "source.fixAll.eslint": true
        }
    },
```

## configurando import
```
yarn add -D eslint-import-resolver-typescript
// no .eslintrc.json
"rules": {
    "import/extensions": [
      "error",
      "ignorePackages",
      {
        "ts": "never"
      }
    ]
  },
  "settings": {
    "import/resolver": {
      "typescript":{}
    }
  }
```
## Adicionando Prettier
```
yarn add prettier eslint-config-prettier eslint-plugin-prettier -D
// no .eslintrc.json
"extends": [
      "plugin:@typescript-eslint/recommended",
      "prettier/@typescript-eslint",
      "plugin:prettier/recommended"
  ],
  "plugins": [
    "prettier"
  ],
  "rules": {
      "prettier/prettier": "error",
  }
```

## ID
```
yarn add uuidv4
```
## Lidar com data
```
yarn add date-fns
```

## Rota
Receber a requisição, chamar outro arquivo, devolver um resposta
