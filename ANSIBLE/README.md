# Deployer avec Ansible

**prerequis** : 

- disposer d'un serveur avec tomcat installé
- disposer d'un serveur mysql installé
- disposer du war à déployer (un exemplaire est disponible dans le repertoire courant pour eviter le build)

**Taches**:

- créer un fichier host en s'inspirant du host.template
- vérifier et éventuellement modifier le fichier ansible.cfg (remote_user par exemple)
- executer le playbook deploy.yaml