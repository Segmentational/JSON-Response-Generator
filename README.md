# JSON-Response-Generator #

*`mockend` Front-End Unit Testing + JSON Generation*

## Overview ##

API endpoint is available at https://mockend.com/cloud-hybrid/json-response-generator/graphql
- Formatted: `https://mockend.com/cloud-hybrid/json-response-generator/graphql`

## Example ##

`graphql` has a special type of formatted JSON; for example:

```graphql
{ 
    posts(limit: 1) {
        title
    } 
}
```

The exact function + arguments are dependent upon another
JSON file, `.mockend.json`:

```json
{
  "Post": {
    "title": "string",
    "views": "int",
    "published": "boolean",
    "createdAt": "date",
    "comments": "Comment[]"
  },
  "Comment": {
    "body": "string",
    "post": "Post"
  }
}
```

Finally, using the aforementioned `.mockend.json` file & `graphql` query will return
a JSON response:

```json
{
  "data": {
    "posts": [
      {
        "title": "jIMYipLrgi"
      }
    ]
  }
}
```
