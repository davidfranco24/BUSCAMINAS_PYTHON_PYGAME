# BUSCAMINAS_PYTHON_PYGAME
Documento explicativo del código
Requisitos
• Python 3.x
• Juego Py
Estructura del código
Importación de bibliotecas
• import pygame
• import random
• import sys
Variables Globales
• primera_celda_pulsada: Indica si la primera celda ha sido pulsada.
• calidades_casilla: Diccionario que almacena información sobre cada 
celda.
• bombas_restantes: Número de bombas que quedan por marcar.
• bombas_correctas: Número de bombas marcadas correctamente.
• puntos: Puntuación del jugador.
Funciones
crear_cuadricula(numero, tamaño_cuadricula)
Crea la cuadrícula del juego.
• Args:
o numero (int): Número de filas y columnas de la cuadrícula.
o tamaño_cuadricula (int): Tamaño de cada celda de la cuadrícula.
crear_bombas_random(numero, primer_click, dificultad)
Coloca bombas de forma aleatoria en la cuadrícula, asegurando que no se 
coloquen alrededor del primer clic del jugador.
• Args:
o numero (int): Número de filas y columnas de la cuadrícula.
o primer_click (tuple): Índice (fila, columna) del primer clic del 
jugador.
o dificultad (float): Factor de dificultad que determina el número de 
bombas.
donde_ahy_bombas()
Calcula el número de bombas adyacentes a cada celda de la cuadrícula.
color_numero(element, color)
Dibuja el número de bombas adyacentes en una celda específica.
• Args:
o element (int): Número de celda.
o color (tuple): Color del texto.
click_casilla(numero, event, dificultad)
Maneja los clics del ratón en las celdas del juego.
• Args:
o numero (int): Número de filas y columnas de la cuadrícula.
o event (pygame.event): Evento del clic del ratón.
o dificultad (float): Factor de dificultad que determina el número de 
bombas.
• Returns:
o tuple: Indicadores de victoria y derrota.
menu()
Muestra el menú principal del juego y permite seleccionar la dificultad.
• Returns:
o tuple: Número de filas/columnas, dificultad y tamaño de celdas.
mostrar_bombas(numero, casillas)
Muestra el número de bombas restantes en la interfaz.
• Args:
o numero (int): Número de filas y columnas de la cuadrícula.
o casillas (int): Tamaño de cada celda.
mostrar_puntos()
Muestra los puntos actuales en la interfaz.
game(numero, dificultad, casillas)
Maneja el ciclo principal del juego.
• Args:
o numero (int): Número de filas y columnas de la cuadrícula.
o dificultad (float): Factor de dificultad que determina el número de 
bombas.
o casillas (int): Tamaño de cada celda.
run()
Inicia el juego y gestiona el menú y la cuadrícula inicial.
Estructura del Juego
1. Inicio: El juego inicia llamando a la función run(), que muestra el menú y 
permite seleccionar la dificultad.
2. Menú: La función menu() permite al jugador seleccionar la dificultad del 
juego.
3. Creación de la Cuadrícula: Basado en la selección del jugador, se 
llama a crear_cuadricula().
4. Juego Principal: El ciclo principal del juego se maneja en la función 
game(), que llama a click_casilla() para manejar los clics del ratón.
5. Mostrar Bombas y Puntos: Durante el juego, mostrar_bombas() y 
mostrar_puntos() actualizan la interfaz con el número de bombas 
restantes y los puntos del jugador.
6. Final del Juego: El juego termina cuando el jugador gana o pierde, y se 
reinicia llamando a run() nuevamente.
Consideraciones de Dificultad
La dificultad del juego se ajusta mediante el factor dificultad, que determina el 
número de bombas en la cuadrícula:
• Fácil: Menos bombas.
• Normal: Número moderado de bombas.
• Difícil: Más bombas.
Ejecución del Código
Para ejecutar el código, se debe tener instalada la biblioteca Pygame. El script 
se puede ejecutar directamente desde la línea de comandos o un entorno de 
desarrollo Python.
