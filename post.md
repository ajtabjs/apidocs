assuming `bliish_token` is a valid bliish token\
assuming `post_text` is the text to be posted\
\
post request to `https://bliish.com/api/v1/posts`\
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

json

```
{
    "body": post_text,
    "client_mutation_id": "ajs-bliishtoolbox"
}
```

credits: [@ajtabjs: bliish-toolbox: main: /main.py](https://github.com/ajtabjs/bliish-toolbox/blob/main/main.py)
