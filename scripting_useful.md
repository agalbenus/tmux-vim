grep --include={*.php,*.html,*.js} -rnl './' -e "old-word" | xargs -i@ sed -i 's/old-word/new-word/g' @

-------------------
Error : `An error occurred trying to connect: Get http://hsotname:2375/v1.23/containers/json: read tcp 127.0.0.1:58704->127.0.1.1:2375: read: connection reset by peer`

Fix : 
```
sudo service docker stop
sudo rm /var/lib/docker/network/files/local-kv.db
sudo service docker start
```
https://learnxinyminutes.com/docs/bash/
