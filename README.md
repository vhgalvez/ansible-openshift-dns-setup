# ansible-dns-cluster-openshift

Este repositorio contiene playbooks de Ansible para configurar el DNS en un clúster de OpenShift. Utiliza FreeIPA como servidor DNS y configura los clientes para usar el servidor DNS de FreeIPA.

## Estructura del Repositorio

- `ansible.cfg`: Configuración de Ansible.
- `inventory/hosts`: Archivo de inventario con las IPs de las máquinas virtuales.
- `playbooks/setup_dns.yml`: Playbook principal para configurar el DNS.
- `roles/dns_config`: Rol de Ansible para configurar DNS.
  - `tasks/main.yml`: Tareas principales del rol.
  - `templates/dns.conf.j2`: Plantilla para la configuración de NetworkManager.
  - `templates/resolv.conf.j2`: Plantilla para la configuración de resolv.conf.

## Uso

1. Clona este repositorio.
2. Configura el archivo de inventario (`inventory/hosts`) con las IPs de tus máquinas virtuales.
3. Ejecuta el playbook de Ansible:

   ```bash
   ansible-playbook playbooks/setup_dns.yml
   ```

## Requisitos

- Ansible instalado en la máquina de administración.

- Acceso SSH a las máquinas virtuales con la clave privada configurada.

## Mantenedor

Victor Galvez