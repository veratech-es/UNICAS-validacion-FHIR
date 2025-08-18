# Validación de Servidor FHIR

Esta carpeta contiene scripts y herramientas para verificar que un servidor FHIR implementa el API REST de HL7 FHIR y los casos de uso requeridos por el proyecto UNICAS

## Contenido

Workspaces para Postman e Insomnia
- **Insomnia**
  - [`Insomnia_collection.yaml`](./Insomnia_collection.yaml)
- **Postman**
  - [`Postman_collection.json`](./Postman_collection.json)

## Objetivo

Asegurar que el servidor cumple con las especificaciones mínimas requeridas para interoperar de forma segura 

## Requisitos previos

- Un servidor FHIR desplegado y accesible desde la red.
- Conocer la **URL base** del servidor (por ejemplo: `https://fhir.mi-servidor.org/fhir`), así como el id de cliente y secreto, la url donde conseguir token de sesión (por ejemplo: `https://mi-servidor.org/token`) y la url del servidor terminológico.
- Herramientas instaladas:
  - [Insomnia](https://insomnia.rest/download) o [Postman](https://www.postman.com/downloads/).

## Instrucciones de uso

### Usando Insomnia

1. Abrir Insomnia.
2. Importar el archivo [`Insomnia_collection.yaml`](./Insomnia_collection.yaml).
3. Configurar las variable de entorno `base_url`, `token_url`, `terminology_id`, `client_id`, `client_secret`.
4. Ejecutar los requests agrupados por carpetas.

### Usando Postman

1. Abrir Postman.
2. Importar el archivo [`Postman_collection.json`](./Postman_collection.json).
3. Configurar las variables de entorno `base_url`, `token_url`, `terminology_id`, `client_id`, `client_secret`.
4. Obtener el token de sesión.
5. Ejecutar las colecciones de pruebas.

> **Nota:** Insomnia gestiona automaticamente el token de sesión. En caso de utilizar Postman es necesario obtener el token de sesión antes de realizar las llamadas.

