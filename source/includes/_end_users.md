# End Users

## End User Object

A end user object has the following fields:

Attribute | Type | Description
--------- | ------- | -----------
id | integer | 
created_at | datetime |
updated_at | datetime |
email | string |
last_surveyed | datetime |
external_created_at | integer |
user_id | integer |
page_views_count | integer |
properites | hstore |

## Get All End Users

```shell
curl "http://api.wootric.com/api/end_users"
  -H "Authorization: meowmeowmeow"
```

> The above command returns JSON structured like this:

```json
[
  {
    "id": 1,
    "created_at" : "2014-12-01 18:36:59",
    "updated_at" : "2014-12-01 18:36:59",
    "email": "nps@example.com",
    "last_surveyed": null,
    "external_created_at": null,
    "user_id": 16,
    "page_views_count" : 1,
    "properites": {"plan": "Small Business", "product": "Example"}
  },
  {
    "id": 2,
    "created_at" : "2014-12-01 18:36:59",
    "updated_at" : "2014-12-04 12:43:44",
    "email": "nps2@example.com",
    "last_surveyed": null,
    "external_created_at": null,
    "user_id": 16,
    "page_views_count" : 3,
    "properites": {"plan": "Enterprise", "product": "The Company"}
  }
]
```

This endpoint retrieves all kittens.

### HTTP Request

`GET http://api.wootric.com/api/end_users`

### Query Parameters

Parameter | Default | Description
--------- | ------- | -----------
include_cats | false | If set to true, the result will also include cats.
available | true | If set to false, the result will include kittens that have already been adopted.

<aside class="success">
Remember — a happy kitten is an authenticated kitten!
</aside>

## Get a Specific End User

```shell
curl "http://api.wootric.com/api/end_users/2"
  -H "Authorization: meowmeowmeow"
```

> The above command returns JSON structured like this:

```json
  {
    "id": 2,
    "created_at" : "2014-12-01 18:36:59",
    "updated_at" : "2014-12-04 12:43:44",
    "email": "nps2@example.com",
    "last_surveyed": null,
    "external_created_at": null,
    "user_id": 16,
    "page_views_count" : 3,
    "properites": {"plan": "Enterprise", "product": "The Company"}
  }
```

This endpoint retrieves a specific kitten.

<aside class="warning">If you're not using an administrator API key, note that some kittens will return 403 Forbidden if they are hidden for admins only.</aside>

### HTTP Request

`GET http://api.wootric.com/api/end_users/<ID>`

### URL Parameters

Parameter | Description
--------- | -----------
ID | The ID of the end user to retrieve