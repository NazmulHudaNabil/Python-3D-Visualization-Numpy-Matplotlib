# 3D Surface Plot using Python, NumPy & Matplotlib

This project demonstrates how to create a **3D surface plot** in Python using NumPy and Matplotlib.  
The plot visualizes the mathematical function:

\[
Z = \sin\left(\sqrt{X^2 + Y^2}\right)
\]

This generates a **radial wave pattern**, similar to ripples spreading outward from the center.

---

## 🔧 Technologies Used
- Python
- NumPy
- Matplotlib (mplot3d)

---

## 📌 Code Example

```python
import numpy as np
import matplotlib.pyplot as plt
from mpl_toolkits.mplot3d import Axes3D

x = np.linspace(-5, 5, 50)
y = np.linspace(-5, 5, 50)
X, Y = np.meshgrid(x, y)
Z = np.sin(np.sqrt(X**2 + Y**2))

fig = plt.figure()
ax = fig.add_subplot(111, projection="3d")
ax.plot_surface(X, Y, Z, cmap="viridis")
plt.show()
