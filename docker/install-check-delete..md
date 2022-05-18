# Install / Check / Delete.

### Check and delete any previous versions.

Uninstall any older version if existing in your server:

```bash
sudo apt remove docker docker-engine docker.io containerd runc 
```

### Installation.

#### Docker Website.

If on Linux, go to [https://docs.docker.com/engine/install/ubuntu/](https://docs.docker.com/engine/install/ubuntu/) &#x20;

And then check the prerequisites of version compatibility.

#### Select the 2nd method (convenience script).

This example downloads the script from [get.docker.com](https://get.docker.com/) and runs it to install the latest stable release of Docker on Linux:&#x20;

```bash
curl -fsSL https://get.docker.com -o get-docker.sh
sudo sh get-docker.sh 
```

Check docker version:

```bash
sudo docker version
```

To double-check if everything installed correctly, go to [https://hub.docker.com/r/docker/whalesay](https://hub.docker.com/r/docker/whalesay) , &#x20;

and copy the docker run command from inside the script:  (add sudo in the beginning).&#x20;

![](<../.gitbook/assets/GetImage (1).png>)

Or just copy-paste this code in your server terminal:

```bash
sudo docker run docker/whalesay cowsay boo 
```

With this command, docker will pull the image from the hub repo, and run it.

This is the result you should get:

![](../.gitbook/assets/GetImage\(1\).png)

### Upgrade Docker after using the convenience script

If you installed Docker using the convenience script, you should upgrade Docker using your package manager directly. &#x20;

There is no advantage to re-running the convenience script, and it can cause issues if it attempts to re-add repositories which have already been added to the host machine.&#x20;

### Uninstall Docker Engine.

1. Uninstall the Docker Engine, CLI, Containerd, and Docker Compose packages:

```bash
sudo apt-get purge docker-ce docker-ce-cli containerd.io docker-compose-plugin
```

2\. Images, containers, volumes, or customized configuration files on your host are not automatically removed. To delete all images, containers, and volumes:&#x20;

```bash
sudo rm -rf /var/lib/docker
sudo rm -rf /var/lib/containerd
```

3\. You must delete any edited configuration files manually.&#x20;
