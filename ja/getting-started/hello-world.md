> English version is [here](https://doc.poac.pm/en/getting-started/hello-world.html)

## Hello World

poac で新しいプロジェクトを始めるには、`poac new`コマンドを使用します:
```bash
$ poac new hello_world
Created: application `hello_world` project
Running: git init hello
```

プロジェクトディレクトリに移動します。
```bash
$ cd hello_world
$ tree . -a -L 1
.
├── .git
├── .gitignore
├── README.md
├── main.cpp
└── poac.yml

1 directories, 4 files
```

`poac.yml` は設定ファイルです。(`poac.yaml`は無視されます。必ず`poac.yml`にしてください)


ここに依存関係やパッケージの情報を記載します。

設定ファイルの書き方の詳細に関しては [2.4. 設定ファイル](../guide/config-file.md) を参照して下さい。


`poac build`を実行すると、poac は “hello_world” バイナリを生成します:
```bash
$ poac build
Compiled: Output to `_build/bin/hello_world`

$ ./_build/bin/hello_world
Hello, world!
```

また、`poac run`を使用してコンパイルと実行を行うことができます:
```bash
$ poac run
Compiled: Output to `_build/bin/hello_world`
Running: `_build/bin/hello_world`
Hello, world!
```
