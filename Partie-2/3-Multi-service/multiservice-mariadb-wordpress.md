# Multi service

Pour faire le lien entre Wordpress et MariaDB il faut dans le fichier docker-compose :

préciser les infos de la bdd dans wordpress avec

```
environment:
      WORDPRESS_DB_HOST: mariadb
      WORDPRESS_DB_USER: wordpress
      WORDPRESS_DB_PASSWORD: mypass
      WORDPRESS_DB_NAME: wordpress
```

préciser que mariadb doit fonctionner avant wordpress avec

```
depends_on:
      - mariadb
```

et dans mariadb il faut préciser les infos de la même manière

```
environment:
      MYSQL_ROOT_PASSWORD: root
      MYSQL_DATABASE: wordpress
      MYSQL_USER: wordpress
      MYSQL_PASSWORD: mypass
```

et ensuite créer un réseau avec

```
networks:
  network-wp-mdb:
    driver: bridge
```

je le mets dans wordpress et mariadb

```
networks:
      - network-wp-mdb
```

et pour mariadb je crée un volume avec

```
volumes:
  mariadb_wordpress_data:
    driver: local
```

que je précise

```
volumes:
      - mariadb_wordpress_data:/var/lib/mysql
```
