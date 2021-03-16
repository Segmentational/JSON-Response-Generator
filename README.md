# JSON-Response-Generator #

*`mockend` Front-End Unit Testing + JSON Generation*

## Overview ##

API endpoint is available at https://mockend.com/cloud-hybrid/json-response-generator/graphql
- Formatted: `https://mockend.com/cloud-hybrid/json-response-generator/graphql`

Example Query Request:

```graphql
{ 
    posts(limit: 1) {
        title
    } 
}
```

which assumes a `.mockend.json` file:

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

finally, response returning as

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
