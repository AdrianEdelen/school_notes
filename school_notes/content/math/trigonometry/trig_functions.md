---
jupytext:
  cell_metadata_filter: -all
  formats: md:myst
  text_representation:
    extension: .md
    format_name: myst
    format_version: 0.13
    jupytext_version: 1.11.5
kernelspec:
  display_name: Python 3
  language: python
  name: python3
---
# trigonometric functions

There are six trigonometric functions :

- Sine      (sin)
- Cosine    (cos)
- Tangent   (tan)
- Secant    (sec)
- Cosecant  (csc)
- Cotangent (cot)

The functions are defined as ratios of sides of a triangle. That is to say, that given an angle θ (theta), a right angle triangle is constructed, the given function of the angle is a ratio of two of the sides of this triangle.

```(code-cell) Python
import matplotlib.pyplot as plt
import numpy as np

# Coordinates for the triangle vertices
triangle_coords = np.array([[0, 0], [4, 0], [2, 3]])

# Plot the triangle
fig, ax = plt.subplots()
ax.plot([triangle_coords[0][0], triangle_coords[1][0]], 
        [triangle_coords[0][1], triangle_coords[1][1]], 'k-')
ax.plot([triangle_coords[1][0], triangle_coords[2][0]], 
        [triangle_coords[1][1], triangle_coords[2][1]], 'k-')
ax.plot([triangle_coords[2][0], triangle_coords[0][0]], 
        [triangle_coords[2][1], triangle_coords[0][1]], 'k-')

# Label the vertices
ax.text(triangle_coords[0][0] - 0.2, triangle_coords[0][1] - 0.2, 'A', fontsize=12)
ax.text(triangle_coords[1][0] + 0.2, triangle_coords[1][1] - 0.2, 'B', fontsize=12)
ax.text(triangle_coords[2][0], triangle_coords[2][1] + 0.2, 'C', fontsize=12)

# Label the sides
ax.text(2, -0.3, 'AB', fontsize=12)
ax.text(3, 1.5, 'BC', fontsize=12)
ax.text(0.5, 1.5, 'CA', fontsize=12)

# Set limits and aspect ratio
ax.set_xlim(-1, 5)
ax.set_ylim(-1, 4)
ax.set_aspect('equal')

# Hide axes
ax.axis('off')

# Show the plot
plt.show()
```

