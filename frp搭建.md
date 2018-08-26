#git地址 https://github.com/fatedier/frp

frpc.ini 常用配置
[common]
server_addr = 127.0.0.1
server_port = 7000
token = token

[ssh]
type = tcp
local_ip = 127.0.0.1
local_port = 22
remote_port = 6000

启动frpc
./frpc -c frpc.ini >/dev/null 2>&1 &

ftps.ini 配置
[common]
bind_port = 7000
vhost_http_port = 8080
privilege_token = token

#dashboard
dashboard_port = 7001
dashboard_user = admin
dashboard_pwd = pwd
log_file = ./log/frps.log
log_level = info
log_max_days = 5

启动frps
./frps -c frps.ini >/dev/null 2>&1 &