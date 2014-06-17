mysql plugin for octohost
=====================

Setup the correct access variables in `/usr/local/octohost/plugins/mysql/env`

Once that's done, here's how to use it:

```
# This creates the user and database and adds the result
# to the octohost env variable store.
root@octohost:~# octo mysql:create andy_test
Creating user and database for 'andy_test' container.
/andy_test/MYSQL_USERNAME:andy_test
/andy_test/MYSQL_PASSWORD:the-password-shows-up-here
/andy_test/MYSQL_DATABASE:andy_test
/andy_test/MYSQL_HOSTNAME:10.xxx.xxx.xxx
# Now let's show the environment vars that octohost knows about.
root@octohost:~# octo config andy_test
/andy_test/MYSQL_USERNAME:andy_test
/andy_test/MYSQL_PASSWORD:the-password-shows-up-here
/andy_test/MYSQL_DATABASE:andy_test
/andy_test/MYSQL_HOSTNAME:10.xxx.xxx.xxx
root@octohost:~# octo mysql:delete andy_test
root@octohost:~#
```

That's it.
