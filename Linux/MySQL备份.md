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