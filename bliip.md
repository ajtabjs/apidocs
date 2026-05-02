assuming `bliish_token` is a valid bliish token\
assuming `bliip_handle` is the user's handle to be bliipped\
\
post request to `https://bliish.com/api/v1/bliips`\
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
    "handle": bliip_handle
}
```

credits: [@ajtabjs: bliish-toolbox: main: /main.py](https://github.com/ajtabjs/bliish-toolbox/blob/main/main.py)
