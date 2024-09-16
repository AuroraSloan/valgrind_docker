# valgrind_docker

Simplest docker container for using valgrind<br>
valgrindを使うための最もシンプルなドッカーコンテナ

## Usage 使い方

clone this repository.<br>
このリポジトリをクローンします。
```bash
https://github.com/AuroraSloan/valgrind_docker
```
Copy your project to the 'srcs' directory.<br>
This directory will be mounted to the container.<br>
プロジェクトを「srcs」ディレクトリにコピーします。
このディレクトリはコンテナにマウントされます。

Build the image.<br>
イメージを作成します。

```bash
docker build -t valgrind_image .
```

Run the container.<br>
コンテナを実行します。

```bash
docker run -it -v /<absolute_path>/srcs:/srcs valgrind_image
```
```bash
docker run -it -v /<絶対パス>/srcs:/srcs valgrind_image
```

`-it` will enter you into the container directly from the terminal.<br>
`-it` でターミナルから直接コンテナに入ることができます。<br>

`-v` will allow you to mount a shared directory your local workspace and the container.<br>
i.e `-v <local path>:<container path>`<br>

`-v` により、ローカル・ワークスペースとコンテナの共有ディレクトリをマウントすることができます。<br>
例えば `-v <ローカルパス>:<コンテナパス>`
