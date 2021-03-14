Album
=====

## Albums

Get all the albums associated with the account.

```
from imgur_python import Imgur

page = 0
imgur_client = Imgur({'client_id': 'cf8c57ca8......'})
albums = imgur_client.albums(page)
print(albums)
```

## Album

Get additional information about an album.

```
from imgur_python import Imgur

album_id = 'SomeAlbumHash'
imgur_client = Imgur({'client_id': 'cf8c57ca8......'})
album = imgur_client.album_get(album_id)
print(album)
```

## Album Images

Get information about an image in an album.

```
from imgur_python import Imgur

album_id = 'SomeAlbumHash'
imgur_client = Imgur({'client_id': 'cf8c57ca8......'})
images = imgur_client.album_images(album_id)
print(images)
```

## Album create

Create a new album. The privacy level of the album could be public, hidden or secret.

| Key         | Required | Description                                                                 |
|-------------|----------|-----------------------------------------------------------------------------|
| ids[]       | optional | The image ids that you want to be included in the album.                    |
| title       | optional | The title of the album                                                      |
| description | optional | The description of the album                                                |
| privacy     | optional | Sets the privacy level of the album. Values are : public, hidden or secret. |

```
from imgur_python import Imgur

images = []
title = 'Album title'
description = 'Album description'
privacy = 'hidden'

imgur_client = Imgur({'client_id': 'cf8c57ca8......'})
response = imgur_client.album_create(images, title, description, privacy)
print(response)
```

## Album update

Update the information of an album. The privacy level of the album could be public, hidden or secret.
The update will replace all the previous images.

```
from imgur_python import Imgur

album_id = 'SomeAlbumId'
images = ['g38lQAb', 'flF3tuE', 'DZhTxTf', 'qmjQAHV']
title = 'Album edited title'
description = 'Album edited description'
privacy = 'hidden'

imgur_client = Imgur({'client_id': 'cf8c57ca8......'})
response = imgur_client.album_update(album_id, images, title, description, privacy)
print(response)
```

## Album delete

Delete an album with a given deletehash.

```
from imgur_python import Imgur

delete_hash = 'someAlbumDeleteHash'
imgur_client = Imgur({'client_id': 'cf8c57ca8......'})
response = imgur_client.album_delete(delete_hash)
print(response)
```

## Add images

Adds the marked images to an album.

```
from imgur_python import Imgur

album_id = 'SomeAlbumId'
images = ['g38lQAb', 'flF3tuE', 'DZhTxTf', 'qmjQAHV']

imgur_client = Imgur({'client_id': 'cf8c57ca8......'})
response = imgur_client.album_add(album_id, images)
print(response)
```

## Remove images

Remove the marked images from an album.

```
from imgur_python import Imgur

delete_hash = 'SomeAlbumDeleteHash'
images = ['DZhTxTf', 'qmjQAHV']

imgur_client = Imgur({'client_id': 'cf8c57ca8......'})
response = imgur_client.album_remove(delete_hash, images)
print(response)
```

## Album IDs

Return an array of all of the album IDs (hashes).

```
from imgur_python import Imgur

page = 0
imgur_client = Imgur({'client_id': 'cf8c57ca8......'})
result = imgur_client.album_ids(page)
print(result)
```

## Favorite Album

Favorite an album with a given ID.

```
from imgur_python import Imgur

album = 'SomeAlbumHash'
imgur_client = Imgur({'client_id': 'cf8c57ca8......'})
result = imgur_client.album_fav(album)
print(result)
```