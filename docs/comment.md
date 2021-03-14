Comments
========

# Comments

Return the comments the user has created

```
from imgur_python import Imgur

page = 0
imgur_client = Imgur({'client_id': 'cf8c57ca8......'})
comments = imgur_client.comments(page)
print(comments)
```

# Comment

Get information about a specific comment.

```
from imgur_python import Imgur

comment_id = 'someImgurCommentId'
imgur_client = Imgur({'client_id': 'cf8c57ca8......'})
comment = imgur_client.comment_get(comment_id)
print(comment)
```

# Comment and reply creation

Creates a new comment, returns the ID of the comment. You could provide the ID of the parent comment, this is an alternative method to create a reply. The API provides another method, `Reply Creation`, it works a little bit different, but at the end, it's the same result.

| Key       | Required | Description                                                                    |
|-----------|----------|--------------------------------------------------------------------------------|
| image_id  | required | The ID of the image or album in the gallery that you wish to comment on        |
| comment   | required | The comment text, this is what will be displayed                               |
| parent_id | optional | The ID of the parent comment, this is an alternative method to create a reply. |

```
from imgur_python import Imgur

image_id = 'someImgurAlbumId'
comment = 'Some interesting comment about the post'
parent_id = None
imgur_client = Imgur({'client_id': 'cf8c57ca8......'})
response = imgur_client.comment_post(image_id, comment, parent_id)
print(response)
```

# Comment deletion

Delete a comment by the given id.

```
from imgur_python import Imgur

comment_id = 'someImgurCommentId'
imgur_client = Imgur({'client_id': 'cf8c57ca8......'})
response = imgur_client.comment_delete(comment_id)
print(response)
```

# Comment vote

Vote on a comment. The vote parameter can only be set as up, down or veto.

```
from imgur_python import Imgur

comment_id = 'someImgurCommentId'
imgur_client = Imgur({'client_id': 'cf8c57ca8......'})
response = imgur_client.comment_vote(comment_id, 'up')
print(response)
```

# Comment report

Report a comment for being inappropriate.

| Value | Description                         |
|-------|-------------------------------------|
| 1     | Doesn't belong on Imgur             |
| 2     | Spam                                |
| 3     | Abusive                             |
| 4     | Mature content not marked as mature |
| 5     | Pornography                         |

```
from imgur_python import Imgur

comment_id = 'someImgurCommentId'
imgur_client = Imgur({'client_id': 'cf8c57ca8......'})
response = imgur_client.comment_report(comment_id, 2)
print(response)
```

## Comment IDs

Return an array of all of the comment IDs.

| Value | Description                     |
|-------|---------------------------------|
| sort  | best, worst, oldest, or newest  |
| page  | page number (50 items per page) |

```
from imgur_python import Imgur

page = 0
sort = 'newest'
imgur_client = Imgur({'client_id': 'cf8c57ca8......'})
response = imgur_client.comment_ids(page, sort)
print(response)
```

## Replies

Get the comment with all of the replies for the comment.

```
from imgur_python import Imgur

comment_id = 'someImgurCommentId'
imgur_client = Imgur({'client_id': 'cf8c57ca8......'})
response = imgur_client.comment_replies(comment_id)
print(response)
```
