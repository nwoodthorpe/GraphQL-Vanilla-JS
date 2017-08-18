# GraphQL-Vanilla-JS
A vanilla JS client that simplifies making GraphQL requests

The library exposes one global, `GraphQL`, which is used for creating clients.

# Example

```javascript
// Create the client, specify the endpoint URL
client = GraphQL.makeClient("https://api.github.com/graphql"); 

// Set headers to be passed with each request
// The GitHub API specifies authentication via the Authorization header
client.setHeader("Authorization", "bearer " + auth_token);  

var query = `
query {
  user {
    login
  }
}`;

// Pass the query and a callback to handle the response
client.query(query, function(response){ 
  console.log(response); // {"data":{"user":{"login":"nwoodthorpe"}}}
});
```
