```shell
#!/usr/local/bin/fish

function 5hl; test (count $argv) -gt 0; or set argv hello; set -l IFS; set w (wget -qO- https://5hl.github.io/"$argv[1]"); and echo "$w" | sh -s "$argv[2..-1]"; end

5hl hello world
```

```shell
#!/bin/bash

5hl() { s="${1:-hello}"; shift; w=$(wget -qO- https://5hl.github.io/"${s}") && echo "${w}" | sh -s "${@}"; }

5hl hello world
```

```shell
wget -qO- https://5hl.github.io/hello | sh -s world
```

```shell
curl -sSL https://5hl.github.io/hello | sh -s world
```

```shell
curl -i https://git.io -F "url=https://raw.githubusercontent.com/5hl/5hl.github.io/m/hello" -F "code=5hl-hello"
```

```shell
wget -qO- https://git.io/5hl-hello | sh -s world

curl -ssL https://git.io/5hl-hello | sh -s world
```
