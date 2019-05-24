# Ansible-create-module-role

Usage of a role for setting a git_key encrypted with Ansible Vault. 

Go to  module/defaults/
Type

```ansible-vault encrypt  main.yml``` 

enter a secret password.
 
and save it in a file located in the home directory.

```vi /home/<home_directory>/mysecret``` 
 
You can run the playbook with the following command. 

```ansible-playbook -i inventory --vault-password-file /home/hme/mysecret playbook.yml``` 
 
or declare a global environment variable beforehand or it should be placed in your .bash_profile file.

```export  ANSIBLE_VAULT_PASSWORD_FILE=/home/hme/mysecret```

and type the playbook as the normal way 

```ansible-playbook -i inventory playbook.yml``` 
