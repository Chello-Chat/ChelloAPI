# Messages

<img src="https://styviostorage.blob.core.windows.net/styviofilecontainer/logoBanner.png" alt="Chello API"> 
Send, receive, edit, delete, retrieve.  Listen to a room's message stream in real time with a websocket connection.

## Connect, Send, Receive (Websocket)
```
wss://www.chello.chat/ws/messages/
```

### Connect (Websocket.onopen, .send)
Body keys: command (connect), apiKey, roomID


### Send (Websocket.send)
Body keys: command (send), apiKey, roomId, username (string), message (string), programmableKey (optional, stringified JSON), saveBD (optional, avoids saving to database if "False")

### Receive (Websocket.onmessage)
Body keys: username, message, programmableKey, messageID

## Send (POST)
```
https://www.chello.chat/api/messages/send/
```
Body keys:
apiKey, roomID, username, message, programmableKey (optional)

Response keys:
responseStatus, responseText

## Edit (POST)
```
https://www.chello.chat/api/messages/edit/
```
Body keys:
apiKey, messageID, newMessage (optional), newProgrammableKey (optional)

Response keys:
responseStatus, responseText

## Delete (POST)
```
https://www.chello.chat/api/messages/delete/
```
Body keys:
apiKey, messageID

Response keys:
responseStatus, responseText

## Retrieve (POST)
```
https://www.chello.chat/api/messages/retrieve/
```
Body keys:
apiKey, roomID, startsAt (optional, messageID)

Response keys:
responseStatus, responseText, messages

