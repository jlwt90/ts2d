# TS2D

TS2D is the command that translates a Timestamp to Date

# Installation

```
$ go install github.com/s-ichikawa/ts2d@latest
```

# Usage

```
$ echo 1660358443.2188597 | ts2d
"2022-08-13 11:40:43.002188597 +0900 JST"
```

example of kubectl logs
```
$ kubectl logs -f hello-server-1234567890-abcdef
{"level":"info","ts":1660358286.850947,"msg":"hello"}
{"level":"info","ts":1660358286.8685086,"msg":"hello"}
...

$ kubectl logs -f hello-server-1234567890-abcdef | ts2d
{"level":"info","ts":"2022-08-13 11:38:06.000850947 +0900 JST","msg":"hello"}
{"level":"info","ts":"2022-08-13 11:38:06.008685086 +0900 JST","msg":"hello"}
...
```