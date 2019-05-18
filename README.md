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
