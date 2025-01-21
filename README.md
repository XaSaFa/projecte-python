# Projecte Python

En aquest projecte utilitzarem el llenguatge de programació Python per a crear pàgines web interactives.

## Tecnologies que utilitzarem

- VirtualBox (Màquines virtuals).
- Python (llenguatge de programació).
- Pycharm (IDE - Entorn de desenvolupament per a Python).
- MariaDB (Base de dades BBDD).
- Jinja2 (llibreria de gestió de plantilles).
- Flask (servidor per a l'aplicació).

## Pas 1 - Creació de la MV

Utilitzarem una MV amb 4GB de RAM, 50GB de disc, 4 CPUs i 128MB de memòria gràfica.

El SO serà Ubuntu 22.04LTS.

## Pas 2 - Instal·lació de Pycharm a Linux

Utilitzem la comanda següent per instal·lar el IDE:

```
sudo snap install pycharm-community --classic
```

## Pas 3 - Instal·lació del gestor de BBDD MariaDB

Utilitzem les següents comandes per instal·lar MariaDB:

```
sudo apt update
sudo apt install mariadb-server
sudo apt-get install libmariadb3 libmariadb-dev
```

