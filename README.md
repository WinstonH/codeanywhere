# codeanywhere

git clone https://github.com/WinstonH/codeanywhere.git && codeanywhere/codeanywhere.sh 

codeanywhere的免费容器container，提供了所有http和websocket端口，不提供tcp端口，但有一个“漏洞”，它提供了ssh远程连接，也就是对外映射了22/tcp。

该脚本实现了以下功能： \
1.自动替换ssh端口22→220，原22端口用ssr代替，且做了redirect转发，以防止codeanywhere的UI界面无法连接终端 \
2.在容器内搭建了xfce中文桌面环境+vnc \
3.使用novnc连接vnc桌面，内部端口为3000，即codeanywhere提供的https接口 \
4.安装了火狐和谷歌；谷歌用于登录codeanywhere（默认屏蔽，登录需要特殊姿势），使容器主机保持开启；火狐用于挂机等任务。
