# PostgreSQL Setup Sccripts

Setup PostgreSQL on Ubuntu

## Install PostgreSQL

```
sudo apt install postgresql postgresql-contrib
```

## Use it

```
sudo -i -u postgres
psql
```

## Create a User

```
sudo -u postgres createuser --interactive
```

Output

```
Enter name of role to add: sammy
Shall the new role be a superuser? (y/n) y
```

Create DB for user

```
sudo -u postgres createdb sammy
```

Set password for User

```
ALTER USER sammy PASSWORD 'newpassword';
```

## Backup and Restore

SQL Dump

```
pg_dump dbname > outfile
```

Restore Dump

```
psql dbname < infile
```

**Important Options**

```
pg_dump dbname -U potgres -p 5432 > outfile
```

- `-U xxx`: Specifies potgres user account to use

- `-p xxx`: Specifies the port number