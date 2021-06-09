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