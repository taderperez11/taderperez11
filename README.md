import matplotlib.pyplot as plt
import numpy as np

# Función
def f(x):
    return x**3 - 5*x**2 + 7*x - 10

# Puntos de mínimo y máximo
x1 = 2.33
y1 = 8.19
x2 = 1
y2 = -13

# Puntos de la función
x = np.linspace(-5, 5, 100)
y = f(x)

# Gráfica de la función
plt.plot(x, y, label='f(x) = x^3 - 5x^2 + 7x - 10')

# Punto de mínimo
plt.scatter(x1, y1, color='red', label='Mínimo')
plt.annotate('Mínimo', (x1, y1), xytext=(x1+0.5, y1+2), arrowprops=dict(arrowstyle='->', color='black'))

# Punto de máximo
plt.scatter(x2, y2, color='green', label='Máximo')
plt.annotate('Máximo', (x2, y2), xytext=(x2+0.5, y2-6), arrowprops=dict(arrowstyle='->', color='black'))

# Configuración de la gráfica
plt.axhline(0, color='black', linewidth=0.5)
plt.axvline(0, color='black', linewidth=0.5)
plt.grid(True, linestyle='--', alpha=0.7)
plt.legend()

# Mostrar gráfica
plt.show()
