# Proyecto de extensión: Sala de Emergencias

## Índice

* [1. Preámbulo](#1-preámbulo)
* [2. Resumen del proyecto](#2-resumen-del-proyecto)
* [3. Objetivos de aprendizaje](#3-objetivos-de-aprendizaje)
* [4. Consideraciones generales](#4-consideraciones-generales)
* [5. Criterios de aceptación mínimos del proyecto](#5-criterios-de-aceptación-mínimos-del-proyecto)
* [6. Hacker edition](#6-hacker-edition)

## 1. Preámbulo

Los datos son de poca utilidad si no están organizados para ser analizados y que
sirvan como para entender y tomar decisiones sobre un fenómeno. Para que los datos
se conviertan en **información** fácil de entender para los usuarios, necesitamos
procesar estos datos. Una manera simple de hacerlo es creando _interfaces_ interactivas
y _visualizaciones_.

Un caso especial, y que es crítico en los hospitales, es la gestión de los
pacientes que llegan a la sala de emergencias según sus necesidades particulares.
El análisis de la información nos puede permitir asignar médicos y salas,
que son siempre escasas, a quienes más lo necesitan. Para lograrlo, existen sistemas
de categorización de pacientes, donde no importa el orden de llegada sino su
gravedad de acuerdo a la siguiente tabla:

![Categorización-UEH-660x1025](https://user-images.githubusercontent.com/7809496/71842401-4d6b4e00-30a0-11ea-9784-910bcc7b2a8a.png)

Los pacientes graves deben pasar inmediatamente a atenderse con un
médico. Los de mediana gravedad deberán esperar por una camilla libre, si
hay más de un paciente en esta categoría, se ordenarán según su hora de llegada.
Los demás pacientes se ordenarán primero por categoría de gravedad y luego
por hora de llegada; pasarán sólo si es que no hay alguien de mayor prioridad
esperando por atención.

## 2. Resumen del proyecto

![Free to use from https://pxhere.com/es/photo/599363](emergency-room.jpg)

En esta ocasión trabajarás en dupla para crear una aplicación web para la gestión
de filas/colas de la sala de emergencias de un hospital y que responda a los criterios
de gravedad antes descritos. Esta vez tú misma tendrás que crear los datos con
los que trabajarás.

Este proyecto es agnóstico a la tecnología que uses, es decir puedes desarrollarlo
en Vanilla JavaScript o algún _framework_  o biblioteca (librería) de tu elección.

## 3. Objetivos de aprendizaje

### Generales

1. [Aplicar y profundizar todo lo que ya aprendiste](https://github.com/Laboratoria/bootcamp/blob/master/projects/learning-objectives.md).
2. Pensar en las necesidades de las personas para crear tus "Historias de Usuario".
3. Escribir y trabajar con historias de usuario, sus definiciones de terminado
(_definition of done_) y criterios de aceptación como herramienta central de la
organización y planificación de tu trabajo.
4. Se te recomienda pensar en _test driven development_ al momento de programar la
solución. Tendrás que escribir las pruebas unitarias, aprovechen la oportunidad
de comenzar haciéndolo antes de escribir la funcionalidad.

### Front-end

1. El objetivo principal de este proyecto es que te familiarices con el uso de
arreglos y diccionarios, incluso que los combines para obtener estructuras de
datos más complejas que te permitan resolver problemas grandes de datos.
2. Dominar la manipulación del DOM para hacer aplicaciones interactivas y
dinámicas sin necesidad de tener todo en HTML o varios archivos de HTML, sino
que generando y modificando HTML desde JavaScript.
3. Usar eventos del DOM, como _clicks_ o entradas de texto, para interactuar
con los usuarios.
4. Perfeccionar tus habilidades de diseño y CSS _responsive_ para lograr una
interfaz que permita tener todos los elementos pedidos sin entorpecerse entre sí.

### UX

1. Definir un producto que responda a las necesidades y dificultades de
pacientes que esperan a ser atendidos/as en urgencias y los de el/la doctor/a
que los/as ingresa a la lista de espera, a partir de un acercamiento a los/as
usuarios/as (observación contextual, entrevistas con doctores, enfermeras, etc).
2. Seleccionar y priorizar la información a mostrar para cada usuario/a.
3. Crear interfaces que sigan los principios de diseño visual.
4. Iterar el diseño del producto y su usabilidad a partir del testeo con
usuarios/as (mínimo 5 testeos de usabilidad).

## 4. Consideraciones generales

* El trabajo debe ser hecho en duplas.
* Debes tener tu código alojado en *GitHub* usando *Git* y sus comandos *commit*,
 *push*, *pull*, etc.
* Debes desplegar tu aplicación usando [GitHub Pages](https://pages.github.com/).
* Toma el tiempo necesario para completar el proyecto con la máxima calidad posible.
 Asume 3 semanas como una referencia inicial.
* Tus pruebas unitarias deben tener una cobertura del 70% de _statements_.

## 5. Criterios de aceptación mínimos del proyecto

* Se debe poder "ingresar" un paciente, guardando su nombre, edad, género, descripción
de la emergencia y categoría de la misma (gravedad).
* Se debe poder ver las salas de atención, si están ocupadas por pacientes, sus
datos y la categoría de la emergencia en la que se encuentran.
* Se debe poder ver la cola de atención ordenada según el nivel de emergencia
de cada paciente.
* Se debe poder marcar una sala como "libre" porque ya terminó la atención del
paciente que estaba en ella.
* Se debe poder hacer pasar a un paciente de la cola para su atención en una de
las salas disponible, comunicando su nombre y a cuál sala debe pasar.

Para facilitar el desarrollo toma en cuenta los siguientes consejos:

* Quien usa el sistema es la médico a cargo de categorizar a los pacientes y
nadie más. Su pantalla también es visible en un televisor del hospital.
* Todo debe ser visible en una sola pantalla con resolución de TV (1280x720),
considera esto al diseñar la interfaz.
* Hay solamente 6 salas de atención pero sería genial si la aplicación permitiera
cambiar ese número fácilmente. En primer lugar como una constante dentro de la
aplicación y en una segunda iteración como una configuración que la usuaria puede
definir.

## 6. Hacker edition

* Es probable que en tu solución toda la información se mantenga en memoria, es
decir, si alguien recarga la página todo lo guardado desaparece; considera usar
alguna herramienta para mantener la persistencia de esta. Una opción es guardar
los datos en [window.localStorage](https://developer.mozilla.org/es/docs/Web/API/Window/localStorage)
, otra opción es considerar alguna base de datos, de estas hay muchas incluyendo
Firebase.

## Contenido de referencia

* [Colas y Colas de prioridad](https://medium.com/laboratoria-developers/queues-in-javascript-2602677c9c3b)
* [Priority queue (en Inglés)](https://github.com/trekhleb/javascript-algorithms/tree/master/src/data-structures/priority-queue)
