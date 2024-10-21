# Configure nginx via ansible

```bash
ansible-playbook -i nginx_hosts.yml nginx.yml
```

# or copy via ad-hoc command

```bash
ansible -i nginx_hosts.yml -m copy -a "src=nginx.conf dest=/etc/nginx/nginx.conf" nginx_hosts
```