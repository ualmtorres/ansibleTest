# Ejemplos básicos de Ansible

Requisitos previos:

* Es necesario tener instalado Ansible en el nodo controlador.
* Las máquinas controladas sólo tienen que tener Python instalado. 
* Modifica el archivo `hosts.cfg` con los servidores que quieres configurar


## Operaciones básicas


### Comprobar conexión con hosts a configurar

```
ansible -i hosts.cfg -m ping all
```

### Ejecutar un _playbook_

```
ansible-playbook -i hosts.cfg playbookFile.yml
```

### Continuar un _playbook_ que ha fallado

Tras solucionar el error en el _playbook_, usar el nombre de la tarea por la que debe continuar en este comando

```
ansible-playbook -i hosts.cfg playbookFile.yml --start-at-task="nombre de la tarea por la que continuar"
```

## Ejemplos

* [Update && Upgrade](./01actualizar.yml)
* [Crear un directorio y descargar un archivo](./02descargar_logo.yml)
* [Instalación de un paquete](./03instalar_map.yml)
* [Instalación de varios paquetes](./04instalar_varios.yml)
* [Operaciones con archivos (copia, permisos, descomprimir, añadir texto, ...)](./05files.yml)
* [Git](./06git.yml)

