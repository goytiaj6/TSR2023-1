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

Donde lo que los caracteriza es el tipo de rueda que utilizan, ya que los robots no holonómicos utilizan ruedas convencionales como las que tienen los autos normales
![image](https://www.researchgate.net/profile/Mohamed-Boukattaya/publication/330970738/figure/fig1/AS:724130081017856@1549657473332/Nonholonomic-wheeled-mobile-robot.ppm)

Mientras que los omnidireccionales utilizan ruedas mecanum, mejor conocidas como ruedas secas. Estas ruedas generalmente es una llanta aumentada con rodillos en su circunferencia que giran libremente permitiendo un deslizamiento en todas las direcciones del sistema.
![image](https://www.luisllamas.es/wp-content/uploads/2018/09/arduino-robot-omni-wheel-robots.jpg)

### Restricciones cinemáticas y diferencias entre los tipos de sistmemas
- Para los sistemas no holonómicos sabemos que la cantidad de grados de libertad controlables es menor a la cantidad de grados totales; como los carros normales, tracciones diferenciales o configuracioens de tricíclos, esto nos dice que no todas las trayectorias son posibles.

- Para los sistemas omnidireccionales (holonómicos) sabemos que la cantidad de grados de libertad controlables es igual a la cantidad de grados de libertad totales; Lo que nos dice que todas las trayectorias en el plano son posibles. [[3]](#3)

### Conceptos de localización, ruta, odometría y planeación de ruta.
- Localización: Consiste en determinar la posición del robot en relación a un mapa dado a un entorno. [[4]](#4)
- Ruta: secuencia de posiciones en las que un robot se encuentra libre de colisión con los obstáculos del espacio de trabajo. [[5]](#5)
- Odometría: Estudio de la estimación de la posición de vehículos con ruedas durante la navegación 
- Planeación de rutas: Sea un espacio de trabajo de un robot cuya planeación de ruta es aquella por la cual este desea encontrar un camino libre de colisión dada una configuración incial y una final si existe; en caso contrario que sea capaz de determinarla. [[5]](#5)

### Caracterización de la plataforma móvil TurtleBot3:
- Modelo cinemático

Como es un robot diferencial, tiene el modelo cinemátcio siguiente:

![image](https://user-images.githubusercontent.com/20031100/190882535-94d602be-c1f8-484d-a60d-3976a3b4d6c2.png)

![image](https://user-images.githubusercontent.com/20031100/190882543-b3ce3e11-d0f2-4b36-9805-c756ae547b8f.png)

![image](https://user-images.githubusercontent.com/20031100/190883055-de66617c-74fd-4875-8d10-2fd724d90433.png)


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

donde: 
- Φ: es el angulo de giro con respecto al origen 
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

<a id="4">[4]</a> Localización y planificación de trayectorias. (s/f). Tekniker.es. Recuperado el 16 de septiembre de 2022, de https://www.tekniker.es/es/localizacion-y-planificacion-de-trayectorias

<a id="5">[5]</a>(S/f-b). Udlap.mx. Recuperado el 16 de septiembre de 2022, de http://catarina.udlap.mx/u_dl_a/tales/documentos/lis/munoz_r_o/capitulo4.pdf

<a id="6">[6]</a> ROBOTIS e-manual. (s/f). ROBOTIS E-Manual. Recuperado el 16 de septiembre de 2022, de https://emanual.robotis.com/docs/en/platform/turtlebot3/features/
