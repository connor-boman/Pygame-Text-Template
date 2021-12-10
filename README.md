# Pygame-Text-Template
You may use this code (Exercise 3 on the graphical content assignment) as a base to help in programming the text into the phase 1 project. 

import pygame
pygame.init()
WHITE = (255, 255, 255)
BLACK=(0,0,0)
RED=(255,0,0)
GREEN=(0,255,0)
BLUE=(0,0,255)
pygame.display.set_mode(size=(0, 0), flags=0, depth=0, display=0)
scn_width=800
scn_height=500
screen=pygame.display.set_mode((scn_width,scn_height))
screen.fill(WHITE)
print(pygame.font.get_fonts())
font = pygame.font.SysFont("freesans", 72)
text = font.render("Game Time!",True,BLACK)
tw = text.get_width()
th = text.get_height()
screen.blit(text, [0, 0])
screen.blit(text, [scn_width / 2 -tw / 2, scn_height / 2 -th / 2])
screen.blit(text, [scn_width -tw, scn_height -th])
pygame.display.flip()           # Display screen
