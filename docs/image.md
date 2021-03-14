Image
=====

## Images

Return all of the images associated with the account. You can page through the images by setting the page, this defaults to 0.

```
from imgur_python import Imgur

page = 0
imgur_client = Imgur({'client_id': 'cf8c57ca8......'})
images = imgur_client.images(page)
print(images)
```

## Image

Get information about an image.

```
from imgur_python import Imgur

image_id = 'someImgurImageId'
imgur_client = Imgur({'client_id': 'cf8c57ca8......'})
image = imgur_client.image(image_id)
print(image)
```

## Image upload

Upload a new image or video.

| Key           | Description                                           |
|---------------|-------------------------------------------------------|
| file          | The path of the image, video, or the URL.             |
| title         | The title of the image.                               |
| description   | description of the image.                             |
| album         | The id of the album you want to add the image.        |
| disable_audio | Remove the audio track of the video.                  |

```
from os import path
from imgur_python import Imgur

file = path.realpath('./images/untitled.png')
title = 'Untitled'
description = 'Image description'
album = None
disable_audio = 0

imgur_client = Imgur({'client_id': 'cf8c57ca8......'})
response = imgur_client.image_upload(file, title, description, album, disable_audio)
print(response)
```

## Image update

Updates the title or description of an image.

```
from imgur_python import Imgur

image_id = 'someImgurImageId'
title = 'Untitled'
description = 'Image description'

imgur_client = Imgur({'client_id': 'cf8c57ca8......'})
response = imgur_client.image_update(image_id, title, description)
print(response)
```

## Image delete

Deletes an image.

```
from imgur_python import Imgur

image_id = 'someImgurImageId'

imgur_client = Imgur({'client_id': 'cf8c57ca8......'})
response = imgur_client.image_delete(image_id)
print(response)
```

## Image IDs

Returns an array of Image IDs that are associated with the account.

```
from imgur_python import Imgur

page = 0

imgur_client = Imgur({'client_id': 'cf8c57ca8......'})
response = imgur_client.image_ids(page)
print(response)
```

## Favorite an Image

Favorite an image with the given ID.

```
from imgur_python import Imgur

image_id = 'someImgurImageId'

imgur_client = Imgur({'client_id': 'cf8c57ca8......'})
response = imgur_client.image_fav(image_id)
print(response)
```