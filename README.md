# demo-apollo-graphql-nosql-
temporary test using apollo-graphql

WIP : 👷

## install and run

````
npm install apollo-server graphql --save
node index.js
````
## tests commands

Testing resolvers - nested calls
````
curl --location --request POST 'http://localhost:4000/' \
--header 'Content-Type: application/json' \
-d '{"query":"query { libraries { branch,  books { title } }}","variables":{}}' | jq

curl --location --request POST 'http://localhost:4000/' \
--header 'Content-Type: application/json' \
-d '{"query":"query { libraries { branch,  books { title, author { name} } }}","variables":{}}' | jq

````

