![UCU Logo](https://upload.wikimedia.org/wikipedia/commons/6/63/UCU.png)

# Segundo Obligatorio P1

Por favor, abran el archivo `SegundoObligatorioP1` donde encontrarán todas las instrucciones detalladas para completar el ejercicio.

### Fecha límite: 06/06/2024 

### Se entrega por WebAsigantura

---

### Objetivo

En este proyecto, deberan implementar una version simple de la lógica del clásico juego de Buscaminas. 
Nosotros les proporcionamos la configuracion grafica del juego, todo lo demas deberá ser implementado por ustdes ustedes.

### Inicializacion

Para que la interfaz grafica funcione, definimos algunas especificacion simples como el tamaño de la pantalla y el tamaño de las celdas. 

```python
pygame.init()


tamano_pantalla = 400
filas, columnas = 10, 10
tamano_celda = tamano_pantalla // filas
pantalla = pygame.display.set_mode((tamano_pantalla, tamano_pantalla))
pygame.display.set_caption("Buscaminas")


BLANCO = (255, 255, 255)
NEGRO = (0, 0, 0)
ROJO = (255, 0, 0)
VERDE = (0, 255, 0)



### Funciones de Interfaz Gráfica

'dibujar_tablero(tablero)' inicialamente recibe unicamente el tablero del juego. Observando las operaciones que se hacen dentro de dicha funcion, deberan inferir las caracteristicas que debera tener su tablero. Pueden modificar esta funcion a su conveniencia. 

'mostrar_mensaje(mensaje)' se encargara de desplegar el mensaje que informara al usuario la derrota o la victoria respectivamente.

### main

El bucle principal del juego, se encarga de inicializarlo y de obtener las posiciones del mouse y su representacion en terminos de filas y columnas. Esto ultimo es fundamental para identificar la celda que el usuario destapado. Deben agregar logica a esta para lograr impelemntar lo que se pide.


### Video de la implementacion 

![Buscaminas Demo](./My%20Project.gif)



Santiago Amoretti
