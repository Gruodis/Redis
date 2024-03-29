<p align="center"><img width=150 src="https://upload.wikimedia.org/wikipedia/commons/6/64/Logo-redis.svg"></p>

<h1 align="center">Redis with PHP 7.4</h1>


## Install on Ubuntu/Debian

-    Install redis
-    Install appropriate PHP extension
-    Edit .env file


## To Start Redis server:
```bash
redis-server
```

```bash
                _._                                                  
           _.-``__ ''-._                                             
      _.-``    `.  `_.  ''-._           Redis 7.0.5 (00000000/0) 64 bit
  .-`` .-```.  ```\/    _.,_ ''-._                                  
 (    '      ,       .-`  | `,    )     Running in standalone mode
 |`-._`-...-` __...-.``-._|'` _.-'|     Port: 6379
 |    `-._   `._    /     _.-'    |     PID: 11878
  `-._    `-._  `-./  _.-'    _.-'                                   
 |`-._`-._    `-.__.-'    _.-'_.-'|                                  
 |    `-._`-._        _.-'_.-'    |           https://redis.io       
  `-._    `-._`-.__.-'_.-'    _.-'                                   
 |`-._`-._    `-.__.-'    _.-'_.-'|                                  
 |    `-._`-._        _.-'_.-'    |                                  
  `-._    `-._`-.__.-'_.-'    _.-'                                   
      `-._    `-.__.-'    _.-'                                       
          `-._        _.-'                                           
              `-.__.-'                                               

11878:M 26 Nov 2022 01:00:26.785 # Server initialized
```
            
<br>
<br>

> #### Prerequisites
> If you're running a very minimal distribution (such as a Docker container) you may need to install lsb-release first:
> ```bash
> sudo apt install lsb-release
> ```

<br>
<br>

Add the repository to the apt index, update it, and then install:
```bash
curl -fsSL https://packages.redis.io/gpg | sudo gpg --dearmor -o /usr/share/keyrings/redis-archive-keyring.gpg

echo "deb [signed-by=/usr/share/keyrings/redis-archive-keyring.gpg] https://packages.redis.io/deb $(lsb_release -cs) main" | sudo tee /etc/apt/sources.list.d/redis.list

sudo apt-get update
sudo apt-get install redis
```

<br>
<br>

### Confirm Redis version
    redis-cli

<br>


## Create symlink
```bash
sudo systemctl enable redis-server
```

<br>
<br>

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
