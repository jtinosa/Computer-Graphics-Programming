## Computer Graphics
- A field of computer science that focuses on the creation, manipulation, and representation of visual images and animations using computers.

## Major Areas of Computer Graphics
1. **Modeling** refers to the process of creating a mathematical representation of a 3D object or shape.
2. **Rendering** refers to the process of generating an image from a model.
   - **Raster Graphics**
    - A **raster** is an array of pixels displayed on a screen, arranged in a grid with two dimensions.
    - A **pixel** is the smallest unit of a digital image or graphic that can be displayed. It specify colors using triples of floating-point numbers between 0 and 1, which represent the amount of red, green, and blue light existing in a color. A pixel value of 0 indicates that no amount of that color exists, while a value of 1 represents that color is displayed at full intensity.
    - The quality of an image depends partly on its **resolution** and **precision**.
    - **Resolution** refers to the number of pixels in an image, typically described in terms of the width and height of the image in pixels (e.g., 1920x1080).
    - **Precision** is the number of bits used for each pixel. Higher precision allows for more accurate and subtle variations in color and intensity, leading to more realistic and detailed images.
  - **Framebuffers and Buffers**
    - **Buffer:** Temporary storage for data during transfers.
    - **Framebuffer:** Memory region storing pixel data.
      - **Color Buffer:** Stores RGB values.
      - **Depth Buffer:** Stores distances from scene objects to the camera.
      - **Stencil Buffer:** Used for advanced effects like shadows and reflections.
4. **Animation** is the process of creating the illusion of motion by displaying a sequence of images or frames.
  - **Frame:** Each individual image in the sequence.
  - **Frame Rate:** Speed or rate at which images appear.
  - **Frames Per Second (FPS)** unit used to measure the frame rate.

## Major Applications of Computer Graphics
1. **Video Games** increasingly use sophisticated 3D models and rendering algorithms.
2. **Cartoons** are often rendered directly from 3D models. Many traditional 2D cartoons use backgrounds rendered from 3D models, which allow a continuously moving viewpoint without huge amounts of artist time.
3. **Visual effects** use almost all types of computer graphics technology. Almost every modern film uses digital compositing to superimpose backgrounds with separately filmed foregrounds. Many films also use 3D modeling and animation to create synthetic environments, objects, and even characters that most viewers will never suspect are not real.
4. **Animated films** use many of the same techniques that are used for visual effects, but without necessarily aiming for images that look real.

## Graphics API
- A set of functions that perform basic operations such as drawing images and 3D surfaces into windows on the screen.
- Every graphics program needs to be able to use two related APIs: **a graphics API for visual output** and **a user-interface API to get input from the user**.

## Graphics Pipeline
- An abstract model used to describe a sequence of steps needed in rendering a three-dimensional scene.
- It enables a computational task to be split into subtasks thus increasing overall efficiency.

