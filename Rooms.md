# Rooms

<img src="https://styviostorage.blob.core.windows.net/styviofilecontainer/logoBanner.png" alt="Chello API"> 
Create, Edit, Delete.  Add custom fields by passing stringified JSON through programmableKey (255 char limit).

## Create (POST)
```
https://www.chello.chat/api/rooms/create/
```
Body keys:
apiKey, name, photo (optional, URL), programmableKey (optional)

Response keys:
responseStatus, responseText, roomID

## Edit (POST)
```
https://www.chello.chat/api/rooms/edit/
```
Body keys:
apiKey, roomID, newName (optional), newPhoto (optional), newProgrammableKey (optional)

Response keys:
responseStatus, responseText

## Delete (POST)
```
https://www.chello.chat/api/rooms/delete/
```
Body keys:
apiKey, roomID

Response keys:
responseStatus, responseText

