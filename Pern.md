https://www.youtube.com/watch?v=_zGL_MU29zs

## Uso
PostgreSQL
Expressjs
React
Nodejs

## Setup

`npm init -y` 
inicializa nodejs

`npm i express morgan cors`
express: servidor con nodejs
morgan: mostrar por consola las peticiones 
cors: comunicar dos servidores con dominios distintos (conectar el front con el back)

`npm i nodemon -D`
Esto nos servira para no tener que reiniciar el servidor con cada cambio mientras desarrollamos

creamos src/index.js y src/config.js y db.js
src/routes/tasks.routes.js (como haremos una app de tasks ese sera el titulo)
src/controllers/tasks.controllers.js (funciones)

codigo prueba index (listar ruta en script)
```javascript
const express = require('express');
const app = express();

app.listen(3000)
console.log('Server running on port 3000')
```

añadir script de start para poder arrancar index
```javascript
"scripts":{
	"start": "node src/index.js",
	"dev": "nodemon src/index.js"
}```

Ejecutaremos `npm start` y nos fijaremos de que la consola devuelva el log que escribimos si buscamos en  el navegador localhost:3000 nos devolvera un error de  `Cannot GET /` ya que no tenemos nada de frontend en nuestro archivo index 

Con el comando `npm run dev` vamos a poder evitarnos tener que detener la instancia de node y ejecutarla denuevo para ver los cambios, cada vez que hagamos cambios estos se veran reflejados inmediatamente.

## ENDPOINTS

definiremos las rutas en  src/tasks.routes.js
```Javascript
const { Router } = require('express');
const router = Router();

router.get('/', (req, res) => {
	res.send('Hello World')
})

module.exports = router;
```

importamos tasks.routes en index con
```javascript
const taskRoutes = require('./routes/tasks.routes');

app.use(taskRoutes)
```

una vez visitando la pagina veremos como el mensaje estara ahi y la ruta ya estara lista.

toca añadir los otros endpoints basandonos en lo que hicimos en taskRoutes

```Javascript
const { Router } = require('express');
const router = Router();

router.get('/tasks', (req, res) => {
	res.send('retrieving a list of tasks');
})

router.get('/tasks/10', (req, res) => {
	res.send('retrieving a single task');
})

router.post('/tasks', (req, res) => {
	res.send('creating tasks');
})

router.delete('/tasks', (req, res) => {
	res.send('deleting a task');
})

router.put('/tasks', (req, res) => {
	res.send('updating a task');
})
module.exports = router;
```

## Conectando a postgress