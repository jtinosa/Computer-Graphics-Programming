## Graphics Pipeline
- An abstract model used to describe a sequence of steps needed in rendering a three-dimensional scene.
- It enables a computational task to be split into subtasks thus increasing overall efficiency.

## Stages of Graphics Pipeline
1. **Application** – initializing the window where rendered graphics will be displayed; sending data to the GPU.
2. **Geometry Processing** – determining the position of each vertex of the geometric shapes to be rendered, implemented by a program known as vertex shader.
3. **Rasterization** – determining which pixels correspond to the geometric shapes to be rendered.
4. **Pixel Processing** – determining the color of each pixel in the rendered image, involving a program called a fragment shader.

