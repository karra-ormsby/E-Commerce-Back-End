# E-Commerce-Back-End

## Description

Given some starter code, I have build the back end for an e-commerce site. With the code I have written, and apps like Insomnia, you can view the models for Categories, Products, and Tags, and view they way they tie into each other and interact with each other. All three models have a GET, POST, PUT, and DELETE route.

## Table of Contents

  - [Installation](#installation)
  - [Usage](#usage)
  - [Credits](#credits)

## Installation

This application uses node.js to run. Please make sure you have it installed before trying to run the application. You can find a link to node.js [here](https://nodejs.org/en).

This application uses npm packages Express.js for running the server, mysql2 for running the database queries, Sequelize to interact with the MySQL database, and dotenv to be able to use a .env file to keep mysql login data safe. All of these packages have already been loaded into the dependencies of the package.json file.

As this application is using dotenv to use a .env file for Sequelize login data, you will needs to create your own file and populate it with your own information. It should have the format:

The application comes with a source.sql file to create the database. You will need to have mysql running on your computer and run the following commands in the terminal:
1. "mysql -u root" to open mysql (if you have a password on your mysql you will need to run the command "mysql -u root -p" instead and then input your password when prompted).
2. "source db/schema.sql;" to create the database and tables associated with it.

To run the application:
1. Right click the server.js file and click 'open in integrated terminal' or if you code editor does not have this function then you can use your terminal and make sure you are giving it the right file path.
2. Type "npm install" into the terminal to load in the npm packages.
3. Type "npm run seed" to seed the database with the test data.
4. Type "node server.js" to start the application.

## Usage

Once you have opened up the terminal to the path corresponding to the application (see installation section for how to do this), type "node server.js" and press enter to run the application. You will get a message saying 'Now listening', which will tell you that the express server is running.

You can now go into an app like Insomnia and test out the routes.

The available routes are:
- GET http://localhost:3001/api/categories. The output will look something like this: 

![GET categopries](./assets/images/GET%20categories.png)

- GET http://localhost:3001/api/categories/id, where id is a category id. If the id given does not exist you will receive the message: 'No category found with this id!'. The output will look something like this:

![GET categories by id](./assets/images/Get%20caterogies%20by%20id.png)

- POST http://localhost:3001/api/categories, where req.body should look like this...

    {

      "category_name": "Clothing"

    }

    The output will look something like this: 

![POST categories](./assets/images/POST%20categories.png)

- PUT http://localhost:3001/api/categories/id, where id is a category id, and req.body should look like this...

    {

      "category_name": "Clothing"

    }

    If the id given does not exist you will receive the message: 'No category found with this id!'. The output will look something like this: 

![PUT categories](./assets/images/PUT%20categories.png)

- DELETE http://localhost:3001/api/categories/id. The output will look something like this: 

![DELETE categories](./assets/images/DELETE%20categories.png)

- GET http://localhost:3001/api/products. The output will look something like this: 

![GET products](./assets/images/GET%20products.png)

- GET http://localhost:3001/api/products/id, where id is a product id. If the id given does not exist you will receive the message: 'No product found with this id!'. The output will look something like this: 

![GET products by id](./assets/images/GET%20products%20by%20id.png)

- POST http://localhost:3001/api/products, where req.body should look like this...

    {

      "product_name": "Basketball Shoes",
      "price": 200.00,
      "stock": 3,
      "category_id": 5,
      "tagIds": [1, 2, 3, 4]

    }

    The output will look something like this: 

![POST products](./assets/images/POST%20products.png)

- PUT http://localhost:3001/api/products/id, where id is a product id, and req.body should look like this...

    {

      "product_name": "Basketball Shoes",
      "price": 200.00,
      "stock": 3,
      "category_id": 5,
      "tagIds": [1, 2, 3, 4]

    }

    If the id given does not exist you will receive the message: 'No product found with this id!'. The output will look something like this: 

![PUT products](./assets/images/PUT%20products.png)

- DELETE http://localhost:3001/api/products/id. The output will look something like this: 

![DELETE products](./assets/images/DELETE%20products.png)


- GET http://localhost:3001/api/tags. The output will look something like this: 

![GET tags](./assets/images/GET%20tags.png)

- GET http://localhost:3001/api/tags/id, where id is a tag id. If the id given does not exist you will receive the message: 'No tag found with this id!'. The output will look something like this: 

![GET tags by id](./assets/images/GET%20tags%20by%20id.png)

- POST http://localhost:3001/api/tags, where req.body should look like this...

    {

    "tag_name": "clothing",
    "productIds": [1, 2, 3, 5]

    }

  The output will look something like this: 

![POST tags](./assets/images/POST%20tags.png)

- PUT http://localhost:3001/api/tags/id, where id is a tag id, and req.body should look like this...

    {

    "tag_name": "clothing",
    "productIds": [1, 2, 3, 5]

    }

    If the id given does not exist you will receive the message: 'No tag found with this id!'. The output will look something like this: 

![PUT tags](./assets/images/PUT%20tags.png)

- DELETE http://localhost:3001/api/tags/id. The output will look something like this: 

![DELETE tags](./assets/images/DELETE%20tags.png)

A video of the usage of this application can be found [here](https://drive.google.com/file/d/1d0DCmTRjugbruZ17-JOizY2X1TAPdCgM/view).


## Credits

Starter code provided by Monash Bootcamp : https://git.bootcampcontent.com/Monash-University/MONU-VIRT-FSF-PT-02-2023-U-LOLC/-/tree/main/Week-13/02-Challenge

