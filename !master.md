# bliip users

assuming `bliish_cookies` are valid bliish token cookies\
assuming `bliip_handle` is the user's handle to be bliipped\
\
post request to `https://bliish.com/api/v1/bliips`\
\
file headers

```
{
    "cookie": bliish_cookies,
    "origin": "https://bliish.com",
    "referer": "https://bliish.com",
    "content-type": "application/json"
}
```

json

```
{
    "handle": bliip_handle
}
```

credits: [@ajtabjs: bliish-toolbox: main: /main.py](https://github.com/ajtabjs/bliish-toolbox/blob/main/main.py)

# reading the comments

assuming `bliish_cookies` are valid bliish token cookies\
assuming `post_id` is the post to comment on (ex: HLB5avAp, get from (...) -> "copy link" -> copy the letters at the end)\
\
get request to `https://bliish.com/api/v1/posts/{post_id}/comments`\
\
file headers

```
{
    "cookie": bliish_cookies,
    "origin": "https://bliish.com",
    "referer": "https://bliish.com",
    "content-type": "application/json"
}
```

credits: [@ajtabjs: bliish-toolbox: main: /main.py](https://github.com/ajtabjs/bliish-toolbox/blob/main/main.py) / me

# posting a comment

assuming `bliish_cookies` are valid bliish token cookies\
assuming `comment_text` is the text to be commented\
assuming `post_id` is the post to comment on (ex: QZQXftQz, get from (...) -> "copy link" -> copy the letters at the end)\
\
post request to `https://bliish.com/api/v1/posts/{post_id}/comments`\
\
file headers

```
{
    "cookie": bliish_cookies,
    "origin": "https://bliish.com",
    "referer": "https://bliish.com",
    "content-type": "application/json"
}
```

json

```
{
    "body": comment_text,
    "client_mutation_id": "ajs-bliishtoolbox"
}
```

credits: [@ajtabjs: bliish-toolbox: main: /main.py](https://github.com/ajtabjs/bliish-toolbox/blob/main/main.py)

# get user feed

assuming `bliish_cookies` are valid bliish token cookies\
\
get request to `https://bliish.com/api/v1/feed`\
\
file headers

```
{
    "cookie": bliish_cookies,
    "origin": "https://bliish.com",
    "referer": "https://bliish.com",
    "content-type": "application/json"
}
```

credits: me

# post

assuming `bliish_cookies` are valid bliish token cookies\
assuming `post_text` is the text to be posted\
\
post request to `https://bliish.com/api/v1/posts`\
\
file headers

```
{
    "cookie": bliish_cookies,
    "origin": "https://bliish.com",
    "referer": "https://bliish.com",
    "content-type": "application/json"
}
```

json

```
{
    "body": post_text,
    "client_mutation_id": "ajs-bliishtoolbox"
}
```

credits: [@ajtabjs: bliish-toolbox: main: /main.py](https://github.com/ajtabjs/bliish-toolbox/blob/main/main.py)

# get user's wall

assuming `bliish_cookies` are valid bliish token cookies\
assuming `wall_handle` is the user's handle who's wall to read (i hate the english language)\
\
post request to `https://bliish.com/api/v1/profiles/{wall_handle}/wall`\
\
file headers

```
{
    "cookie": bliish_cookies,
    "origin": "https://bliish.com",
    "referer": "https://bliish.com",
    "content-type": "application/json"
}
```

credits: [@ajtabjs: bliish-toolbox: main: /main.py](https://github.com/ajtabjs/bliish-toolbox/blob/main/main.py)
