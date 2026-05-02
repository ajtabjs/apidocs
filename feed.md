# page one of feed

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

# more pages of feed

this relies on page one and/or the last page so do that first\

assuming `bliish_cookies` are valid bliish token cookies\
assuming `last_post_uuid` is the last page's last post's uuid\
assuming `last_post_time` is the last page's last post's `created_at` timestamp in the `yyyy-MM-DDThh:mm:ss.ddddd+00:00` (`ex: 2026-05-02T15:41:42.38913+00:00`) NOT to be confused with the timestamp at the time of sending the request (why does this have to be so complicated \[nvm thats a dumb question\])\
\
get request to `https://bliish.com/api/v1/feed?cursor={last_post_time}|{last_post_uuid}` (like for example: `https://bliish.com/api/v1/feed?cursor=2026-05-02T15:41:42.38913+00:00|0f96630f-016d-4d1c-97ac-5c55de91f797`)\ but url escape everything after `?cursor=`
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