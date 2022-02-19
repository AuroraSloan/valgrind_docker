# valgrind_docker

Simplest docker container for using valgrind

## Usage

clone this repositroy
```bash
https://github.com/AuroraSloan/valgrind_docker
```

Build the image

```bash
docker build -t val .
```

Run the container

`-it` will enter you into the container dirctly from the terminal

`-v` will allow you to mount a shared directory your local workspace and the container<br>
local:container

```bash
docker run -it -v /<absolute_path>/srcs:/srcs val
```
