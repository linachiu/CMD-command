# CMD-command

- 創建 test 資料夾指令:  ```mkdir test```

- 刪除 test資料夾: ```rm -r test ```

- 更改 demo 檔案權限為755: ```chmod 755 demo```

- 更改 test 資料夾與底下資料權限為755: ```chmod -R 755 test```

- 回上層資料夾: ```../``` 

- 查看現在位置: ```pwd```

- 將歷史指令輸出至 hiscmd.txt 檔案中: ```history > hiscmd.txt``` 

- 開機自動執行 echo "hello world" > /Users/xxxxxx/Music/hi.txt

- 排程 crontab -e ,  crontab -l ,  crontab -r 意思


- 用crontab排程 每10秒 送 post request  可以用任何方法 (hint curl + sleep)

```
* * * * * curl -X POST --data "name=LINA&id=123"  https://xxxxxxxx/test/exam.php
* * * * * sleep 10;curl -X POST --data "name=LINA&id=123"  https://xxxxxxxx/test/exam.php
........依此類推
```


- 壓縮資料夾 tar :  ```tar cvf FileName.tar DirName```

- 解壓縮資料夾 : ```tar xvf FileName.tar  有 X 就解壓```

- 遠端連線到 ip:x.x.x.x 帳號centos 連線port為1920 的主機 : ```ssh -p 1920 centos@x.x.x.x```

- 將檔案由本機(資料夾)複製到遠端主機。遠端主機ssh的port為8023
```scp –P 8023 /var/www/html/* admin@ccsh.no-ip.tw:/home/data/```
- 遠端複製資料夾
```scp -r /Users/advmedia/Downloads/school/jtgo_school/ root@192.168.1.99:/hi```

- 格式化硬碟步驟 略

- 掛載硬碟
```
mkdir /mydata
mount /dev/vdb1 /mydata
```

- 卸載
```
umount -v /dev/vdb1
```


- mySQL 備份 demo資料庫  指令 （ 帳號 demo，密碼 123457890 ）
```
mysqldump -u使用者 -e -p密碼 資料庫名稱 > ${dbname}
```
- HOST IDENTIFICATION HAS CHANGED!
```ssh-keygen -R IP```

- CMD游標指令
  - Ctrl-a:移動到指令列最前面 
  - Ctrl-e:移動到指令列最後面 
  - Alt-b:往後跳一個字(在Mac終端機用 Alt-右) 
  - Ctrl-f:往前跳一個字(在Mac終端機用 Alt-左) 
  - Ctrl-u:刪除游標之前所有的字 
  - Ctrl-k:刪除游標之後所有的字 
  - Ctrl-w:刪除前面一個字 
  - Alt-d:刪除後面一個字(在Mac終端機內無法使用)

- 解除鎖定權限
chattr -i /home/wwwroot/你的网站目录/.user.ini

- 路由設定怎麼新增修改網卡資訊為靜態網路後可以成功聯網 （使用以下資訊）

DEVICE=eth0
BOOTPROTO=dhcp
HWADDR=00:0C:29:1D:F0:FE
NM_CONTROLLED=yes
ONBOOT=yes
TYPE=Ethernet


網路資訊
DNS:8.8.8.8 
遮罩:255.255.255.0
路由:192.168.6.1
IPV4: 172.30.156.23

```
DEVICE=eth0
BOOTPROTO=static (原本為dhcp)
HWADDR=00:0C:29:1D:F0:FE
NM_CONTROLLED=yes
ONBOOT=yes
TYPE=Ethernet
DNS1=8.8.8.8
GATEWAY=192.168.6.1
NETMASK=255.255.255.0
IPADDR=172.30.156.23
```
