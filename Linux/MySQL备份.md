``` bash
/data/backups/mysql

backup.sh


#!/bin/bash


USERNAME="root"
PASSWORD="root"


BACKUP_DIR="/data/backups/mysql"


mysqldump -u $USERNAME -p$PASSWORD --databases szjz > "$BACKUP_DIR/szjz_$(date +%Y%m%d).sql"


crontab -e
crontab -l


0 2 * * * /bin/bash /data/backups/backup.sh
```

参考资料：[MySQL定期备份](https://zhengxiaoping.xyz/fullstack/MySQL%E5%AE%9A%E6%9C%9F%E5%A4%87%E4%BB%BD.html)