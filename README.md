## tmux installation  
- - - -  

##### 1. Condition  
- Execute with root  


##### 2. Download Tmux
```bash
cd /tmp

yum -y install gcc  ncurses-devel.x86_64

wget -O tmux.tar.gz https://github.com/tmux/tmux/releases/download/2.8/tmux-2.8.tar.gz

sudo tar xvfP tmux.tar.gz
```


###### I got handshake error so I input the tar file to the server  
> wget https://github.com/downloads/libevent/libevent/libevent-2.0.21-stable.tar.gz  
> tar xzvf libevent-2.0.21-stable.tar.gz  
> cd libevent-2.0.21-stable  
> ./configure && make && make install && ldconfig  


##### 3. Tmux complie  
```bash
cd /tmp/tmux-2.8
./configure && make 

```


###### The server already had the library with 5.1.9  
> ln -s /usr/local/lib/libevent-2.0.so.5 /usr/lib64/libevent-2.0.so.5  



##### 4. Move tmux  
```bash
mv tmux  /usr/sbin/
```


##### 5. Config tmux  
```bash
user$> cd ~
user$> git clone https://github.com/inniy2/tmux.git
user$> mv  tmux/.tmux.conf ./
user$> vim .tmux.conf
```
> Edit to linux or OSX  

