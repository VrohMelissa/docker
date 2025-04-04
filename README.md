# docker
# Installation docker

#  Installer Docker sur Ubuntu (Linux)

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
   echo \"deb [arch=$(dpkg --print-architecture) signed-by=/usr/share/keyrings/docker-archive-keyring.gpg] https://download.docker.com/linux/ubuntu \
  $(lsb_release -cs) stable" | sudo tee /etc/apt/sources.list.d/docker.list > /dev/null

Mettre à jour les informations du dépôt :
  sudo apt-get update
-Installer Docker 
sudo apt-get install docker-ce docker-ce-cli containerd.io
-Vérifier l'installation :
  sudo docker --version

 # Installer Docker sur Windows  

 Télécharger Docker Desktop pour Windows depuis le site officiel :
   https://docs.docker.com/desktop/install/windows-install/
et suivre les instructions pour installation .

![image](https://github.com/user-attachments/assets/8ebe34a6-a337-4ccf-b5ef-6ee36cc8f2aa)


3- Pull une image depuis Docker Hub :
  docker pull <nom_image>

4-Construire une image à partir d'un Dockerfile :
Créer un Dockerfile dans le répertoire de votre projet et ensuite:
  docker build -t <nom_image> 
                  
5-Taguer une image pour Docker Hub :

docker tag <nom_image> <votre_utilisateur>/<nom_image>:<tag>

6-Pousser une image sur Docker Hub :

  docker push <votre_utilisateur>/<nom_image>:<tag>
  
7-Exécuter un conteneur à partir d'une image :

 docker run -d -p <port_hôte>:<port_conteneur> --name <nom_conteneur> <nom_image>:<tag>

1. Créer un Volume
   
docker volume create <nom_volume>

2. Lister les Volumes

docker volume ls

3. Inspecter un Volume

docker volume inspect <nom_volume>

5. Supprimer un Volume

docker volume rm <nom_volume>

6. Supprimer Tous les Volumes Inutilisés

docker volume prune

7. Monter un Volume dans un Conteneur

docker run -d -v <nom_volume>:/chemin/dans/conteneur <image>

docker run -d --mount source=<nom_volume>,target=/chemin/dans/conteneur <image>
