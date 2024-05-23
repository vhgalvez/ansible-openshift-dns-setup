# ansible-dns-cluster-openshift

Este repositorio contiene playbooks de Ansible para configurar el DNS en un clúster de OpenShift. Utiliza FreeIPA como servidor DNS y configura los clientes para usar el servidor DNS de FreeIPA. Adicionalmente, se incluyen pasos para instalar Python en los nodos Flatcar utilizando Docker.

## Estructura del Repositorio

- `ansible.cfg`: Configuración de Ansible.
- `inventory/hosts`: Archivo de inventario con las IPs de las máquinas virtuales.
- `playbooks/install_python_flatcar.yml`: Playbook para instalar Python en nodos Flatcar.
- `playbooks/setup_dns_flatcar.yml`: Playbook para configurar el DNS en nodos Flatcar.
- `playbooks/setup_dns.yml`: Playbook principal para configurar el DNS.
- `roles/dns_config`: Rol de Ansible para configurar DNS.
  - `tasks/main.yml`: Tareas principales del rol.
  - `templates/dns.conf.j2`: Plantilla para la configuración de NetworkManager.
  - `templates/resolv.conf.j2`: Plantilla para la configuración de resolv.conf.

## Uso

1. Clona este repositorio:

   ```bash
   git clone https://github.com/vhgalvez/ansible-openshift-dns-setup.git
   cd ansible-openshift-dns-setup
  ```

2.Configura el archivo de inventario (inventory/hosts) con las IPs de tus máquinas virtuales.

3. Instala Python en los nodos Flatcar usando Docker:


4. Configura el DNS en los nodos Flatcar:

   ```bash
  sudo ansible-playbook -i inventory/hosts playbooks/setup_dns_flatcar.yml
   ```


## Mantenedor

Victor Galvez