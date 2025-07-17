
# create_snapshot: Rol para la ansible collection pichincha.wintel

Este rol automatiza la creación del snapshot de una máquina virtual en VMware. 

## Dependencias

  - community.vmware: '>=5.7.0'

## Variables de Rol

| Variable (vars)   | Descripción    | Mandatorio* | Default | Tipo | Opciones |
| ----------------  | ---------- | ---------- | ------- | ---- | -------- |
| `nombre_server` | Nombre de la VM de la que se creará el snapshot. | SI | N/A | string | N/A |
| `create_snapshot_quiesce` | Especifica si se debe almacenar la memoria de la VM. | NO | false | boolean | false, true |

## Playbook de ejemplo #1

Crear snapshot de la máquina virtual `precdb01`.

```yaml
---
- name: Playbook maestro para crear snapshots en VMware.
  hosts: localhost
  gather_facts: false
  roles:
    - role: pichincha.wintel.create_snapshot
      vars:
        nombre_server: precdb01
```

## Playbook de ejemplo #2

Crear snapshot de la máquina virtual `precdb02`, incluyendo la data en memoria.

```yaml
---
- name: Playbook maestro para crear snapshots en VMware.
  hosts: localhost
  gather_facts: false
  roles:
    - role: pichincha.wintel.create_snapshot
      vars:
        nombre_server: precdb01
        create_snapshot_quiesce: true
```
