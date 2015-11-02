# vsftp public

This is a Dockerfile to set up an anonymous FTP server with vsftpd.

Build from docker file:
```
git clone git@github.com:4z3rty/docker-vsftpd-public.git
cd docker-vsftpd-public
docker build -t vsftpd-public .
```

You can also obtain it via:
```
docker pull 4z3rty/vsftpd-public
```

Instructions to run:
```
docker run -d -h HOST -p 20:20 -p 21:21 -p 50000:50100 -v /your/public/directory:/public vsftpd-public
```
or for auto detection to work add --net="host". Though be aware this more insecure and not best practice with docker images.
