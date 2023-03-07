# Express Setup

`npm init -y` 
Este comando  crea un package.json para listar las dependencias

npm install express mysql2 morgan
esto instala servers

npm i nodemon -D

crear un index.js dentro de server y luego usar node {ruta} para verificar que ande

agregar "dev": "nodemon server/index.js" en package.json para poder actualizar el server automaticamente

añadir la propiedad "type": "module", bajo main para poder importar modulos


```javascript
// /server/index.js
import express from 'express';

const app = express()

app.listen(3000)
console.log('Server is running on port 3000')
```
se hace para revisar que todo ande como corresponde

```javascript
// /server/config.js
export const PORT = 3000;
```
definimos el puerto en otro archivo, para luego poder tener todas nuestras configuraciones separadas del servidor (Es recomendar cambiar de puerto para que al crear el archivo de react este no moleste ya que su puerto por defecto es el 3000)

cambiamos nuestro index a 
```javascript
// /server/index.js
import express from 'express';
import { PORT } from './config.js'

const app = express()

app.listen(PORT)
console.log(`Server is running on port ${PORT}`);
```
# MYSQL Setup