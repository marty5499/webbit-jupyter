## 產生新的 image
docker build -t jupyter/webbit .

## 執行 jupyter-webai
docker run --name jupyter-webbit -d -v ${PWD}/work:/home/jovyan/— -p 8888:8888 jupyter/webbit

## 進入 jupyter-webai container
docker run --name jupyter-webbit -e GRANT_SUDO=yes --user root -it -v ${PWD}/work:/home/jovyan/— -p 8888:8888 jupyter/webbit bash
