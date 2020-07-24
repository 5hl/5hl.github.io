```shell
wget -qO- https://5hl.github.io/hello | sh -s world

curl -sSL https://5hl.github.io/hello | sh -s world
```


```shell
curl -i https://git.io -F "url=https://raw.githubusercontent.com/5hl/5hl.github.io/m/hello" -F "code=5hl-hello"
```

```shell
wget -qO- https://git.io/5hl-hello | sh -s world

curl -ssL https://git.io/5hl-hello | sh -s world
```
