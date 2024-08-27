## Pygame and OpenGL
- Based on the graphics pipeline, the first step to render graphics is to develop
an application where the graphics will be displayed.

- A window is a graphical interface element that displays an application’s
content. Below are the phases of an interactive and graphics-based windowed
application.

  1. Startup: During this stage, objects are created, values are initialized,
      and any required external files are loaded.
  2. Main Loop: This stage repeats continuously while the application is
      running. It consists of the following three (3) substages:
      - Process Input – checks if the user has performed any action that
         sends data to the computer, such as pressing keys on a keyboard
         or clicking buttons on a mouse.
      - Update – changes values of variables and objects.
      - Render – creates graphics that are displayed on the screen.
  3. Shutdown: This stage typically begins when the user performs an
      action indicating that the program should stop (for example, by clicking
      a button to quit the application). This stage may involve tasks such as
      signaling the application to stop checking for user input and closing
      any windows created by the application.

## Pygame 
- Pygame is a set of Python modules designed for creating video games. It is a
popular Python game development library.

```
# Example code showing a circle moving on screen
import pygame

# pygame setup
pygame.init()
screen = pygame.display.set_mode((1280, 720))
clock = pygame.time.Clock()
running = True
dt = 0

player_pos = pygame.Vector2(screen.get_width() / 2, screen.get_height() / 2)

while running:
    # poll for events
    # pygame.QUIT event means the user clicked X to close your window
    for event in pygame.event.get():
        if event.type == pygame.QUIT:
            running = False

    # fill the screen with a color to wipe away anything from last frame
    screen.fill("purple")

    pygame.draw.circle(screen, "red", player_pos, 40)

    keys = pygame.key.get_pressed()
    if keys[pygame.K_w]:
        player_pos.y -= 300 * dt
    if keys[pygame.K_s]:
        player_pos.y += 300 * dt
    if keys[pygame.K_a]:
        player_pos.x -= 300 * dt
    if keys[pygame.K_d]:
        player_pos.x += 300 * dt

    # flip() the display to put your work on screen
    pygame.display.flip()

    # limits FPS to 60
    # dt is delta time in seconds since last frame, used for framerate-
    # independent physics.
    dt = clock.tick(60) / 1000

pygame.quit()

```

## OpenGL
- OpenGL (Open Graphics Library) is a cross-platform, open-standard API used for rendering 2D and 3D vector graphics.
- OpenGL provides a set of functions that allow developers to specify the geometry, texture, lighting, and other properties of objects. These functions interact with the GPU to render images on the screen.

```
import pygame
from pygame.locals import *
from OpenGL.GL import *
from OpenGL.GLU import *
import time

# Vertices of the triangle
vertices = (
    (1, -1, -1),
    (1, 1, -1),
    (-1, 1, -1),
)

# Colors for each vertex
colors = (
    (1, 0, 0),  # Red
    (0, 1, 0),  # Green
    (0, 0, 1),  # Blue
)

def draw_triangle():
    glBegin(GL_TRIANGLES)
    for i in range(3):
        glColor3fv(colors[i])
        glVertex3fv(vertices[i])
    glEnd()

def main():
    pygame.init()
    display = (800, 600)
    pygame.display.set_mode(display, DOUBLEBUF | OPENGL)

    gluPerspective(45, (display[0] / display[1]), 0.1, 50.0)
    glTranslatef(0.0, 0.0, -5)

    angle = 0
    while True:
        for event in pygame.event.get():
            if event.type == pygame.QUIT:
                pygame.quit()
                quit()

        glRotatef(angle, 0, 1, 0)  # Rotate around the Y axis
        glClear(GL_COLOR_BUFFER_BIT | GL_DEPTH_BUFFER_BIT)
        draw_triangle()
        pygame.display.flip()
        pygame.time.wait(10)

        angle += 1  # Increment the angle for rotation

if __name__ == "__main__":
    main()

```


