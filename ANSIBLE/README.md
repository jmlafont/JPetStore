# Deployer JpetStore avec Ansible

**Taches**:

- installer les roles indiqués dans roles/requirements.yml 

```
ansible-galaxy role install tomcat-install mysql-install -r roles/requirements.yml -p roles
```

- modifier le fichier hosts en fonction de l'environnement cible
- vérifier et éventuellement modifier le fichier ansible.cfg (remote_user par exemple)
- executer le playbook deploy.yaml
- vérifier en accédant à http://<host-cible>/jpetstore
