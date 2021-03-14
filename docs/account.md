Account
=======

## Account base

Request standard user information. If you need the username for the account that is logged in, it is returned in the request for an access token.

```
from imgur_python import Imgur

username = 'someImgurUserName'
imgur_client = Imgur({'client_id': 'cf8c57ca8......'})
user_info = imgur_client.account_base(username)
print(user_info)
```

## Block status

Determine if the user making the request has blocked a username.

```
from imgur_python import Imgur

username = 'someImgurUserName'
imgur_client = Imgur({'client_id': 'cf8c57ca8......'})
block_info = imgur_client.block_status(username)
print(block_info)
```

## Blocked accounts

List all accounts being blocked.

```
from imgur_python import Imgur

imgur_client = Imgur({'client_id': 'cf8c57ca8......'})
block_info = imgur_client.blocks()
print(block_info)
```

## Block user

Block a user

```
from imgur_python import Imgur

imgur_client = Imgur({'client_id': 'cf8c57ca8......'})
block_info = imgur_client.block(username)
print(block_info)
```

## Unblock user

Unblock a user

```
from imgur_python import Imgur

imgur_client = Imgur({'client_id': 'cf8c57ca8......'})
block_info = imgur_client.unblock(username)
print(block_info)
```

## Favorites

Returns the users favorited images, only accessible if you're logged in as the user.

```
from imgur_python import Imgur

page = 0
sort = 'newest'
imgur_client = Imgur({'client_id': 'cf8c57ca8......'})
favorites = imgur_client.favorites(page, sort)
print(favorites)
```

## Submissions

Return the images a user has submitted to the gallery.

```
from imgur_python import Imgur

username = 'someImgurUserName'
page = 0
imgur_client = Imgur({'client_id': 'cf8c57ca8......'})
submissions = imgur_client.submissions(username, page)
print(submissions)
```

## Avatars

Get the list of available avatars for the current account

```
from imgur_python import Imgur

imgur_client = Imgur({'client_id': 'cf8c57ca8......'})
avatars = imgur_client.avatars()
print(avatars)
```

## Avatar

Get the current account's avatar URL and avatar name.

```
from imgur_python import Imgur

imgur_client = Imgur({'client_id': 'cf8c57ca8......'})
avatar = imgur_client.avatar()
print(avatar)
```

## Settings

Returns the account settings.

```
from imgur_python import Imgur

imgur_client = Imgur({'client_id': 'cf8c57ca8......'})
settings = imgur_client.settings()
print(settings)
```

## Save Settings

Updates the account settings for a given user. It's the same method as settings, but if you pass the settings object, it will update the account data. All the parameters are optional.

```
from imgur_python import Imgur

settings_data = {
    'bio': 'The biography of the user, is displayed in the gallery profile page',
    'public_images': 'Set the users images to private or public by default',
    'messaging_enabled': 'true or false - Allows the user to enable / disable private messages',
    'album_privacy': 'public, hidden or secret - Sets the default privacy level of albums the users creates',
    'accepted_gallery_terms': 'true or false - The user agreement to the Imgur Gallery terms',
    'username': 'A valid Imgur username (between 4 and 63 alphanumeric characters',
    'show_mature': 'true or false - Toggle display of mature images in gallery list endpoints',
    'newsletter_subscribed': 'true or false - Toggle subscription to email newsletter'
}

imgur_client = Imgur({'client_id': 'cf8c57ca8......'})
response = imgur_client.settings(settings_data)
print(response)
```
## Account gallery profile

Returns the totals for the gallery profile.

```
from imgur_python import Imgur

username = 'someImgurUserName'
imgur_client = Imgur({'client_id': 'cf8c57ca8......'})
gallery_profile = imgur_client.gallery_profile(username)
print(gallery_profile)
```

## Follow tag

Follows the __tagName__ specified for the currently logged in user.

```
from imgur_python import Imgur

tag_name = 'someImgurTagName'
imgur_client = Imgur({'client_id': 'cf8c57ca8......'})
result = imgur_client.follow_tag(tag_name)
print(result)
```

## Unfollow tag

Unfollows the __tagName__ specified for the currently logged in user.

```
from imgur_python import Imgur

tag_name = 'someImgurTagName'
imgur_client = Imgur({'client_id': 'cf8c57ca8......'})
result = imgur_client.unfollow_tag(tag_name)
print(result)
```

## Notifications

Returns all of the reply notifications for the user.

| Value | Description                                                       |
|-------|-------------------------------------------------------------------|
| new   | alse for all notifications, true for only non-viewed notification |

```
from imgur_python import Imgur

new = False
imgur_client = Imgur({'client_id': 'cf8c57ca8......'})
result = imgur_client.notifications(new)
print(result)
```