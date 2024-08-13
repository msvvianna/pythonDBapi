## 12/08/2024 – REVISÃO PYTHON DB API – DAY 1

### 5504. APRESENTAÇÃO

- Iremos ver nesse módulo a configuração do DB API.

### 5505. CRIANDO UM OBJETO CONNECTION

```bash
└─[$] <> mysql -u root -pAllstar@3
Welcome to the MariaDB monitor.  Commands end with ; or \g.
Your MariaDB connection id is 31
Server version: 10.11.6-MariaDB-0+deb12u1 Debian 12

Copyright (c) 2000, 2018, Oracle, MariaDB Corporation Ab and others.

Type 'help;' or '\h' for help. Type '\c' to clear the current input statement.

MariaDB [(none)]> create database treinaweb_clientes;
Query OK, 1 row affected (0,008 sec)

MariaDB [(none)]> use treinaweb_clientes;
Database changed
MariaDB [treinaweb_clientes]> show tables;
Empty set (0,001 sec)

MariaDB [treinaweb_clientes]>

```

```python
import MySQLdb

MySQLdb.connect(user="root", passwd="Allstar@3", db="treinaweb_clientes", host="localhost", port=3306)

print("Conexão realizada com sucesso!")

```

## 13/08/2024 – REVISÃO PYTHON DB API – DAY 2

### 5506. ABRINDO E FECHANDO CONEXÕES

```python
import MySQLdb

db = MySQLdb.connect(user="root", passwd="Allstar@3", db="treinaweb_clientes", host="localhost", port=3306)

print("Conexão realizada com sucesso!")

db.close()

```
