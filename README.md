# docker
Installation docker

1. Installer Docker sur Ubuntu (Linux)

Prérequis
-Système Ubuntu 18.04 ou supérieur.
-Compte utilisateur avec des privilèges sudo.

Étapes d'installation
  -Mettre à jour votre système :
  sudo apt-get update

 -Installer les paquets requis :
  sudo apt-get install \
  apt-transport-https \
  ca-certificates \
  curl \
  software-properties-common

 -Ajouter la clé GPG officielle de Docker :
  curl -fsSL https://download.docker.com/linux/ubuntu/gpg | sudo gpg --dearmor -o /usr/share/keyrings/docker-archive-keyring.gpg

  -Ajouter le dépôt Docker :
   echo \
  "deb [arch=$(dpkg --print-architecture) signed-by=/usr/share/keyrings/docker-archive-keyring.gpg] https://download.docker.com/linux/ubuntu \
  $(lsb_release -cs) stable" | sudo tee /etc/apt/sources.list.d/docker.list > /dev/null

Mettre à jour les informations du dépôt :
  sudo apt-get update
-Installer Docker 
sudo apt-get install docker-ce docker-ce-cli containerd.io
-Vérifier l'installation :
  sudo docker --version

 Installer Docker sur Windows  

 Télécharger Docker Desktop pour Windows depuis le site officiel :
   https://docs.docker.com/desktop/install/windows-install/
et suivre les instructions pour installation .
![image](https://github.com/user-attachments/assets/8ebe34a6-a337-4ccf-b5ef-6ee36cc8f2aa)



