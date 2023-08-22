# Installing Docker
## On Ubuntu:

1. Update the apt package index and install packages to allow apt to use a repository over HTTPS:
>  <sub> _copy and past this comand to terminal_ </sub>
```bash
sudo apt update && sudo sudo apt-get install ca-certificates curl gnupg
```

2. Add Docker’s official GPG key:
>  <sub> _copy and past this comand to terminal_ </sub>
```bash
sudo install -m 0755 -d /etc/apt/keyrings
curl -fsSL https://download.docker.com/linux/ubuntu/gpg | sudo gpg --dearmor -o /etc/apt/keyrings/docker.gpg
sudo chmod a+r /etc/apt/keyrings/docker.gpg
```
3. Use the following command to set up the repository:
>  <sub> _copy and past this comand to terminal_ </sub>
```bash
echo \
  "deb [arch="$(dpkg --print-architecture)" signed-by=/etc/apt/keyrings/docker.gpg] https://download.docker.com/linux/ubuntu \
  "$(. /etc/os-release && echo "$VERSION_CODENAME")" stable" | \
  sudo tee /etc/apt/sources.list.d/docker.list > /dev/null
```

4. Update the apt package index:
>  <sub> _copy and past this comand to terminal_ </sub>
```bash
sudo apt-get update
```

5. Install Docker Engine, containerd, and Docker Compose:
>  <sub> _copy and past this comand to terminal_ </sub>
```bash
sudo apt-get install docker-ce docker-ce-cli containerd.io docker-buildx-plugin docker-compose-plugin
```

6. Verify that the Docker Engine installation is successful by running the hello-world image:
>  <sub> _copy and past this comand to terminal_ </sub>
```bash
sudo docker run hello-world
```

## On CentOS:

1. Install the yum-utils package (which provides the yum-config-manager utility) and set up the repository:
>  <sub> _copy and past this comand to terminal_ </sub>
```bash
sudo yum install -y yum-utils
sudo yum-config-manager --add-repo https://download.docker.com/linux/centos/docker-ce.repo
```

2. Install Docker Engine, containerd, and Docker Compose:
>  <sub> _copy and past this comand to terminal_ </sub>
```bash
sudo yum install docker-ce docker-ce-cli containerd.io docker-buildx-plugin docker-compose-plugin
```

3. Start Docker:
>  <sub> _copy and past this comand to terminal_ </sub>
```bash
sudo systemctl start docker
```

4. Verify that the Docker Engine installation is successful by running the hello-world image:
>  <sub> _copy and past this comand to terminal_ </sub>
```bash
sudo docker run hello-world
```


# Installing Jenkins
## On Ubuntu:

1. Install Java:
>  <sub> _copy and past this comand to terminal_ </sub>
```bash
sudo apt-get update
sudo apt install openjdk-11-jdk
java --version
```

2. Add Jenkins repository:
>  <sub> _copy and past this comand to terminal_ </sub>
```bash
curl -fsSL https://pkg.jenkins.io/debian-stable/jenkins.io-2023.key | sudo tee /usr/share/keyrings/jenkins-keyring.asc > /dev/null
echo deb [signed-by=/usr/share/keyrings/jenkins-keyring.asc]  https://pkg.jenkins.io/debian-stable binary/ | sudo tee /etc/apt/sources.list.d/jenkins.list > /dev/null
sudo apt update
```

3. Install Jenkins:
>  <sub> _copy and past this comand to terminal_ </sub>
```bash
sudo apt install jenkins
```

4. Start Jenkins:
>  <sub> _copy and past this comand to terminal_ </sub>
```bash
sudo systemctl start jenkins
sudo systemctl status jenkins
```

5. Configure firewall:
>  <sub> _copy and past this comand to terminal_ </sub>
```bash
sudo ufw allow 8080
sudo ufw allow ssh
sudo ufw enable
sudo ufw status
```

6. Set up Jenkins:
To set up Jenkins, go to your browser and open http://localhost:8080 where Jenkins server is running.

The Unlock Jenkins screen will appear as shown below, asking for the administrator password.
By default, you will be given a 32-character alphanumeric initial admin password to login into Jenkins dashboard. Later, you can create an admin user and password.

Open a new tab in the terminal and run the command below to get the initial credential to unlock Jenkins.
>  <sub> _copy and past this comand to terminal_ </sub>
```bash
sudo cat /var/lib/jenkins/secrets/initialAdminPassword
```

Now copy and paste this password on the “Unlock Jenkins” page in the browser and click on continue.
Next, you need to customize Jenkins and install plugins. You can either select plugins of your choice or install suggested plugins, which are the most widely used plugins by the community.

## On CentOS:

1. Install Java:
>  <sub> _copy and past this comand to terminal_ </sub>
```bash
sudo yum install java-11-openjdk-devel
java --version
```

2. Add Jenkins repository:
>  <sub> _copy and past this comand to terminal_ </sub>
```bash
sudo wget -O /etc/yum.repos.d/jenkins.repo https://pkg.jenkins.io/redhat-stable/jenkins.repo
sudo rpm --import https://pkg.jenkins.io/redhat-stable/jenkins.io.key
sudo yum update
```

3. Install Jenkins:
>  <sub> _copy and past this comand to terminal_ </sub>
```bash
sudo yum install jenkins
```

4. Start Jenkins:
>  <sub> _copy and past this comand to terminal_ </sub>
```bash
sudo systemctl start jenkins
sudo systemctl status jenkins
```

5. Configure firewall:
>  <sub> _copy and past this comand to terminal_ </sub>
```bash
sudo firewall-cmd --zone=public --permanent --add-port=8080/tcp
sudo firewall-cmd --zone=public --permanent --add-service=ssh
sudo firewall-cmd --reload
sudo firewall-cmd --list-all
```

6. Set up Jenkins:
To set up Jenkins, go to your browser and open http://localhost:8080 where Jenkins server is running.

The Unlock Jenkins screen will appear as shown below, asking for the administrator password.
By default, you will be given a 32-character alphanumeric initial admin password to login into Jenkins dashboard. Later, you can create an admin user and password.

Open a new tab in the terminal and run the command below to get the initial credential to unlock Jenkins.
>  <sub> _copy and past this comand to terminal_ </sub>
```bash
sudo cat /var/lib/jenkins/secrets/initialAdminPassword
```

Now copy and paste this password on the “Unlock Jenkins” page in the browser and click on continue.
Next, you need to customize Jenkins and install plugins. You can either select plugins of your choice or install suggested plugins, which are the most widely used plugins by the community.
