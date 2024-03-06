# This code is created to learn about pygame library in Python

# Pip install pygame

Pygame is a Python library for dealing with game 2D.

## Installation

Use the package manager [pip](https://pip.pypa.io/en/stable/) to install pygame.

```bash
pip install pygame
```

## Usage

```python
# Import and initialize the pygame library
import pygame
pygame.init()

# Set up the drawing window
screen = pygame.display.set_mode([500, 500])

# Run until the user asks to quit
running = True
while running:

    # Did the user click the window close button?
    for event in pygame.event.get():
        if event.type == pygame.QUIT:
            running = False

    # Fill the background with white
    screen.fill((255, 255, 255))

    # Draw a solid blue circle in the center
    pygame.draw.circle(screen, (0, 0, 255), (250, 250), 75)

    # Flip the display
    pygame.display.flip()

# Done! Time to quit.
pygame.quit()
```

# Brief explanation programe
## The program includes 5 classes:
 - Dot: this is the layer to create bright spots in fireworks
- Bullet: creates light spots when starting to fly up from the bottom of the program window
- BulletFlyUp: used to create movement for light spots when flying
- FireWork: creates fireworks including Bullets
- Random: initializes parameters such as color, number of fireworks, speed of fireworks when flying and exploding and their x position
- main function: initializes the basic parameters of the program and executes the program in the while True loop
## Attached files
- To make the program have more sound, we will use file.wav

```python
# Load file 
pygame.mixer.music.load('music.mp3')
# Set volume if you want to adjust
pygame.mixer.music.set_volume(0.4)
```
- When the timer starts counting to 0, a sound will be played
```python
while countdown_time > 0:
	DISPLAYSURF.fill((0, 0, 0))
	text = font.render(str(countdown_time), True, (255, 255, 255))
	text_rect = text.get_rect()
	text_rect.center = (WINDOWWIDTH/2, WINDOWHEIGHT/2)
	DISPLAYSURF.blit(text, text_rect)
	pygame.display.flip()
	countdown_time -= 1
	pygame.time.wait(1000)
	if countdown_time < 1:
		pygame.mixer.music.play()
```
😋 If you have any question, please don't hesitate to contact me via email: minh9thanh@gmail.com
# License

[MIT](https://choosealicense.com/licenses/mit/)
