# valgrind_docker

Simplest docker container for using valgrind
valgrindを使うための最もシンプルなドッカーコンテナ

## Usage 使い方

clone this repository.
このリポジトリをクローンします。
```bash
https://github.com/AuroraSloan/valgrind_docker
```
Create a local directory that will contain your project. 
Copy your project to the directory you created.
This directory will be copied to the container.
In this example I am using a directory called 'src'.
ローカルでプロジェクトを格納するディレクトリを作成します。
作成したディレクトリにプロジェクトをコピーします。
このディレクトリはコンテナにコピーされます。
この例では、「src」というディレクトリを使用しています。

Build the image.
イメージを作成します。

```bash
docker build -t valgrind_image .
```

Run the container.
コンテナを実行します。

```bash
docker run -it -v /<absolute_path>/srcs:/srcs valgrind_image
```
```bash
docker run -it -v /<絶対パス>/srcs:/srcs valgrind_image
```

`-it` will enter you into the container directly from the terminal.
`-it` でターミナルから直接コンテナに入ることができます。

`-v` will allow you to mount a shared directory your local workspace and the container.<br>
i.e `-v <local path>:<container path>`

`-v` により、ローカル・ワークスペースとコンテナの共有ディレクトリをマウントすることができます。<br>
例えば `-v <ローカルパス>:<コンテナパス>`
