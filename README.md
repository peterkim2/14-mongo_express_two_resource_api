# Two Resource API Using MongoDB and Express

This project creates a two resource REST API using [Express.js](http://expressjs.com/) and [MongoDB](https://docs.mongodb.com/) that allows users send POST, GET, PUT and DELETE requests related
to dogs through the terminal.
When sending requests, use filepath `/api/size` or `/api/dog` with a query or parameters and a response will return with appropriate message/content.
You will need to [HTTPie](https://httpie.org/) to send requests through the terminal.

## How to run

Install any Dependencies from the `package.json` file into the project root
directory. Using [Node.js](https://nodejs.org/), to create a `package.json` file, enter command `npm init` in the project root.
You can run the command `npm i` to install all dependencies.

## Running server

Run the `server.js` file using command `node server.js` or `npm start`. In terminal, you should see `Server up: 8000` or
port that is set in your environmental variable in terminal.

## Sending POST GET PUT DELETE Request

>POST Request

>Size POST Request

In an new terminal window, send a `POST` request by using the command
`http POST localhost:8000/api/size name=<name>`.
Example: `http POST localhost:8000/api/size name='Large'`
The successful response should return a JSON object with values you entered along with a unique `id` and
a status code of `200`.

>Dog POST Request

In an new terminal window, send a `POST` request by using the command
`http POST localhost:8000/api/size/<sizeID>/dog name=<name> breed=<breed> color=<color>`.
Example: `http POST localhost:8000/api/size/5865db2fe19c9621196c0b7f/dog name='Buddy' breed='Golden Retriever' color='brown'`
The POST request must include the `sizeID`, as well as the `name` `breed` and `color` parameters.
The successful response should return a JSON object with values you entered along with a unique `id` and
a status code of `200`.

>GET Request

>Size GET Request

In an new terminal window, send a Size `GET` request by using the command `http localhost:8000/api/size/<sizeID>`.
Example: `http localhost:8000/api/size/5865db2fe19c9621196c0b7f`
The successful response should return a JSON object with a status of `200`.

>Dog GET Request

In an new terminal window, send a Dog `GET` request by using the command `http localhost:8000/api/dog/<dogID>`.
Example: `http localhost:8000/api/dog/5865db2fe19c9621196c0b7f`
The successful response should return a JSON object with a status of `200`.

![GET request screenshot](/assets/get-response-screenshot.png)

>PUT Request

>Size PUT Request

In an new terminal window, send a `PUT` request by using the command
`http PUT localhost:8000/api/size/<sizeID> name=<updateName>`.
Example: `http PUT localhost:8000/api/size/5865db2fe19c9621196c0b7f name='Medium'`
A successful response should return a `200` status code with a json object
with the updated content.

>Dog PUT Request

In an new terminal window, send a `PUT` request by using the command
`http PUT localhost:8000/api/dog/<dogID> name=<updateName>`.
Example: `http PUT localhost:8000/api/dog/5865db2fe19c9621196c0b7f name='Buster'`
A successful response should return a `200` status code with a json object
with the updated content.

>DELETE Request

>Size DELETE Request

In a new terminal window, send a `DELETE` request by using the command `http DELETE localhost:8000/api/size/<sizeID>`. A successful response should return a `204` status code and an empty body.

>Dog DELETE Request

In a new terminal window, send a `DELETE` request by using the command `http DELETE localhost:8000/api/dog/<dogID>`. A successful response should return a `204` status code and an empty body.

## Closing server

In server terminal, enter `control` + `c`.
