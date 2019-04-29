# Automatic local MySQL DB backup

Docker container which runs mysqldump automatically so that you don't loose your changes.

## Usage

* Copy `env-example` to `.env` and make changes as needed.
* Run `docker-compose up --build mysql mysql-backup

This will bring up `mysql` and and `mysql-backup` container. 

The `mysql-backup` container will run a cronjob which will periodically do a mysqldump. All you need to do is make sure you copy the dump file to `MYSQL_DATA_DIRECTORY` from `MYSQL_BACKUP_DIR_LOCATION`.