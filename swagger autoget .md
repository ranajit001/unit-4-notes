```javascript

1  npm install swagger-autogen 
2  npm install swagger-ui-express

3  then create swagger.js file and inside src

4
import swaggerAutogen from 'swagger-autogen';

const doc = {
    info: {
        title: 'My API',
        description: 'API Documentation for src1',
    },
    host: 'localhost:8080',  // Your host URL, adjust as needed
    schemes: ['http'],
};

const outputFile = './swagger.json';  // The generated swagger.json path
const endpointsFiles = ['./routes/*.js'];  // Path to your route files

// Initialize swaggerAutogen and generate the documentation
const swaggerGenerator = swaggerAutogen();
swaggerGenerator(outputFile, endpointsFiles);



5  node swagger.js   => swagger.json file created

6  inside swagger.json chege the port to app port.


7 inside app.js at vey bottom but top of app.listne() PAste:

import swaggerUi from 'swagger-ui-express';
import fs from 'fs';
const swaggerDocument = JSON.parse(fs.readFileSync('./swagger.json', 'utf8'));  //corrct the path
app.use('/api-docs', swaggerUi.serve, swaggerUi.setup(swaggerDocument));



7 inside swagger.json file chege the port to app port


// const endpointsFiles = [
//     './routes/user.route.js',
//     './routes/todo.route.js', 
//     './routes/reward.route.js'
// ];
// localhost:8080
// /user
// /todo
// /reward
// /api-docs
```