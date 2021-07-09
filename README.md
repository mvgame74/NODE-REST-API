# NODE-REST-API

## Installation

1. We start by initialising Node.js : > npm init
2. We also initialise the libraries we are going to be using: > yarn add express mongoose dotenv helmet morgan nodemon
This references to the following websites for reference:

3. We start building our required librariesa in the index.js with:

```
const express = require('express');
const app = express();
const mongoose = require('mongoose');
const dotenv = require('dotenv');
const helmet = require('helmet');
const morgan = require('morgan');

dotenv.config();

mongoose.connect(process.env.MONGO_URL, {useNewUrlParser: true},()=>{
  console.log('Connected to MondoDB')
});

app.listen(8800,() => {
  console.log('Backend server is running!')
})
```

and our .env with the routing for our database:

```
MONGO_URL = mongodb+srv://mvgame:Boadicea74@cluster0.iouf5.mongodb.net/lama?retryWrites=true&w=majority
```

4. We can now initialise our server & connections with **yarn start** and it will give us the message that both ser ver is running and DB is connected.
