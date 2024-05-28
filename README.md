# GitHub-MultiRepo

## Contexto:
Imagina que trabajas como desarrollador de software en la famosa empresa TuEmpresa, una empresa de comercio electrónico en rápido crecimiento. La empresa dispone de varias aplicaciones webs así como de varias aplicaciones de backend para su funcionamiento.

## Problema:
El proceso actual de despliegue de las aplicaciones web y de backend se lleva a cabo a través de GitHub Actions almacenadas en cada uno de los repositorios de las aplicaciones, lo que da lugar a que ante cualquier cambio que deba hacerse en una 
Action se deban editar n veces, una para cada repositorio de aplicación, lo que da lugar a numerosos problemas por olvidos de actualización o por Actions diferentes en diferentes repositorios.
Ademas, estas Actions abusan de la Action de bash ejecutando scripts de considerable tamaño que aumentan significativamente la dificultad de lectura y comprensión de las Actions.

## Solución:
Se propone externalizar las actions a un repositorio especifico y del que luego los repositorios de aplicación hereden y configuren según sus necesidades. Ademas se propone la creación de varias actions custom para incluir en ellas los script de bash y que así la comprensión de las pipelines mejoren.

## Implementación:
### Creación de repositorios:
 - Crear un repositorio en GitHub para almacenar el código fuente de la aplicación de TuEmpresa (un hello world en el lenguaje que prefieras).
 - Crear un segundo repositorio en GitHub para almacenar las Pipelines genéricas de las que heredar y las Actions personalizadas.
 - Configuración de la herencia de pipelines
 - Configura una GitHub Action en el repositorio de aplicación para que herede del repositorio de las actions y ejecute el hola mundo.

## Desarrollo de Actions personalizadas:
 - Desarrollar una Action personalizada de GitHub que ejecute el hola mundo sin necesidad de pasarle la orden de ejecución, solamente el nombre del fichero a ejecutar.
 - Ejecución de otra versión de Action
 - Incluye la action personalizada en la pipeline.

## Tips:
 - Crea un hola mundo en tu lenguaje favorito, por defecto bash.
 - Custom Actions: https://docs.github.com/en/actions/creating-actions
 - Reusing workflows: https://docs.github.com/en/actions/using-workflows/reusing-workflows
