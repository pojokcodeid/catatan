# Setting jsconfig.json supaya auto import

- Seting 1 projek Express JS degnan CommontJS
```json
{
  "compilerOptions": {
    "module": "commonjs",
    "target": "es6",
    "allowSyntheticDefaultImports": true
  },
  "exclude": ["node_modules"],
  "include": ["**/*.js"]
}
```

- Setting 2 Express JS ES6 Module

```json
{
  "compilerOptions": {
    "module": "es6",
    "target": "es6",
    "moduleResolution": "node",
    "baseUrl": "src",
    "paths": {
      "*": ["node_modules/*"]
    }
  },
  "include": ["src"]
}
```
```json
{
  "compilerOptions": {
    "target": "es6",
    "module": "es6",
    "allowSyntheticDefaultImports": true,
    "esModuleInterop": true,
    "moduleResolution": "node"
  },
  "include": ["src/**/*"]
}
```

- Setting Reat JS

```json
{
  "compilerOptions": {
    "baseUrl": ".",
    "paths": {
      "./": ["src"]
    }
  },
  "include": ["src"]
}
```
