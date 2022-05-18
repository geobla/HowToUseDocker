# Docker Commands.

### docker run

```bash
docker run <imageName>
```

This will run the selected image. &#x20;

If the image is not inside the server, it will go to the docker hub, download, and then run it.&#x20;

but this is only done the first time. After the first time it will use your downloaded image.   &#x20;

For example:&#x20;

![](../.gitbook/assets/GetImage\(2\).png)

### docker ps

```bash
docker ps
```

Lists all running containers and some basic info about them.&#x20;

Each container gets a random ID and name assigned to it.

![](../.gitbook/assets/GetImage\(3\).png)

### docker ps –a

```bash
docker ps –a
```

If we use this command, we will also get the previous terminated containers.

![](../.gitbook/assets/GetImage\(4\).png)

### Stop a container from running.

To stop a container from running we use the command:

```bash
docker stop <name> 
```

We confirm with **Status** must be **Exited.**

![](../.gitbook/assets/GetImage\(5\).png)
