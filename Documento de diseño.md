# Titulo: Template de documento de diseño

## ¿Que es este documento?

El documento de diseño contiene todos los detalles necesarios para desarrollar el sistema

## Overview: Problema a resolver

La empresa "RandomCameraReviews" necesita un sistema (página web) que permita que fotografos profesionales suban "reviews" de Camaras fotograficas, para que cualquier persona desde cualquier parte del mundo pueda buscar los los reviews y comprarlas a travez de su portal.

La empresa cuenta con un equipo de developers especializado en frontEnd que realizara un portal para que los editores suban los "reviews" y los usuarios puedan verlos, y han solicitado que tu como especista en Backend, les proporciones un sistema, incluyendo API que permita  realizar lo siguiente:

* Subir reviews de Camaras fotograficas
* Obtener el contenido de los reviews para mostrarlo en vistas del portal en sus versiones web y mobile.
* Manejo de usuarios para editores (no incluye visitantes que leen los reviews)

Tambien se sabe que la empresa "RandomCameraReviews" planea distribuir mayormente en America del Sur donde esta su mercado mas grande, pero tambien tienen ventas en norte america, Europa, y muy pocas en Asia.


### Alcance(Scope)

Descripción..

#### Casos de uso

* Como editor me gustaria poder subir una review de una camara
* Como usuario no registrado me gustaria poder leer una review de una camara

#### Out of Scope (casos de uso No Soportados)

* Como usuario no registrado me gustaria poder subir una review de una camara
* Como editor me gustaria dar feedback a otras review
* Como editor me gustaria aprobar comentarios en reviews de usuario registrados
* Como usuario no registrado me gustaria registrarme
* Como usuario no registrado me gustaria poder compartir una review en mis redes sociales
* Como usuario registrado me gustaria comentar en las reviews
* Como usuario registrado me gustaria dar seguimiento de los comentarios en la reviews que me interesan

---

## Arquitectura

### Diagramas

    poner diagramas de secuencia, uml, etc

![ejercicio-264d63e6-df5b-4dcd-ae5c-6e963131aa79](https://github.com/andres-brinez/CameraReviews/assets/94869227/114c790c-4032-4ce9-90a4-7b072b9470a7)

![image](https://github.com/andres-brinez/CameraReviews/assets/94869227/fafbcb7d-3b14-4e36-9825-8456b5898f2c)

#### Diagrama de clase 

![entity-design-c8050de6-acb1-44e7-addc-be92a47b7372](https://github.com/andres-brinez/CameraReviews/assets/94869227/5430aa7d-fccf-49cd-ad88-a1e2820bac05)

![EntityDiagram drawio-6fbe9896-4606-47a2-ba82-7216291fab7f](https://github.com/andres-brinez/CameraReviews/assets/94869227/ac078f4c-9c19-46a6-a3b4-354acac7dd67)


### Modelo de datos

    Poner diseño de entidades, Jsons, tablas, diagramas entidad relación, etc..

![image](https://github.com/andres-brinez/CameraReviews/assets/94869227/8ac40ee8-00ab-4462-ae9b-5a4d5eb529a8)

### Plan de pruebas

* Crear proyecto de pruebas que valide los siguientes casos de uso 
- Registrar un usuario nuevo y validar que se haya creado correctamente, 
- loguear un usuario y crear un review,
- simular que un visitante puede  obtener un review, 

## Limitaciones

Lista de limitaciones conocidas. Puede ser en formato de lista.
A la medida que el sistema se vaya desarrollando, se iran agregando mas limitaciones.

- Llamadas al API que permiten subir un review, no exceden los limites de latencia 500ms
- Llamadas al API que permiten obtener un review para lectura deben tener una latencia menor a 200ms    

Ejempo.

- Llamadas del API tienen latencia X
- No se soporta mas de X usuarios concurrentes
- No se soporta mas de X llamadas por segundo
- No se soporta mas de X llamadas por dia
- Llamdas al API que permiten subir contenido tienen un limite de X MB
- No se soporta mas de X MB de contenido por review
- No se soporta mas de X reviews por usuario
- No se soporta mas de X usuarios
- No se soporta mas de X reviews


## Costo

Descripción/Análisis de costos
Ejemplo:
"Considerando N usuarios diarios, M llamadas a X servicio/baseDatos/etc"

- 1000 llamadas diarias a serverless functions. $XX.XX
- 1000 read/write units diarias a X Database on-demand. $XX.XX
  Total: $xx.xx (al mes/dia/año)
