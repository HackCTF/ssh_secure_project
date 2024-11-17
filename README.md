# SSH Secure Project

Este proyecto configura servidores con:
- Port Knocking para SSH.
- Puerto SSH personalizado.
- Refuerzo de seguridad en SSH.

## Uso

1. Instalar Ansible:
```bash
sudo dnf install ansible -y
```

Ejecutar el playbook:

```bash
Copiar código
ansible-playbook playbooks/ssh_security.yml
```

Verificar la configuración
```bash
for port in 1234 5678 9012; do nc -zv <server_ip> $port; done
ssh -p 2223 <user>@<server_ip>
