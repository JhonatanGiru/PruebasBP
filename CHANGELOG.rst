================================
pichincha.wintel Release Notes
================================

v1.0.7
======

- Agregados roles para gestión de snapshots en VMware: create_snapshot, obtain_snapshots y restore_snapshot.

v1.0.6
======

- Moviendo la pausa de readiness_dynatrace.yml a main.yml.

v1.0.5
======

- Corrigiendo lista de autores en galaxy.yml.

v1.0.4
======

- Corrigiendo nombre de variable app_urls_list en main.yml de iniciar en bloque pausa.
- Corrigiendo unos cuantos horrores ortográficos más en el README.md y en tareas de los roles.

v1.0.3
======

- Corrigiendo nombre de variable app_urls_list en main.yml de iniciar.
- Corrigiendo horrores ortográficos en el README.md y en tareas de los roles.

v1.0.2
======

- Agregando funcionalidad para la elección del mode de inicio del servicio 'start_mode', para inciar_servicios.yml.
- Agregando funcionalidad para la pausa entre inicio de servicios 'wait_time', para iniciar_servicios.yml.

v1.0.1
======

- Corrigiendo error en validación de la lista app_pools_list en rol 'iniciar' en main.yml.

v1.0.0 (24/04/2025)
===================

Release Summary
---------------

- Esta es la primera versión Estable de la colección ``pichincha.wintel``.


Nuevos Roles
------------

- ``readiness``: Rol para el monitoreo y readiness en dynatrace para plataformas Windos/Wintel.
- ``detener``: Rol para detener IIS, Application pools y servicios en plataformas Windows/Wintel.
- ``iniciar``: Rol para iniciar IIS, Application pools y servicios en plataformas Windows/Wintel.
