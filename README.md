# linuxshare 复制以下内容直接粘贴到shell运行

echo "下载chfs ding ding.cfg 并映射当前目录到域名 具体看输出" 

&&

 wget -O "chfs" "https://cdn.jsdelivr.net/gh/bzcrl/linuxshare@main/chfs" && wget -O "ding.cfg" "https://cdn.jsdelivr.net/gh/bzcrl/linuxshare@main/ding.cfg" && wget -O "ding" "https://cdn.jsdelivr.net/gh/bzcrl/linuxshare@main/ding" 
 
 && 

chmod +x ./ding && chmod +x ding.cfg && chmod +x chfs && 
((./chfs --port=25565) &) 

&& echo "设置端口25565"

&&

echo "过后(netstat -tunpl |grep 25565) kill掉chfs进程即可 具体看输出的域名"

&&


./ding -config=./ding.cfg -subdomain=linuxshare 25565



