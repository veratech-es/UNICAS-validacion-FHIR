# Validación mediante TestScripts FHIR

Esta carpeta contiene los conjuntos de casos de pruebas en TestScript (en formato JSON) para ejecutar pruebas automáticas sobre un servidor FHIR.

## Contenido

- TestScripts definidos para flujos de prueba específicos
- Fixtures (datos previos) necesarios para la ejecución
- Manual de instalación de herramienta que ejecute los TestScripts, en nuestro caso [TestScript Engine](https://github.com/fhir-crucible/testscript-engine)
- Comandos para lanzar los TestScripts en TestScript Engine

## Tipos de TestScript

- [`ReadProfileTemplate`](./TestScript/ReadProfileTemplate) contiene un conjunto de TestScript para la validación de instancias para cada uno de los perfiles en el servidor declarados en el CapabilityStatement. Generado con testscript-generator
- [`search_params`](./TestScript/search_params) contiene un conjunto de TestScript para la validación de los parámetros de búsqueda declarados en el CapabilityStatement. Generado con testscript-generator
- [`operacionesUNICAS`](./TestScript/operacionesUNICAS) contiene un conjunto de TestScript para la validación de las operaciones permitidas para cada uno de los perfiles declarados en el CapabilityStatement. Generado por la oficina técnica de UNICAS
- [`fixtures`](./TestScript/fixtures) contiene los ejemplos referenciados por los distintos TestScript

## Instalando TestScript Engine

Existen diversos métodos para ejecutar los TestScript, se ha seleccionado [TestScript Engine](https://github.com/fhir-crucible/testscript-engine) para la ejecución, pero cualquier validador como puede ser [Inferno](https://inferno.healthit.gov/) se puede utilizar. TestScript Engine es una aplicación Ruby, por lo que requiere que el servidor disponga de capacidad Para instalar el TestScript Engine se ha de descargar la última versión, o bien compilando el github, o bien descargandolo del gestor de paquetes GEM

## Ejecutando TestScript

Hay dos métodos para ejecutar el TestCript con TestScript engine 

* Clonando el repositorio

Se puede clonar el repositorio git de testscript engine. y entonces compilarlo con *bundle install* seguido de *bundle exec bin/testscript_engine*. Esto arrancará el testscript engine en un contexto local.

Este repositorio continene TestScript de prueba con lo que habrá que actualizar la carpeta *TestScripts* de prueba.

* Desde gem install

Se puede instalar el testscript engine directamente desde un gestor de paquetes gem. Para ello hay que ejecutar *gem install testscript_engine*. Una vez instalado se puede ejecutar con *testscript_engine*.


En cualquiera de los dos casos, al arrancar el testscript_engine se permite configurar las rutas donde están disponibles los TestScript a ejecutar y la ruta de salida del análisis
