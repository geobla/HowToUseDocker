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

### Remove a Container.

Use the command&#x20;

```bash
docker rm <name> 
```

If we get the name back, we are OK.&#x20;

Running afterwards the &#x20;

```bash
docker ps –a 
```

We should not see it at all.&#x20;

![](../.gitbook/assets/GetImage\(6\).png)

* But the rm command <mark style="color:red;">does not remove</mark> the image nor any remaining docker files and folders.&#x20;

### List docker images & Remove unused.

Use the &#x20;

```bash
docker images 
```

command to get the images list on your server.&#x20;

![](../.gitbook/assets/GetImage.jpeg)

To remove an image run:

```bash
docker rmi <imageName>
```

![](../.gitbook/assets/GetImage\(1\).jpeg)

* <mark style="color:red;">IMPORTANT!!</mark>&#x20;

Remove all depended containers <mark style="color:red;">BEFORE</mark> removing the image!! (Check previous step).

### ONLY download image and DO NOT run.

If we **ONLY** want to download the image but **NOT RUN** the container at the same time we use the command:

```bash
docker pull <imageName>
```

![](../.gitbook/assets/GetImage\(2\).jpeg)

