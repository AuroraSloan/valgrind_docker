# valgrind_docker

Simplest docker container for using valgrind

## Usage

clone this repositroy
```bash
https://github.com/AuroraSloan/valgrind_docker
```
Move the files you want to check into the srcs directory

Build the image

```bash
docker build -t val .
```

Run the container

```bash
docker run -it -v /<absolute_path>/srcs:/srcs val
```

`-it` will enter you into the container dirctly from the terminal

`-v` will allow you to mount a shared directory your local workspace and the container<br>
i.e `-v <local path>:<container path>`
