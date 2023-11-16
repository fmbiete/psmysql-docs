# Clean up

## Exit and remove the container and image

To exit the MySQL command client shell, you can also use the `\q` or `quit` commands. There are other ways to exit a MySQL command client shell, such as using `Ctrl+C`.

To exit a docker container, you can use the command `exit` or `Ctrl+D`. There are other ways to exit a docker container, such as using `docker stop` followed by the container ID or name.

You may want to remove the docker container and the image if they are no longer needed or to free up disk space. To remove a docker container, use the command `docker rm` followed by `psmysql`, the container ID or name. To remove a docker image, use the command `docker rmi` followed by `percona/percona-server`, the image ID or name.

## What to do

This code exits the mysql command line client program and the container.

```{.bash data-prompt="mysql>"}
mysql> exit
```

This code removes the container and removes the image.

```{.bash data-prompt="$"}
$ docker container rm psmysql
$ docker rmi percona/percona-server
```

This code removes the docker volume. If a container uses the volume, you cannot remove it.

```{.bash data-prompt="$"}
$ docker volume rm myvol
```

## Next steps

[Next steps :material-arrow-right:](quickstart-next-steps.md){.md-button}