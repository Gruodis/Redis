<p align="center"><img width=150 src="https://upload.wikimedia.org/wikipedia/commons/6/64/Logo-redis.svg"></p>

<h1 align="center">Redis with PHP 7.4</h1>

## Install on Ubuntu/Debian

-    Install redis
    - Install appropriate PHP extension
    - Edit .env file

***

> #### Prerequisites
> If you're running a very minimal distribution (such as a Docker container) you may need to install lsb-release first:
> ```bash
> sudo apt install lsb-release
> ```

Add the repository to the apt index, update it, and then install:
```bash
curl -fsSL https://packages.redis.io/gpg | sudo gpg --dearmor -o /usr/share/keyrings/redis-archive-keyring.gpg

echo "deb [signed-by=/usr/share/keyrings/redis-archive-keyring.gpg] https://packages.redis.io/deb $(lsb_release -cs) main" | sudo tee /etc/apt/sources.list.d/redis.list

sudo apt-get update
sudo apt-get install redis
```
## Install Redis PHP extension:
Extension for **PHP 7.4**
```bash
sudo apt-get install php7.4-redis
```
Extension for **latest PHP** versnion
```bash
sudo apt-get install php-redis
```


## Edit .env file

CACHE_DRIVER=redis
