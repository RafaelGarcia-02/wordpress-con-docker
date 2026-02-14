# Despliegue de wordpress Seguro con Docker Compose
Este proyecto despliega un sitio **Wordpress** completo utilizando contenedores Docker. Incluye un proxy inverso para HTTPS, una base de datos aislada y una panel de administracion para la base de datos 

## 🚀 Caracteristicas
* **Wordpress**: Sitio web principal (Imagen de Bitnami/oficial)
* **Mysql 9.1**: Base de datos aislada en una red interna
* **phpMyAdmin**: Gestión de base de datos accesible vía web.
* **HTTPS-Portal**: Proxy inverso basado en Nginx con soporte automático para Let's Encrypt (SSL).

## 🛠️ Arquitectura de Red
El proyecto utiliza dos redes bridge para mayor seguridad:
1. **frontend-network**: Conecta el proxy con WordPress y phpMyAdmin.
2. **backend-network**: Conecta WordPress y phpMyAdmin con la base de datos MySQL (aislada del exterior).



## 📋 Requisitos
* Docker y Docker Compose instalado.
* Una instancia (AWS EC2 u otra) con los puertos 80, 443, 8080 abiertos.
* Un dominio (ej. No-IP) apuntando a la IP de la instancia.

## 🔧 Instalación

### Levantar instancia 
![alt text](<fotos/1-levantar instancia maquina virtual ubuntu.png>)

### Script instalacion docker
![alt text](<fotos/2-script instalacion docker.png>)

### Instalacion docker terminal
![alt text](<fotos/3-instalacion docker terminal.png>)

### Creacion dominio
![alt text](<fotos/4-creacion dominio.png>)

### Creacion variables de entorno
![alt text](<fotos/5-creacion variables de entorno.png>)

### Levantar contenedores terminal
![alt text](<fotos/7-levantar contenedores.png>)

### Comprobacion de que funciona
![alt text](<fotos/8-comprobacion que funciona.png>)

### Grupos de seguridad
![alt text](<fotos/9-grupos de seguridad.png>)