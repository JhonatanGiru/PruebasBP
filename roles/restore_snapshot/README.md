
# restore_snapshot: Rol para la ansible collection pichincha.wintel

Este rol automatiza el restablecimiento de un snapshot para una máquina virtual en VMware. 

## Dependencias

  - community.vmware: '>=5.7.0'

## Variables de Rol

| Variable (vars)   | Descripción    | Mandatorio* | Default | Tipo | Opciones |
| ----------------  | ---------- | ---------- | ------- | ---- | -------- |
| `nombre_server` | Nombre de la VM de la que se restaurará el snapshot. | SI | N/A | string | N/A |
| `nombre_snapshot` | Nombre del snapshot a restaurar para la VM. | SI | N/A | string | N/A |
| `restore_snapshot_quiesce` | Especifica si se debe restaurar la memoria de la VM. | NO | false | boolean | false, true |

## Playbook de ejemplo #1

Restaurar el snapshot `snapshot_01_16-07-2025` de la máquina virtual `precdb01`.

```yaml
---
- name: Playbook maestro para restaurar snapshots en VMware.
  hosts: localhost
  gather_facts: false
  roles:
    - role: pichincha.wintel.restore_snapshot
      vars:
        nombre_server: precdb01
        nombre_snapshot: snapshot_01_16-07-2025
```

## Playbook de ejemplo #2

Restaurar el snapshot `snapshot_02_16-07-2025` de la máquina virtual `precdb02`, incluyendo la data en memoria.

```yaml
---
- name: Playbook maestro para restaurar snapshots en VMware.
  hosts: localhost
  gather_facts: false
  roles:
    - role: pichincha.wintel.restore_snapshot
      vars:
        nombre_server: precdb02
        nombre_snapshot: snapshot_02_16-07-2025
        create_snapshot_quiesce: true
```
