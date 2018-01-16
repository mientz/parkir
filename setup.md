# Parkir Management App Setup

## prerequisite
1. Nodejs
2. PM2 node module
3. http-master node module

### PM2
1. install pm2 `npm install -g pm2`
   * (optional) pm2 keymetric monitoring app.keymetrics.io[keymetrics](https://app.keymetrics.io/)
2. run pm2 as serivices `pm2 startup`
3. save proccess list `pm2 save`

### HTTP-MASTER
1. install http-master `mpm install -g http-master --unsafe-perm`
2. run http-master `http-master --config /root/parkir/http-master.conf`
   * run http-master as services with pm2
	```Shell
	pm2 start /usr/bin/http-master -x --name "http-master" -- --workers 0 --config /root/parkir/http-master.conf
	pm2 save
	```
	
