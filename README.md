## To do app

This repo contains code for inserting users,inserting todos and deleting todos to any underlying database( here it is a pg ) containing these tables. This . You need to enter the appropriate connection string for your db.
Take a look at this [docs](https://hasura.io/docs/3.0/getting-started/local-dev/) to setup the hasurav3 project and configure your database.

Run the below command from the directory containing functions to use the typescript-hasura dataaconnector available in denoland to generate metadata for hasura project. This sets up the listener in localhost:8100.
```sh
deno run -A --watch --check https://deno.land/x/hasura_typescript_connector/mod.ts serve --configuration ./config.json
```
Read more about how to configure this [here](https://github.com/hasura/ndc-typescript-deno)


Befor creating hasura build make sure you use the below command to create a secure tunnel from your hasura3 cloud project and localhost. 
```sh
hasura3 cloud tunnel localhost:8100
```
Replace the localhost:8100 URL with the URL obtained from the above step
Once you make any changes to signatures of existing function or add new functions make sure to run ` Refresh data sources` command & `Track all collections` command from the cmd plt and create a new build following the above steps.