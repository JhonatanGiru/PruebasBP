
# obtain_snapshots: Rol para la ansible collection pichincha.wintel

Este rol lista todos los snapshots generados para una máquina virtual en VMware. 

## Dependencias

  - community.vmware: '>=5.7.0'

## Variables de Rol

| Variable (vars)   | Descripción    | Mandatorio* | Default | Tipo | Opciones |
| ----------------  | ---------- | ---------- | ------- | ---- | -------- |
| `nombre_server` | Nombre de la VM de la que se listarán los snapshots creados. | SI | N/A | string | N/A |

## Playbook de ejemplo #1

Obtener snapshots de la máquina virtual `precdb01`.

```yaml
---
- name: Playbook maestro para obtener snapshots en VMware.
  hosts: localhost
  gather_facts: false
  roles:
    - role: pichincha.wintel.obtain_snapshots
      vars:
        nombre_server: precdb01
```
