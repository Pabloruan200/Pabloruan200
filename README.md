import numpy as np
import matplotlib.pyplot as plt

# Criando um intervalo de valores para x e y
x = np.linspace(-2, 2, 400)
y = np.linspace(-2, 2, 400)

# Criando uma grade de valores de x e y
X, Y = np.meshgrid(x, y)

# Calculando os valores da equação para cada ponto na grade
Z = (X**2 + Y**2 - 1)**3 - X**2 * Y**3

# Plotando o gráfico
plt.figure(figsize=(8, 6))
plt.contour(X, Y, Z, levels=[0], colors='blue')
plt.title('Gráfico da equação (x^2 + y^2 - 1)^3 = x^2y^3')
plt.xlabel('x')
plt.ylabel('y')
plt.grid(True)
plt.axis('equal')
plt.show()
