NOTA: Tuve unos errores al pasar los comandos de git en los CI/CD lo cual no me percate hasta el final que no me funcionaba nada, lo logre corregir al final
 
 
 # WebAvanzada

Pregunta 1 (2 pts). ¿Por qué no se recomienda desarrollar directamente sobre main en este laboratorio?

Para poder desarrollar sin posibilidad de errores accidentales, tambien para la revision de codigo segura.

Pregunta 2 (2 pts). ¿Qué problema se evita al utilizar --skip-git al crear el proyecto Angular?

Se utiliza para evitar crear un repo y un commit inicial, generando problemas de anidamiento

Pregunta 3 (2 pts). ¿Qué verifica npm run build en esta etapa del laboratorio?

Que no haya errores y la sintaxis sea valida

Pregunta 4 (2 pts). ¿Qué utilidad tiene revisar git status o git diff --cached antes de realizar un commit?

Sirve para revisar la branch en la cual vamos a hacer el commit y tambien para ver que vamos a cambiar con el commit

Pregunta 5 (2 pts). ¿Qué evento activa el workflow ci.yml?

Una pull request que se haga en el main

Pregunta 6 (2 pts). En runs-on: ubuntu-latest, ¿qué representa ubuntu-latest?

Indica la ultima version en la cual se esta trabajando, por ende que se utilice la ultima version de ubuntu

Pregunta 7 (2 pts). Ordene las etapas de validación que ejecuta el job frontend y explique por qué npm ci se ejecuta
antes que las pruebas.

Obtiene el codigo, luego configura node.js, luego instala dependencias y luego ejecuta pruebas y finalmente construyye angular. Siempre se
ejecuta el npm ci para verificar que no haya errores por versiones anteriores.

Pregunta 8 (3 pts). Después del push, indique qué etapa del pipeline falla y qué ocurre con las etapas siguientes.

Falla el pipeline de Ci detiene el aprovisionamiento y la subida.

Pregunta 9 (3 pts). ¿Debería integrarse este Pull Request a main mientras el pipeline está fallando? Justifique.

No seria lo correcto, ya que el pull request deberia ser el filtro de calidad.

Pregunta 13 (2 pts). ¿Qué diferencia existe entre terraform validate, terraform plan y terraform apply?

validate realizar una comprobacion sintatica, plan es una simulacion y apply lleva a cabo los cambios en la infraestructura real

Pregunta 14 (2 pts). ¿Por qué ci.yml se activa con pull_request y cd.yml se activa con push sobre main?

ci usa pull request para validar temporalmente las prue bas y cd usa push sobre main porque el despliegue a los entornos debe ocurrir cuando el codigo fue ejecutado y revisado
Pregunta 15 (2 pts). ¿Qué función cumple Terraform dentro de este flujo de CD?

Funciona como herramienta de automatizacion 
Pregunta 16 (2 pts). ¿Por qué el workflow usa ${{ secrets.DEMO_TOKEN }} en lugar de escribir el valor directamente?
Ya que se usa un cifrado para proteger los valores reales
