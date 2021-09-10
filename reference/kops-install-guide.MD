Kubernetes cmd:

sudo su -i 

sudo apt-get update -y 
sudo apt-get install unzip -y 

# install aws cli

curl "https://awscli.amazonaws.com/awscli-exe-linux-x86_64.zip" -o "awscliv2.zip"
unzip awscliv2.zip
sudo ./aws/install

aws --version 


----------------------------------
# install kube ctl 

sudo curl -fsSLo /usr/share/keyrings/kubernetes-archive-keyring.gpg https://packages.cloud.google.com/apt/doc/apt-key.gpg
curl -LO https://storage.googleapis.com/kubernetes-release/release/$(curl -s https://storage.googleapis.com/kubernetes-release/release/stable.txt)/bin/linux/amd64/kubectl
chmod +x ./kubectl
sudo mv ./kubectl /usr/local/bin/kubectl

Options 2 - Valid

curl -LO "https://dl.k8s.io/release/$(curl -L -s https://dl.k8s.io/release/stable.txt)/bin/linux/amd64/kubectl"

---> Optional
	chmod +x kubectl
	mkdir -p ~/.local/bin/kubectl
	mv ./kubectl ~/.local/bin/kubectl


sudo install -o root -g root -m 0755 kubectl /usr/local/bin/kubectl
-----------------------------------

----------------------------------
# install kubernetes operations

curl -Lo kops https://github.com/kubernetes/kops/releases/download/$(curl -s https://api.github.com/repos/kubernetes/kops/releases/latest | grep tag_name | cut -d '"' -f 4)/kops-linux-amd64
chmod +x kops
sudo mv kops /usr/local/bin/kops

Optional
curl -LO  https://github.com/kubernetes/kops/releases/download/1.15.0/kops-linux-amd64
chmod +x kops-linux-amd64
sudo mv kops-linux-amd64 /usr/local/bin/kops
kops version
 
 --------------------------------

