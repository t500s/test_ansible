### Test Ansible

#### Setup in docker

Add private key for user to `.docker/.ssh`
Add ansible-vault password to `.vault_pass`
```
cd .docker
docker-compose up -d
docker exec -it test_sobes_ansible bash
```

#### Setup on host

Optionally create [venv](https://docs.python.org/3/library/venv.html)
`pip install -r requirements.txt`

#### Run playbook

```
ansible-playbook -i inventory/inventory.yml -l test playbooks/bootstrap.yml -u ubuntu --private-key=path/to/key --diff
``