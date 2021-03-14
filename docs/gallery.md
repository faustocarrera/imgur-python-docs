Gallery
=======

## Gallery Tags

Gets a list of default tags.

```
from imgur_python import Imgur

imgur_client = Imgur({'client_id': 'cf8c57ca8......'})
tags = imgur_client.tags()
print(tags)
```

## Gallery Tag Info

Gets metadata about a tag.

```
from imgur_python import Imgur

tag_name = 'someImgurTagName'

imgur_client = Imgur({'client_id': 'cf8c57ca8......'})
tag_info = imgur_client.tag_info(tag_name)
print(tag_info)
```

## Share with Community (Image)

Share an Album or Image to the Gallery.

```
from imgur_python import Imgur

image_id = 'someImgurImageId'
title = 'Some cat pictures'
mature = 0
tags = 'funny,cats'

imgur_client = Imgur({'client_id': 'cf8c57ca8......'})
response = imgur_client.gallery_image(image_id, title, mature, tags)
print(response)
```

## Share with Community (Album)

Share an Album or Image to the Gallery.

```
from imgur_python import Imgur

album_id = 'someImgurAlbumId'
title = 'Some cat pictures'
mature = 0
tags = 'funny,cats'

imgur_client = Imgur({'client_id': 'cf8c57ca8......'})
response = imgur_client.gallery_album(album_id, title, mature, tags)
print(response)
```

## Remove from Gallery

Remove an image from the public gallery.

```
from imgur_python import Imgur

gallery_id = 'someImgurGalleryHash'

imgur_client = Imgur({'client_id': 'cf8c57ca8......'})
response = imgur_client.gallery_remove(gallery_id)
print(response)
```