
# jqr

Hey! This is a jq repl! If you want fancy things like move up or down or use emacs hotkeys, I recommend trying [rlwrap](https://github.com/hanslub42/rlwrap).

# using

```bash
$ jqr
jq% .
{}
jq% .hi = "there!"
{
  "hi": "there!"
}
jq% .person = {name: "jane", hi: 98989}
{
  "hi": "there!",
  "person": {
    "name": "jane",
    "hi": 98989
  }
}
jq% .person
{
  "name": "jane",
  "hi": 98989
}
```

You can also pipe to `jqr -i` or start with a json file with `jqr -f`.

```
$ cat sample.json | jqr -i
jq% .
[
  {
    "_id": "5819adaff07b745f0c13b00b",
    "index": 0,
    "guid": "b3042e42-b3ed-4f4f-aa9f-ac02eef6e65a",
    "isActive": false,
    "balance": "$1,208.06",
    "picture": "http://placehold.it/32x32",
    "age": 26,
    "eyeColor": "brown",
    "name": {
      "first": "Lawson",
      "last": "Bowman"
    }
  }
]
```

# problems

If you index into a json blob, you can't go back. ¯\_(ツ)_/¯

# license

MIT
