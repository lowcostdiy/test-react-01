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

