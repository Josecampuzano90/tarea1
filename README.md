# tarea1
tarea
# Comparación entre Programación Tradicional y Programación Orientada a Objetos (POO) en Python

# Programación Tradicional

def ingresar_temperaturas():
    """Solicita las temperaturas diarias al usuario y las almacena en una lista."""
    temperaturas = []
    for dia in range(1, 8):
        temp = float(input(f"Ingrese la temperatura del día {dia}: "))
        temperaturas.append(temp)
    return temperaturas

def calcular_promedio(temperaturas):
    """Calcula el promedio de una lista de temperaturas."""
    return sum(temperaturas) / len(temperaturas)

def main_tradicional():
    """Función principal para ejecutar el programa usando programación tradicional."""
    print("--- Programa para calcular el promedio semanal de temperaturas ---")
    temperaturas = ingresar_temperaturas()
    promedio = calcular_promedio(temperaturas)
    print(f"El promedio semanal de temperaturas es: {promedio:.2f} °C")

# Llamada al programa tradicional
if __name__ == "__main__":
    main_tradicional()

# -----------------------------------------------------

# Programación Orientada a Objetos (POO)

class ClimaSemanal:
    """Clase que representa la información climática semanal."""

    def __init__(self):
        self.temperaturas = []

    def ingresar_temperaturas(self):
        """Solicita las temperaturas diarias al usuario y las almacena en el atributo temperaturas."""
        for dia in range(1, 8):
            temp = float(input(f"Ingrese la temperatura del día {dia}: "))
            self.temperaturas.append(temp)

    def calcular_promedio(self):
        """Calcula el promedio de las temperaturas almacenadas."""
        return sum(self.temperaturas) / len(self.temperaturas)

    def mostrar_promedio(self):
        """Muestra el promedio semanal de temperaturas."""
        promedio = self.calcular_promedio()
        print(f"El promedio semanal de temperaturas es: {promedio:.2f} °C")

def main_poo():
    """Función principal para ejecutar el programa usando POO."""
    print("--- Programa para calcular el promedio semanal de temperaturas (POO) ---")
    clima = ClimaSemanal()
    clima.ingresar_temperaturas()
    clima.mostrar_promedio()

# Llamada al programa POO
if __name__ == "__main__":
    main_poo()

# -----------------------------------------------------

# Comparación

# Programación Tradicional:
# - Enfocada en funciones y procedimientos.
# - Los datos (temperaturas) se manejan de manera global entre funciones.
# - Fácil de implementar para programas simples.

# Programación Orientada a Objetos:
# - Enfocada en clases y objetos que encapsulan datos y comportamientos.
# - Promueve la reutilización y escalabilidad del código.
# - Los datos (temperaturas) se manejan dentro de objetos, favoreciendo la modularidad.
