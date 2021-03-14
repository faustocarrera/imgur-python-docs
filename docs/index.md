Welcome to the imgur-python wiki!
=================================

The original imgurpython project is no longer supported, so, I decided to create my own python client for the [Imgur API](https://apidocs.imgur.com/?version=latest).

__Disclaimer:__ This is a work in progress. In this first version, I'm not gonna implement all the API calls, only the necessary ones to interact with imgur and be able to create albums, upload images and share them on the site.

## API credentials

You must [register your client](https://api.imgur.com/oauth2/addclient) with the Imgur API, and provide the Client-ID to make any request to the API. If you want to perform actions on accounts, the user will have to authorize your application through OAuth2.

Each client must register their application and receive the `client_id` and `client_secret`.

More info about the API usage [https://apidocs.imgur.com/?version=latest#intro](https://apidocs.imgur.com/?version=latest#intro).

## API client methods

* [Configuration object](config.md)
* [Authorize](authorize.md)
    - Get authorize URL
    - Generate access token
* [Account](account.md)
    - Account Base
    - Block Status
    - Blocks
    - Block
    - Unblock
    - Favorites
    - Submissions
    - Available Avatars
    - Avatar
    - Settings
    - Change Account Settings
    - Account Gallery Profile
    - Follow Tag
    - Unfollow tag
    - Notifications
* [Comment](comment.md)
    - Comments
    - Comment
    - Comment/Reply Creation
    - Comment Deletion
    - Vote
    - Report
    - Comment IDs
    - Replies
* [Album](album.md)
    - Albums
    - Album
    - Album Images
    - Album Creation
    - Update Album
    - Album Deletion
    - Add Images to an Album
    - Remove Images from an Album
    - Album IDs
    - Favorite Album
* [Image](image.md)
    - Images
    - Image
    - Image Upload
    - Image Deletion
    - Update Image Information
    - Image IDs
    - Favorite an Image
* [Gallery](gallery.md)
    - Gallery Tags
    - Gallery Tag Info 
    - Share with Community (Image)
    - Share with Community (Album)
    - Remove from Gallery