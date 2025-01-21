# Instal·lació de l'entorn

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

## Pas 4 - Instal·lació del gestor d'instal·lació de llibreries pip

```
sudo apt install python3-pip
```

## Pas 5.- Instal·lació de llibreria per controlar BBDD MySQL (MariaDB) des de Python

```
pip install mariadb
pip install Flask
```

## Pas 6.- Crear nou projecte a Pycharm

![image](https://github.com/user-attachments/assets/05ce34cb-174c-416a-b21e-29b8393f14f8)

![image](https://github.com/user-attachments/assets/3eaa6171-96bc-4a36-901b-38d8adf2d133)

![image](https://github.com/user-attachments/assets/be44706a-f5df-4727-9040-82992ed8bb1d)

![image](https://github.com/user-attachments/assets/07bc27bf-66db-450e-a5f0-a083006eaba3)



