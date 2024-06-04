Processamento de Imagens em Python
Este conjunto de scripts utiliza a biblioteca OpenCV para realizar várias operações de processamento de imagens. Abaixo estão as funcionalidades implementadas e uma breve explicação de cada uma.

Funcionalidades
1. Separação de Canais R, G e B
A função separa os canais de cor vermelho (R), verde (G) e azul (B) de uma imagem colorida e os exibe separadamente.

python
Copiar código
import cv2

# Carregar a imagem
img = cv2.imread('imagem.jpg')
# Separar os canais R, G e B
b, g, r = cv2.split(img)
# Exibir os canais separadamente
cv2.imshow('Canal R', r)
cv2.imshow('Canal G', g)
cv2.imshow('Canal B', b)
# Aguardar a tecla ESC para fechar as janelas
cv2.waitKey(0)
cv2.destroyAllWindows()

2. Conversão de RGB para Tons de Cinza
A função converte uma imagem colorida no espaço de cores RGB para uma imagem em tons de cinza.

python
Copiar código
import cv2

# Carregar a imagem
img = cv2.imread('imagem.jpg')
# Converter a imagem para tons de cinza
gray = cv2.cvtColor(img, cv2.COLOR_BGR2GRAY)
# Exibir a imagem em tons de cinza
cv2.imshow('Imagem em tons de cinza', gray)
# Aguardar a tecla ESC para fechar a janela
cv2.waitKey(0)
cv2.destroyAllWindows()

3. Conversão de Tons de Cinza para Preto e Branco (Limiarização/Binarização Manual)
A função converte uma imagem em tons de cinza para uma imagem binarizada em preto e branco utilizando um limiar definido.

python
Copiar código
import cv2

# Carregar a imagem em tons de cinza
gray = cv2.imread('imagem.jpg', cv2.IMREAD_GRAYSCALE)
# Definir o limiar
threshold = 128
# Aplicar a limiarização
_, binary = cv2.threshold(gray, threshold, 255, cv2.THRESH_BINARY)
# Exibir a imagem binarizada
cv2.imshow('Imagem binarizada', binary)
# Aguardar a tecla ESC para fechar a janela
cv2.waitKey(0)
cv2.destroyAllWindows()

4. Filtro da Média
A função aplica um filtro da média a uma imagem em tons de cinza, suavizando-a.

python
Copiar código
import cv2

# Carregar a imagem em tons de cinza
gray = cv2.imread('imagem.jpg', cv2.IMREAD_GRAYSCALE)
# Aplicar o filtro da média
blur = cv2.blur(gray, (5, 5))
# Exibir a imagem filtrada
cv2.imshow('Imagem filtrada', blur)
# Aguardar a tecla ESC para fechar a janela
cv2.waitKey(0)
cv2.destroyAllWindows()

5. Filtro da Mediana
A função aplica um filtro da mediana a uma imagem em tons de cinza, reduzindo o ruído de forma mais eficaz do que o filtro da média em alguns casos.

python
Copiar código
import cv2

# Carregar a imagem em tons de cinza
gray = cv2.imread('imagem.jpg', cv2.IMREAD_GRAYSCALE)
# Aplicar o filtro da mediana
median = cv2.medianBlur(gray, 5)
# Exibir a imagem filtrada
cv2.imshow('Imagem filtrada', median)
# Aguardar a tecla ESC para fechar a janela
cv2.waitKey(0)
cv2.destroyAllWindows()

6. Girar a Imagem 90 Graus
A função gira uma imagem 90 graus no sentido horário.

python
Copiar código
import cv2

# Carregar a imagem
img = cv2.imread('imagem.jpg')
# Girar a imagem 90 graus
rotated = cv2.rotate(img, cv2.ROTATE_90_CLOCKWISE)
# Exibir a imagem girada
cv2.imshow('Imagem girada', rotated)
# Aguardar a tecla ESC para fechar a janela
cv2.waitKey(0)
cv2.destroyAllWindows()

7. Inverter a Imagem (Horizontal/Vertical)
A função inverte a imagem horizontalmente e verticalmente.

python
Copiar código
import cv2

# Carregar a imagem
img = cv2.imread('imagem.jpg')
# Inverter a imagem horizontalmente
flipped_h = cv2.flip(img, 0)
# Inverter a imagem verticalmente
flipped_v = cv2.flip(img, 1)
# Exibir as imagens invertidas
cv2.imshow('Imagem invertida horizontalmente', flipped_h)
cv2.imshow('Imagem invertida verticalmente', flipped_v)
# Aguardar a tecla ESC para fechar as janelas
cv2.waitKey(0)
cv2.destroyAllWindows()

