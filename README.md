# X-UI Docker 版

> 基于 https://github.com/sprov065/x-ui 制作的 Docker镜像，原汁原味，未做任何改动

x-ui 使用说明：https://github.com/sprov065/x-ui/blob/main/README.md

### Docker版本说明

拉取镜像：`docker push thesadboy/x-ui`

创建容器：`docker run --restart=always --name x-ui -d -p 54321:54321 -p 8000-8010:8000-8010/tcp -p 8000-8010:8000-8010/udp --tmpfs /tmp --tmpfs /run --tmpfs /run/lock -v /sys/fs/cgroup:/sys/fs/cgroup:ro -v /你的数据存放路径(最好是绝对路径):/etc/x-ui thesadboy/x-ui`

注意：8000-8010是你创建账户用到的端口（同时绑定了TCP/UDP 协议，不建议绑定太多端口），54321 是管理页面访问端口，本地端口也可看自己需求改动，请注意在宿主机上将以上端口放行