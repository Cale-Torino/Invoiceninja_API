## INSTALL STEPS

### 1. SSH into the linux disto (buster)

```
mkdir apisource

ls public_html/apisource
```

### 2. run to create initial project
installs fusio to `apisource` dir.
```
composer create-project fusio/fusio public_html/apisource
```

### 3. Now copy files to dir via filezilla or run command below

```
composer create-project fusio/fusio
```
if you copied files via filezilla it may fail when trying to install the backed just ignore and install manualy.

see [this question]() for more info

### 4. If you need to install manualy [fusio,developer etc]
run in root dir on ssh instance to install fusio app
```
php bin/fusio marketplace:install fusio
```

run in root dir on ssh instance to install developer app
```
php bin/fusio marketplace:install developer
```

del all files and folders in dir
```
rm -r public_html/apisource/*
```

---