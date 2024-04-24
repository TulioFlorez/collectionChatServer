# CollectionChatServer

## POST http://localhost:8080/api/chatrooms
This is a POST request, submitting data to an API via the request body. This request submits JSON data, and the data is reflected in the response.

A successful POST request typically returns a 200 OK or 201 Created response code.

### Authorization
**Basic Auth**
Username: admin
Password: adminpassword

**Body**
raw (json)
json
{
  "name": "room1"
}

## POST  http://localhost:8080/api/messages (USER1 & USER2)
This API endpoint allows you to send a POST request to create a new message in a chat room. The request should be sent to http://localhost:8080/api/messages with a JSON payload in the request body.

###Authorization
**Basic Auth**
Username: user1
Password: chatpassword 

**Basic Auth**
Username: user2
Password: newpassword

**Request Body**
content (string, required): The content of the message.
chatRoom (string, required): The name or ID of the chat room where the message should be posted.

**Response**
Upon successful execution, the API will return a JSON response with a status code of 200 and the following structure:


JSON

{
    "room": "",
    "chat": [
        {
            "user": "",
            "message": ""
        }
    ]
}


room (string): The name or ID of the chat room where the message was posted.
chat (array): An array containing the details of the posted message, including the user who posted the message and the message content.


## DELETE  http://localhost:8080/api/messages
This is a DELETE request, and it is used to delete the last message`s user 

### Authorization
**Basic Auth**
Username: user1
Password: chatpassword

## get  http://localhost:8080/api/messages
This is a GET request and it is used to retrieve the historial chat
### Authorization
**Basic Auth**
Username: user1
Password: chatpassword




