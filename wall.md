# page one of wall

assuming `bliish_cookies` are valid bliish token cookies\
assuming `wall_handle` is the user's handle who's wall to read\
\
get request to `https://bliish.com/api/v1/profiles/{wall_handle}/wall`\
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

# more pages of feed

this relies on page one and/or the last page so do that first

assuming `bliish_cookies` are valid bliish token cookies
assuming `wall_handle` is the user's handle who's wall to read\
assuming `last_post_uuid` is the last page's last post's uuid\
assuming `last_post_time` is the last page's last post's `created_at` timestamp in the `yyyy-MM-DDThh:mm:ss.ddddd+00:00` (`ex: 2026-05-02T15:41:42.38913+00:00`) NOT to be confused with the timestamp at the time of sending the request (why does this have to be so complicated \[thats a dumb question\])

assuming `bliish_cookies` are valid bliish token cookies\
\
get request to `https://bliish.com/api/v1/profiles/{wall_handle}/wall?cursor={last_post_time}|{last_post_uuid}` (like for example: `https://bliish.com/api/v1/profiles/{wall_handle}/wall?cursor=2026-05-02T15:41:42.38913+00:00|0f96630f-016d-4d1c-97ac-5c55de91f797`)\ but url escape everything after `?cursor=`
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