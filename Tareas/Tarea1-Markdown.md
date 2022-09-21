# Practica de documentación en Markdown
Desarrollo 

## 

| Código | Description |
| ------:| ----------- |
| ***Asignatura*** | Código del Trabajo o Número de Tarea | 
| **TSM-2023-1** |  Tarea1-Markdown |

## Contenido
- [1 . Introducción](#introduccion)
- [2 . Desarrollo](#desarrollo)
- [3. Conclusiones](#conclusiones)
- [4 . Autor](#autor)
- [5 . Referencias](#referencias)

## Introducción
Markdown originalmente nació como una herramienta de conversión de texto plano a HTML. Esta herramienta fue creada en 2004 por John Gruber que es distribuida de manera gratuita bajo una licencia BSD (Berkeley Software Distribution, un tipo del sistema operativo Unix-like). Markdown es considerado como un lenguaje ya que permite crear contenido de una manera sencilla de escribir, manteniendo un diseño legible. Visto de manera muy simple, Markdown puede considerarse como un método de escritura.

Markdown cuenta con tres tipos de elementos básicos, siendo elementos de bloque, elementos de línea y elementos varios,  entro los cuales nos permite crear:

* Encabezados
* Listas
* Citas
* Links
* Código
* Imágenes

Markdown permite realizar lo antes mencionado y más, de forma rápida, sencilla y limpia, además de que se basa en texto plano, tiene compatiblidad con topo tipo de dispositivos. [[1]](#1)[[2]](#2)

## Desarrollo
### Clasificación de los robots móviles por configuración 
Los robots moviles se encuentran clasificados en tres: 

1. Robots móviles por ruedas
2. Robots móviles por patas
3. Robots móviles por orugas

Siendo los robots moviles por ruedas la categoría que tiene mayor desarrollo, esta, a su vez consta de dos categorias:

* Omnidireccionales
* No holonómicos

Donde lo que los caracteriza es el tipo de rueda que utilizan, ya que los robots no holonómicos utilizan ruedas convencionales como las que tienen los autos normales.

![image](https://ars.els-cdn.com/content/image/1-s2.0-S092188901300095X-gr1.jpg)

Mientras que los omnidireccionales utilizan ruedas mecanum, mejor conocidas como ruedas secas. Estas ruedas generalmente es una llanta aumentada con rodillos en su circunferencia que giran libremente permitiendo un deslizamiento en todas las direcciones del sistema.

![image](https://www.luisllamas.es/wp-content/uploads/2018/09/arduino-robot-omni-wheel-robots.jpg)

### Restricciones cinemáticas y diferencias entre los tipos de sistmemas
* Para los sistemas no holonómicos, se encuentran restringidos por la cantidad de grados de libertad controlables, que son menores al numero de grados de libertad totales del sistema. Siendo los ejemplos más comunes los carros normales, tracciones diferenciales o configuraciones de tricíclos. No todas sus trayectorias son posibles.

* Para los sistemas omnidireccionales u holonómicos, se encuentran restringidos por la cantidad de grados de libertad controlables, que son iguales al numero de grados de libertad totales del sistema. Todas sus trayectorias son posibles. [[3]](#3)

### Conceptos de localización, ruta, odometría y planeación de ruta.
* Localización: Consiste en determinar la posición del robot en relación a un mapa dado del entorno. [[4]](#4)
* Ruta: Representa la secuencia de posiciones en las que un robot se encuentre libre de colisiones con los obstáculos del espacio de trabajo. [[5]](#5)
* Odometría: Es el estudio de la estimación de la posición de vehículos con ruedas durante la navegación.
* Planeación de rutas: *Dado un robot, un espacio de trabajo, una configuración inicial y una configuración final, se desea encontrar una ruta libre de colisión para el robot, de la configuración inicial a la configuración final, si ésta existe. En caso contrario, determinar que dicha ruta no existe.* [[5]](#5)

### Caracterización de la plataforma móvil TurtleBot3:
* Modelo cinemático

![image](https://emanual.robotis.com/assets/images/platform/turtlebot3/hardware_setup/turtlebot3_dimension1.png)

Al ser un robot no holonómico, es un robot diferencial, por lo que tiene el siguiente modelo cinemático:

$$
\mathbb{q^°} \ =\ \begin{bmatrix}
	Φ & x^° & y^°
\end{bmatrix} \ =\ \begin{bmatrix}
-r/d2 & r/2d \\
r/2 cosΦ & r/2 cosΦ \\
r/2 isnΦ & r/2 sinΦ
\end{bmatrix} * \ \begin{bmatrix}
ωL\\
ωR
\end{bmatrix}\
$$

en donde: 
- Φ: es el ángulo de giro con respecto al origen 
- r: es el radio de las ruedas del robot 
- d: es la distancia del eje hacia el centro del eje del robot 
- ωL y ωR : son las velocidades angulares de las ruedas del robot 

### Sensores y actuadores que lo integran

  Según la página de Robotis, el único sensor que usa el TurtleBot3 en su versión Burger es un     LIDAR "LDS-01" o "LDS-02" [[6]](#6)

  
  En cuanto a actuadores, tenemos que usa dos Motores 	DYNAMIXEL (XL430-W250-T) [[6]](#6)
   ![image](https://user-images.githubusercontent.com/20031100/190827583-2d136908-5c30-4047-854f-fb7e6483c27b.png)

- Nodos y Tópicos de ROS utilizados por la plataforma Turtlebot3 y sus sensores

Algunos de los nodos que ocupa el Turtlebot son: 
- SLAM 
- Teleoperation

Algunos de los tópicos que opcupa 
- cmd_vel 
- odom
- LaserScan

## Conclusiones
Markdown es una forma fácil de hacer reportes en repositorios y es sumanente versatil para documentar de forma colaborativa con tu equipo de trabajo, además de lo rápido que es pra hacer cambios en el sistema sin necesidad de abrir varios programas, sino en el mismo sistema de código implementado.
 

## Autor
| Iniciales  | Description |
| ----------:| ----------- |
| **JHGG**  | Jorge Hadamard Goytia González [GitHub profile](https://github.com/goytiaj6) |

## Referencias
<a id="1">[1]</a> J. Cristóbal. "Markdown - La guía definitiva en español". Markdown. https://markdown.es/ (accedido el 18 de septiembre de 2022).

<a id="2">[2]</a> J. Cristóbal. "Sintaxis Markdown al completo - Cheatsheet en español". Markdown. https://markdown.es/sintaxis-markdown/ (accedido el 18 de septiembre de 2022).

<a id="3">[3]</a> K. M. Lynch y F. C. Park, "13. Wheeled Mobile Robots", en Modern Robotics: Mechanics, Planning, and Control. Londres: Cambridge University Press, 2017, pp. 513–553.

<a id="4">[4]</a> "Localización y planificación de trayectorias - TEKNIKER". Tekniker | Research and Technology Centre. https://www.tekniker.es/es/localizacion-y-planificacion-de-trayectorias (accedido el 20 de septiembre de 2022).

<a id="5">[5]</a> R. O. Muñoz, "Planeación de Rutas para un Actor Digital en un Ambiente Virtual", Electronic Thesis or Dissertation, Universidad de las Américas Puebla, Cholula, Puebla, 2007. Accedido el 20 de septiembre de 2022. [En línea]. Disponible: http://catarina.udlap.mx/u_dl_a/tales/documentos/lis/munoz_r_o/

<a id="6">[6]</a> ROBOTIS - Open Robotics. "ROBOTIS e-Manual". ROBOTIS e-Manual. https://emanual.robotis.com/docs/en/platform/turtlebot3/features/ (accedido el 20 de septiembre de 2022).
