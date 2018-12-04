# Docker MySQL-Backup

A tool to automatically dump running [MySQL](https://www.mysql.com/) and [MariaDB](https://mariadb.org/) databases in Docker containers.

## Installation

### Manual from GitHub

Clone the [Docker MySQL-Backup repository:](https://github.com/binfalse/docker-mysql-backup)

    git clone https://github.com/kibach/docker-mysql-backup.git

Copy the [backup script](etc/cron.daily/docker-mysql-backup) to the `cron.daily` (most likely `/etc/cron.daily/`) directory on your system:

    cp docker-mysql-backup/etc/cron.daily/docker-mysql-backup /etc/cron.daily/docker-mysql-backup

Copy the [configuration](etc/default/docker-mysql-backup) to `/etc/default/`:

    cp docker-mysql-backup/etc/default/docker-mysql-backup /etc/default/docker-mysql-backup

## How does that work?

You'll find [the detailed information on the Docker MySQL-Backup tool in the original binfalse's blog article.](https://binfalse.de/2017/02/06/docker-mysql-backup/)

This version of the tool relies on `MYSQL_USER` and `MYSQL_PASSWORD` environment variables instead of `MYSQL_ROOT_PASSWORD`, which is useful when `MYSQL_RANDOM_ROOT_PASSWORD=1` is used.

## Licence

    Docker MySQL-Backup - backup of running MySQL containers
    Copyright (C) 2016-2017 Martin Scharm <https://binfalse.de/contact/>
    
    This program is free software: you can redistribute it and/or modify
    it under the terms of the GNU General Public License as published by
    the Free Software Foundation, either version 3 of the License, or
    (at your option) any later version.
    
    This program is distributed in the hope that it will be useful,
    but WITHOUT ANY WARRANTY; without even the implied warranty of
    MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE.  See the
    GNU General Public License for more details.
    
    You should have received a copy of the GNU General Public License
    along with this program.  If not, see <http://www.gnu.org/licenses/>.

