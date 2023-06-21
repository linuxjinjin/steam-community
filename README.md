# steam-community
steam community 302 linux
Centos:
cp steamcommunityCA.pem /etc/pki/ca-trust/source/anchors
运行/bin/update-ca-trust
Ubuntu:
cp steamcommunityCA.pem /usr/local/share/ca-certificates
运行update-ca-certificates
#赋予caddy执行权限
chmod +x caddy
#启动
./caddy run --config steamcommunity_302.caddy.json --adapter caddyfile
