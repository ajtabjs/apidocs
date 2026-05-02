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
