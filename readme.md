to find `bliish_cookies` for your account, run the following code snippet while logged in on [bliish](bliish.com):
```
const cookies = document.cookie.split("; ").map(c => {
  const [key, ...rest] = c.split("=");
  return { key, value: rest.join("=") };
});
const main = cookies.find(c => c.key === "sb-prkqirdzadljdpkrvjvz-auth-token");
let result = "";
if (main) {
  result = `${main.key}: ${main.value};`;
} else {
  const part0 = cookies.find(c => c.key === "sb-prkqirdzadljdpkrvjvz-auth-token.0");
  const part1 = cookies.find(c => c.key === "sb-prkqirdzadljdpkrvjvz-auth-token.1");
  if (part0) result += `${part0.key}: ${part0.value};`;
  if (part1) result += `${part1.key}: ${part1.value};`;
}
console.clear();
console.log(result.trim());
```

started on may 1, 2026

# TODO
find out how to get more than one page in on feed.md and wall.md\
start developing bliish-3ds
