# Validación mediante TestScripts FHIR

Esta carpeta contiene los conjuntos de casos de pruebas en TestScript (en formato JSON) para ejecutar pruebas automáticas sobre un servidor FHIR.

## Contenido

- TestScripts definidos para flujos de prueba específicos
- Fixtures (datos previos) necesarios para la ejecución
- Manual de instalación de herramienta que ejecute los TestScripts, en nuestro caso [TestScript Engine](https://github.com/fhir-crucible/testscript-engine)
- Comandos para lanzar los TestScripts en TestCript Engine

## Tipos de TestScript

- [`ReadProfileTemplate`](./ReadProfileTemplate) contiene un conjunto de TestScript para la validación de instancias para cada uno de los perfiles en el servidor declarados en el CapabilityStatement. Generado con testscript-generator
- [`search_params`](./search_params) contiene un conjunto de TestScript para la validación de los parámetros de búsqueda declarados en el CapabilityStatement. Generado con testscript-generator
- [`operacionesUNICAS`](./operacionesUNICAS) contiene un conjunto de TestScript para la validación de las operaciones permitidas para cada uno de los perfiles declarados en el CapabilityStatement. Generado por la oficina técnica de UNICAS
- [`fixtures`](./fixtures) contiene los ejemplos referenciados por los distintos TestScript