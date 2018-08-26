github地址： https://github.com/aria2/aria2
aria2c.conf 配置：
dir=/data/download //目录必须存在
input-file=/data/aria2/aria2.session //文件必须存在
save-session=/data/aria2/aria2.session 

file-allocation=prealloc
log=/data/aria2/log/aria2.log //目录必须存在
log-level=warn
enable-http-pipelining=true
enable-dht=true
bt-enable-lpd=true
enable-peer-exchange=true
max-concurrent-downloads=3
max-connection-per-server=10
min-split-size=10M
split=10
continue=true
max-overall-download-limit=0
max-overall-upload-limit=1K
listen-port=51413
enable-rpc=true
rpc-listen-all=true
rpc-allow-origin-all=true
rpc-listen-port=6800
rpc-secret=6463279
seed-time=0
#bt
bt-tracker=udp://tracker.coppersurfer.tk:6969/announce,udp://tracker.leechers-paradise.org:6969/announce,udp://allesanddro.de:1337/announce,udp://9.rarbg.to:2710/announce,udp://p4p.arenabg.com:1337/announce,http://p4p.arenabg.com:1337/announce,udp://tracker.internetwarriors.net:1337/announce,http://tracker.internetwarriors.net:1337/announce,http://tracker.opentrackr.org:1337/announce,udp://tracker2.christianbro.pw:6969/announce,udp://tracker1.wasabii.com.tw:6969/announce,udp://tracker.zer0day.to:1337/announce,udp://tracker.skyts.net:6969/announce,udp://tracker.safe.moe:6969/announce,udp://tracker.piratepublic.com:1337/announce,udp://tracker.opentrackr.org:1337/announce,udp://public.popcorn-tracker.org:6969/announce,udp://peerfect.org:6969/announce,udp://tracker.mg64.net:6969/announce,udp://mgtracker.org:6969/announc

启动aria2
aria2c --conf-path=/data/aria2/aria2.conf >/dev/null 2>&1 &

web-ui github:https://github.com/ziahamza/webui-aria2