>  <sub> _copy and past this comand to terminal_ </sub>
```bash
chmod u+x myfile.txt && ls -ltr myfile.txt
```

#Installing Docker
##On Ubuntu:

1. Update the package index:
>  <sub> _copy and past this comand to terminal_ </sub>
```bash
sudo apt update && sudo apt install docker.io -y
```

2. Start and enable Docker:
>  <sub> _copy and past this comand to terminal_ </sub>
```bash
sudo systemctl start docker && sudo systemctl enable docker
```
3. Add your user to the docker group:
>  <sub> _copy and past this comand to terminal_ </sub>
```bash
sudo usermod -aG docker $USER
```

##On CentOS:

1. Install the epel-release repository and then Docker:
>  <sub> _copy and past this comand to terminal_ </sub>
```bash
sudo yum install epel-release
sudo yum install docker
```

2. Start and enable Docker:
>  <sub> _copy and past this comand to terminal_ </sub>
```bash
sudo systemctl start docker
sudo systemctl enable docker
```

3. Add your user to the docker group:
>  <sub> _copy and past this comand to terminal_ </sub>
```bash
sudo usermod -aG docker $USER
```




