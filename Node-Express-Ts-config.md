# Instalación y configuracion de Node + Express + Ts
## En proyectos de Node y Express con TypeScript

1. inicializar el proyecto en Node:

```
npm init -y

```

2. crear el archivo de configuracion de Ts:

```
tsc --init

```

3. Hacer los cambios en el archivo __tsconfig.json__

```
 "target": "ES6", 
 "sourceMap": true,   
 "outDir": "./dist", 
 "moduleResolution": "node", 

```

4. intalar  typescipt de manera local y tslint

```
npm i typescript --save-dev
npm i tslint --save-dev

```

5. abrir un terminal de Git Bash y ejecutar el siguiente comando:


```
    ./node_modules/.bin/tslint --init
```


6. Configurar el archivo tslint.json:

```
{
 "defaultSeverity": "error",
 "extends": [
     "tslint:recommended"
 ],
 "jsRules": {},
 "rules": {
     "no-console": false
 },
 "rulesDirectory": []
}

```
7. intalar  express cors dotenv

```
npm i express cors dotenv

```

8. intalar  los types/express

```
npm i --save-dev @types/express

```

9. Ejemplo Basico de inicio


```
import express from 'express';

const app = express();
const port = process.env.PORT || 8080;

app.get('/', (req, res) => {
  res.send('Hello World!');
});

app.listen(port, () => {
  console.log(`Server listening on port ${port}`);
});


```

10. Ejecutar los siguientes comando en 2 consolas diferentes:

```
tsc --watch

nodemon dist/app.js

```

listo....!