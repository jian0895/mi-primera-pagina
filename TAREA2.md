
```python
import turtle
# Importa la librería turtle, que permite dibujar gráficos en una ventana.

def dibujar_escalera(escalones, tamaño):
    # Define una función que dibuja una escalera con el número de escalones y tamaño indicados.
    print("Iniciando dibujo de la escalera...")
    
    t = turtle.Turtle()  # Crea una tortuga para dibujar.
    t.speed(1)           # Ajusta la velocidad de la tortuga (1 = lento, 10 = rápido).
    
    # Bucle para dibujar cada escalón
    for _ in range(escalones):
        t.forward(tamaño)  # Dibuja el paso horizontal del escalón.
        t.right(90)        # Gira 90° a la derecha para comenzar el paso vertical.
        t.forward(tamaño)  # Dibuja el paso vertical del escalón.
        t.left(90)         # Gira 90° a la izquierda para volver a la orientación original.
    
    print("Escalera completada.")  # Mensaje cuando termina el dibujo.

# Pedir datos al usuario
escalones = int(input("¿Cuántos escalones quieres dibujar? "))
# Convierte el valor ingresado a entero.

tamaño = int(input("¿Cuánto debe medir cada escalón? (elige un valor entero entre 40 y 60) "))
# Convierte el tamaño ingresado a entero.

# Llamar la función con los valores ingresados
dibujar_escalera(escalones, tamaño)# Dibuja la escalera con los parámetros proporcionados por el usuario.

# Mostrar información adicional al usuario
print("El número de escalones es:", escalones)  # Imprime la cantidad de escalones.

print("El tamaño de cada escalón es:", tamaño)  # Imprime el tamaño de cada escalón.

# Finaliza el dibujo y mantiene la ventana abierta
turtle.done()

