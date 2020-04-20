# SMATask

Implement a small REST API in .net core 3.0 that does two things:

- Offers a HTTP Post endpoint that retrieves an JSON Object in the Post Body. The Object needs to be stored in an in memory store (e.g. ConcurrentDictionary or ConcurrentBag)

- Offers a HTTP GET endpoint that has an optional route parameter (integer: start) that returns an array of those json objects from the store with a maximum of 5 entries. When the optional parameter (start) is a positive number, it shall skip that amount of entries from the store and return the next 5 entries.

Optional: Use a Database to store those objects delivered by the API. (e.g. Cosmos db: https://docs.microsoft.com/en-us/azure/cosmos-db/local-emulator )

Starting point on how to create a web api using .net core 3.0:

- https://docs.microsoft.com/en-us/aspnet/core/tutorials/first-web-api?view=aspnetcore-3.0&tabs=visual-studio

Payload object definition:

The input json object shall have the same structure as the output document and is defined as this:

{

"Id": 1, // integer

"Name": "Test", // string

"Text": "Test content", // string

"Created": "2019-11-24T18:55:52.7174882+00:00" // DateTimeOffset Object

}

Please keep out of scope: Authentication, Authorization, HTTPS, CORS, ...
