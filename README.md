import pygame
import sys

def main() :
    pygame.init()
    pygame.display.set_caption("첫번째 Pygame")
    screen = pygame.display.set_mode((800,600))
    clock = pygame.time.Clock()
    font = pygame.font.Font(None, 80)
    tmr = 0

    while True :
        tmr += 1
        for event in pygame.event.get() :
            if event.type == pygame.QUIT :
                pygame.quit()
                sys.exit()
        txt = font.render(str(tmr), True, WHITE)
        screen.fill(BLACK)
        screen.blit(txt, [300,200])
        pygame.display.update()
        clock.tick(10)

if __name__ = '__main__'
    main()
