# Bazaar — Trabajo Práctico KanguShop

Bazaar es una plataforma de eCommerce desarrollada como trabajo práctico para la materia Ingeniería de Software II curso Rojas. La arquitectura está basada en microservicios independientes, cada uno con su propia base de datos y responsabilidad bien definida, comunicados a través de un API Gateway.


![](../profile/images/arquitecture.jpeg)

---

## Repositorios

### [service-catalog](https://github.com/bazaar-fiuba-2026/service-catalog)

Microservicio REST encargado del ciclo de vida de productos: creación, consulta, actualización y eliminación. Gestiona categorías, stock e imágenes de productos, e incluye un endpoint de recomendaciones por categoría y un historial de auditoría de cambios. Construido con **FastAPI** y **PostgreSQL**.

### [service-wishlist](https://github.com/bazaar-fiuba-2026/service-wishlist)

Microservicio REST que permite a los usuarios guardar y gestionar sus listas de deseos. Almacena únicamente IDs de productos (delegando los datos al service-catalog) y valida la identidad del usuario mediante el header `X-User-Id` inyectado por el API Gateway. Construido con **FastAPI** y **MongoDB**.
