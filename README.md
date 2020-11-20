# test-react-01

## 01 Setup

git config --global user.email "weihan.goh@hotmail.com"
git config --global user.name "Lowcostdiy"

npm init
npm install --save express body-parser
npm install --save-dev nodemon


## 02 Graphql

npm install --save express-graphql graphql

query {
  events
}

mutation {
  createEvent(name: "Sports")
}

const { graphqlHTTP } = require('express-graphql');

mongoose
  .connect(
    `mongodb+srv://${process.env.MONGO_USER}:${
      process.env.MONGO_PASSWORD
    }@cluster0.23cx7.mongodb.net/${process.env.MONGO_DB}?retryWrites=true&w=majority`
  )
  .then(() => {
    app.listen(3000);
  })
  .catch(err => {
    console.log(err);
  });

## 03 Type Data

query {
  events {
    title
    price
  }
}

mutation {
  createEvent(eventInput: {title: "A Test", description: "Does this work?", price: 9.99, date: "2020-11-20T02:49:52.926Z"}){
    title
    description
  }
}

## 04 MongoDB

npm install --save mongoose


mongodb+srv://user:<password>@cluster0.23cx7.mongodb.net/<dbname>?retryWrites=true&w=majority

mutation {
  createEvent(eventInput: {title: "Second Test", description: "It is working", price: 999.99, date: "2020-11-20T02:49:52.926Z"}){
    _id
    title
    description
  }
}

## 05 Relations

npm install --save bcryptjs

mutation {
  createUser(userInput:{email:"test@test.com", password:"tester"}) {
    email
    password
  }
}

mutation {
  createEvent(eventInput: {title: "A Test", description: "Does this work?", price: 9.99, date: "2020-11-20T02:49:52.926Z"}){
    title
    description
  }
}