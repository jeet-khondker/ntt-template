# Mock Data Setup Installation Guideline

The purpose of this file is to document the workflow of setting up the mocked data. `json-server` will be used for setting up the mock data in the `project` Application.

Reference Guide : [JSON Server](https://github.com/typicode/json-server)

## JSON Server `json-server`

JSON is an acronym for `JavaScript Object Notation`. JSON Server is a lightweight and easy-to-use Node.js tool that simulates a RESTful API using a JSON file as the data source. With JSON Server, front-end developers can create mock APIs without the need to write complex server-side code, or when a backend API isn't ready yet.

This mock API sends requests to an endpoint that will be provided. It responds to HTTP requests, and this makes it ideal for rapid development for front-end developers. JSON Server also enables developers to perform CRUD (Create-Read-Update-Delete) operations and saves data in JSON files.

## Installation of JSON Server `json-server`

### 🔥 Pre-Requisites

Make Sure you have completed the workflow of the file `00_PRE-REQUISITES.md` inside `documentation` Directory. You need to have NodeJS and Yarn Package Manager installed. Read out the [documentation](../documentation/00_PRE-REQUISITES.md) for more details.

### Global Installation

Global Installation installs JSON Server globally on system so that it can be used from any directory.

#### Using NPM (Node Package Modules) Package Manager

```sh
npm install -g json-server
```

#### Using Yarn Package Manager

```sh
yarn global add json-server
```

### Project-Based Installation

Project-Based Installation installs JSON Server locally for just a particular project.

#### Using NPM (Node Package Modules) Package Manager

```sh
cd frontend
npm install json-server
```

#### Using Yarn Package Manager

```sh
cd frontend
yarn add json-server
```

## Database File Creation

Create a new database file `db.json` inside the `frontend` folder where `package.json` file is located.

## Data Creation

Define your data inside the JSON file. This JSON data can be an array of objects or an object with nested objects. Each object represents a data entity and should each have a unique id.

For Example : 

```json
{
    "database_table_one" : [
        {
            "id" : 1,
            "field_one" : "value_one",
            "field_two" : "value_two"
        },
        {
            "id" : 2,
            "field_one" : "value_one",
            "field_two" : "value_two"
        }
    ],
    "database_table_two" : [
        {
            "id" : 1,
            "field_one" : "value_one"
        }
    ]
}
```

Example : 

```json
{
  "posts": [
    { 
      "id": "1", 
      "title": "a title", 
      "views": 100 
    },
    { 
      "id": "2", 
      "title": "another title", 
      "views": 200 
    }
  ],
  "comments": [
    { 
      "id": "1", 
      "text": "a comment about post 1", 
      "postId": "1" 
    },
    { 
      "id": "2", 
      "text": "another comment about post 1", 
      "postId": "1" 
    }
  ],
  "profile": {
    "name": "Jeet Z. H. Khondker"
  }
}
```

## Alias Configuration for Database Server Execution

In `package.json` File, create an alias script for configuration of Database Server Execution.

```json
...
"scripts": {
  ...,
  "database": "json-server --watch db.json --port 3001"
}
...
```

This can be used to start the database server with one command. The database server will be executed on Port 3001 as Frontend Server is already runningon Port 3000.

## Database Server (JSON Server) Execution

```sh
cd frontend
yarn database
```

## Database Server (JSON Server) Execution URL Endpoint

```sh
http://localhost:3001
```