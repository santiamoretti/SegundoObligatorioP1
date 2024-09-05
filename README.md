![UCU Logo](https://upload.wikimedia.org/wikipedia/commons/6/63/UCU.png)

### Fecha límite: 06/06/2024 

### Se entrega por WebAsigantura

---

### Objetivo

En este proyecto, deberan implementar una version simple de la lógica del clásico juego de Buscaminas. 
Nosotros les proporcionamos la configuracion grafica del juego, todo lo demas deberá ser implementado por ustedes.

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
```


### Funciones de Interfaz Gráfica

'dibujar_tablero(tablero)' inicialamente recibe unicamente el tablero del juego. Observando las operaciones que se hacen dentro de dicha funcion, deberan inferir las caracteristicas que debera tener su tablero. Pueden modificar esta funcion a su conveniencia. 

'mostrar_mensaje(mensaje)' se encargara de desplegar el mensaje que informara al usuario la derrota o la victoria respectivamente.

```python
def dibujar_tablero(tablero, revelado):
    for fila in range(len(tablero)):
        for columna in range(len(tablero[0])):
            rectangulo = pygame.Rect(columna * tamano_celda, fila * tamano_celda, tamano_celda, tamano_celda)
            
            


def mostrar_mensaje(mensaje):
    fuente = pygame.font.Font(None, 72)
    texto = fuente.render(mensaje, True, NEGRO)
    rectangulo = texto.get_rect(center=(tamano_pantalla // 2, tamano_pantalla // 2))
    pantalla.blit(texto, rectangulo)
    pygame.display.flip()
    pygame.time.wait(2000)  
```
### main

El bucle principal del juego, se encarga de inicializarlo y de obtener las posiciones del mouse y su representacion en terminos de filas y columnas. Esto ultimo es fundamental para identificar la celda que el usuario destapado. Deben agregar logica a esta para lograr impelemntar lo que se pide.
```python

jugando = True
juego_terminado = False
while jugando:
    for evento in pygame.event.get():
        if evento.type == pygame.QUIT:
            jugando = False
        elif evento.type == pygame.MOUSEBUTTONDOWN and not juego_terminado:
            x, y = pygame.mouse.get_pos()
            columna, fila = x // tamano_celda, y // tamano_celda
            
           
           

    # Dibujar la imagen de fondo
    pantalla.blit(imagen_fondo, (0, 0))

    # Dibujar el tablero
    dibujar_tablero(tablero, revelado)
    pygame.display.flip()

pygame.quit()

```


### Video de la implementacion 

![Buscaminas Demo](./My%20Project.gif)



Santiago Amoretti
