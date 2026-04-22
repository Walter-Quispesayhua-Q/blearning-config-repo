# B-Learning 2.0 Config Repo

Repositorio de configuración centralizada para la plataforma **B-Learning 2.0**.

## Propósito

Este repositorio almacena los archivos de configuración que serán consumidos por **Spring Cloud Config Server** y distribuidos a los distintos microservicios del sistema.

## Objetivo

Centralizar la configuración de los servicios para:

- mantener consistencia entre entornos
- facilitar cambios de configuración sin duplicar archivos
- separar la configuración del código fuente
- mejorar el mantenimiento y escalabilidad del ecosistema de microservicios

## Estructura

Este repositorio puede contener archivos como:

- `application.yml` → configuración compartida entre todos los servicios
- `{nombre-servicio}.yml` → configuración específica de un microservicio
- `{nombre-servicio}-{perfil}.yml` → configuración específica por entorno o perfil

## Ejemplos

- `application.yml`
- `users-service.yml`
- `users-service-dev.yml`
- `gateway-service.yml`

## Buenas prácticas

- No almacenar credenciales sensibles en texto plano
- Mantener nombres consistentes por servicio
- Separar configuración general de configuración específica
- Versionar los cambios con mensajes claros y descriptivos

## Relación con Config Server

Este repositorio es consumido por el **Config Server**, el cual se encarga de leer estos archivos y exponer la configuración a los microservicios de **B-Learning 2.0**.

## Nota

El archivo `application.yml` propio del **Config Server** **no va en este repositorio**.  
Ese archivo debe existir dentro del proyecto del `config-server`.

---
**Proyecto:** B-Learning 2.0  
**Módulo:** Configuración centralizada
