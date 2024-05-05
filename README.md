import pygame
import sys
initialisation de pygame 
pygame.init()
#définir la taille de l’écran 
screen_width =800
screen_heigth=600
screen=pygame.dysplay.set_mode((screen_width,screen_heigth))
pygame.dysplay.set_caption("Mon premier jeu")
#couleurs
 Black(0,0,0)
 White 255,255,255)
 #classe pour le joueur 
 class player(pygame.sprite.Sprite:)
 super().__init__()
        self.image = pygame.Surface((50, 50))
        self.image.fill(WHITE)
        self.rect = self.image.get_rect()
        self.rect.center = (screen_width // 2, screen_height // 2)
        self.speed = 5

    def update(self):
        keys = pygame.key.get_pressed()
        if keys[pygame.K_LEFT]:
            self.rect.x -= self.speed
        if keys[pygame.K_RIGHT]:
            self.rect.x += self.speed
        if keys[pygame.K_UP]:
            self.rect.y -= self.speed
        if keys[pygame.K_DOWN]:
            self.rect.y += self.speed

# Groupe de sprites
all_sprites = pygame.sprite.Group()
player = Player()
all_sprites.add(player)

# Boucle principale du jeu
running = True
while running:
    for event in pygame.event.get():
        if ():event.type == pygame.QUIT:
            running = False
   
            running = False

    # Mise à jour
    all_sprites.update()

    # Dessin
    screen.fill(BLACK)
    all_sprites.draw(screen)
    
    # Rafraîchissement de l'écran
    pygame.display.flip()

    # Limite de framerate
    pygame.time.Clock().tick(60)

# Quitter Pygame
pygame.quit()
sys.exit() 



<!---
Makthisr7/Makthisr7 is a ✨ special ✨ repository because its `README.md` (this file) appears on your GitHub profile.
You can click the Preview link to take a look at your changes.
--->
