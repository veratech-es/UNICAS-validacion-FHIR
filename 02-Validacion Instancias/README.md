# Validación de Instancias FHIR

Aquí se presentan el manual para la validación de instancias HL7 FHIR respecto a la guía de implementación de UNICAS.

# Manual de validación — Herramientas y Procedimiento

> A continuación se muestra online el contenido del [`Manual validador instancias FHIR`](./Manual%20validador%20instancias%20FHIR.docx).

## Guía de implementación ÚNICAS

La guía de implementación ÚNICAS está disponible en:  
<https://unicas-fhir.sanidad.gob.es/>

## FHIR Validator

La validación de instancias se realiza con **FHIR Validator**, una aplicación Java desarrollada por HL7 International que permite validar una o varias instancias de prueba frente a la guía de implementación ÚNICAS.

- Soporta formatos: **XML**, **JSON** y **Turtle**.  
- Descarga (línea de comandos):  
  <https://github.com/hapifhir/org.hl7.fhir.core/releases/latest/download/validator_cli.jar>

**Requisito mínimo:** Java 11.

---

# Procedimiento

## Ejecución de FHIR Validator

Una vez descargada la aplicación, se puede lanzar desde la línea de comandos:

```bash
java -jar validator_cli.jar RUTA_A_VALIDAR \
    -ig URL_IG \
    -profile URL_PERFIL \
    -html-output OUT.HTML
```

# Parámetros del comando

- **`RUTA_A_VALIDAR`**: Directorio que contiene múltiples ficheros de instancias HL7 FHIR o ruta a un fichero concreto.
- **`-ig`**: URL donde se localiza la guía de implementación sobre la que se va a validar la instancia de datos.
- **`-profile`** *(opcional)*: URL del perfil específico frente al que se valida la instancia.
- **`-version`** *(opcional)*: Versión específica de HL7 FHIR a utilizar en la validación.

| Versión FHIR | Parámetro |
|--------------|-----------|
| R2           | 1.0       |
| R2B          | 1.4       |
| R3           | 3.0       |
| R4           | 4.0       |
| R4B          | 4.3       |
| R5           | 5.0       |

- **`-html-output`** *(opcional)*: Genera un informe HTML con los resultados de validación.  
  Si la `RUTA_A_VALIDAR` es un directorio, el HTML resultante contendrá la validación de todos los artefactos identificados en la carpeta.
  
...etc
