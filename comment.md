# reading the comments

assuming `bliish_token` is a valid bliish token\
assuming `post_id` is the post to comment on (ex: HLB5avAp, get from (...) -> "copy link" -> copy the letters at the end)\
\
get request to `https://bliish.com/api/v1/posts/{post_id}/comments`\
\
file headers

```
{
    "cookie": "sb-prkqirdzadljdpkrvjvz-auth-token={bliish_token};",
    "origin": "https://bliish.com",
    "referer": "https://bliish.com",
    "content-type": "application/json"
}
```

credits: [@ajtabjs: bliish-toolbox: main: /main.py](https://github.com/ajtabjs/bliish-toolbox/blob/main/main.py)

# posting a comment

assuming `bliish_token` is a valid bliish token\
assuming `comment_text` is the text to be commented\
assuming `post_id` is the post to comment on (ex: QZQXftQz, get from (...) -> "copy link" -> copy the letters at the end)\
\
post request to `https://bliish.com/api/v1/posts/{post_id}/comments`\
\
file headers

```
{
    "cookie": f"sb-prkqirdzadljdpkrvjvz-auth-token={bliish_token};",
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
