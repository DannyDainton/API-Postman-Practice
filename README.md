# API-Postman-Practice

As an addition to the [blog post](https://dannydainton.com/2017/05/15/30-second-apis) I wrote about using the [json-server](https://github.com/typicode/json-server) node module, which enables you to make HTTP requests in seconds. I wanted to also get you going with a few practice requests that you can use within Postman.  

### Using the Collection

I'm actually trying something new, you can share a collection from your Postman client and add a "Run in Postman" button to a site, it's the first time that i'm giving it a go so let me know if it doesn't work.

[![Run in Postman](https://run.pstmn.io/button.svg)](https://app.getpostman.com/run-collection/ec29167cc815f290833e)

Alternatively, you can just grab the collection .json file from this repo and manually import this on your machine. It's up to you :)

Although this collection is solely aimed at requesting and posting data using the `dummyUsers.json` file, the same requests can be used with any data file that you create. You will just need to amend the requests as per your routes/endpoints. 

### Just to get you started
Once you have the Json Server collection imported into Postman, you should be able to see the various requests (GETs, POSTs, PUTs and DELETEs) contained within the folder.

Start the server in the directory that you have the `dummyUsers.json` file, using the following command in your terminal: 

```sh
> node json-server dummyUsers.json
```

Add the `--watch` flag to use live-reload on the file or the `-p` flag to change the port number, if required.

Using the `POST Create a New User` request from the collection, inspect the data in the `Body` tab. The request body should look like this:
```json
{
 "id":99,
 "first_name":"Joe",
 "last_name":"User",
 "email":"JoeUser@gmail.com",
 "gender":"Male",
 "ip_address":"999.999.999.999"
}
```
If you're happy with the data, press `Send` on the UI or hit `Ctrl+Enter` to create the new user. You can use the `GET All Users` request to see the new user, as well as the all the other users with the json file. 

So that's just a basic collection to get you started, explore with making new requests or start to intergate some of the json-server features:

- [Filter](https://github.com/typicode/json-server#filter)
- [Sort](https://github.com/typicode/json-server#sort)
- [Full-text search](https://github.com/typicode/json-server#full-text-search)
- [Paginate](https://github.com/typicode/json-server#paginate)

As always, let me know if you have an questions!! Enjoy!
