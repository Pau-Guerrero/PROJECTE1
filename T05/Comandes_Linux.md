## 🎯 Activitat

**AA2 — Repàs de comandes Linux**

Realització d’exercicis en una màquina virtual GNU/Linux utilitzant el terminal.

***

# 📂 Bloc 1: Sistema de fitxers

### 🔹 Llistar fitxers de `/home`

```bash
ls -la /home
```
![](img/1.png)
***

### 🔹 Copiar `/etc/passwd` al directori personal com `users.txt`

```bash
cp /etc/passwd ~/users.txt
```
![](img/2.png)
***

### 🔹 Moure `users.txt` a una carpeta `documents` (crear si no existeix)

```bash
mkdir -p ~/documents
mv ~/users.txt ~/documents/
```
![](img/3.png)
***

### 🔹 Esborrar `users.txt`

```bash
rm ~/documents/users.txt
```
![](img/4.png)
***

### 🔹 Crear tres carpetes amb una sola comanda

```bash
mkdir ~/proves ~/proves2 ~/proves3
```
![](img/5.png)
***

# 👥 Bloc 2: Usuaris i grups

### 🔹 Crear usuaris `prova1` i `prova2`

```bash
sudo useradd -m -s /bin/bash prova1
sudo useradd -m -s /bin/bash prova2
```
![](img/6.png)
***

### 🔹 Crear grup `alumnes`

```bash
sudo groupadd alumnes
```
![](img/7.png)
***

### 🔹 Afegir `prova1` a `alumnes` i a sudo

```bash
sudo usermod -aG alumnes prova1
sudo usermod -aG sudo prova1
```
![](img/8.png)
***

### 🔹 Mostrar grups de `prova1`

```bash
groups prova1
```
![](img/9.png)
***

### 🔹 Eliminar usuari `prova1` (amb directori)

```bash
sudo userdel -r prova1
```
![](img/10.png)
***

# 🔐 Bloc 3: Permisos i propietats

### 🔹 Crear `secret.txt` i treure permisos a “altres”

```bash
touch secret.txt
chmod o-rwx secret.txt
ls -l secret.txt
```
![](img/11.png)
***

### 🔹 Canviar propietari a `prova2`

```bash
sudo chown prova2 secret.txt
ls -l secret.txt
```
![](img/12.png)
***

### 🔹 Assignar grup `alumnes`

```bash
sudo chgrp alumnes secret.txt
ls -l secret.txt
```
![](img/13.png)
***

### 🔹 Canviar propietari i grup de `proves2`

```bash
sudo chown prova2:alumnes ~/proves2
ls -ld ~/proves2
```
![](img/14.png)
***

### 🔹 Assignar permisos a carpeta `proves2` (propietari i grup RW, altres cap)

```bash
chmod 660 ~/proves2
ls -ld ~/proves2
```
![](img/15.png)
***
