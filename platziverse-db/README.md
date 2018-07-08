# platziverse-db

## Usage

```js
const setupDatabase = require('platziverse-db')

setupDatabase(config).then(db => {
  const { Agent, Metric } = db

}).catch(err => console.error(err))
```

### Modules devDependencies

La belleza de JavaScript Standard Style es que es simple. Nadie quiere mantener múltiples archivos de configuración de estilo de cien líneas para cada *módulo / proyecto* en el que trabajan. ¡Suficiente de esta locura!, [standard](https://www.npmjs.com/package/standard).

`npm install standard --save-dev`
