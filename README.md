# Shoukas-Assets

Os assets do Shoukas que ficam online, fora do repositório do código: os GIFs das reações
(abraçar, beijar...) e os das falas das cartas nas partidas do Shoukan, que o bot mostra num
embed, pelo link.

## Organização

- `reactions/<reação>/<NNN>.gif`: os GIFs de cada reação, numerados a partir de 000, sem buracos.
  As reações têm os nomes dos comandos: `bite`, `blush`, `cry`, `dance`, `facedesk`, `hug`, `kiss`,
  `laugh`, `nope`, `pat`, `punch`, `run`, `slap` e `stare`.
- `shoukan/<nome>.gif`: o GIF que uma carta mostra quando fala numa partida, com o nome que o
  efeito dela dá, como `rod_from_god` ou `za_warudo`.

## Como o bot os usa

O link de um GIF é `https://raw.githubusercontent.com/<dono>/<repositório>/<commit>/<caminho>`,
com o commit fixado no código do Shoukas:

- um GIF novo só aparece quando o Shoukas passa a apontar para o commit que o trouxe;
- o link de um GIF já postado nunca muda.

O Discord guarda uma cópia de cada imagem que mostra, e o GitHub só é lido na primeira vez.

## As regras de um GIF

- **As reações:** as do `check_sizes.sh` da v3: um GIF de verdade, de pelo menos 400×200 pixels e
  no máximo 8 MB. Um GIF novo entra no fim da pasta da reação, com o próximo número.
- **As falas das cartas:** um GIF de verdade, com o nome que o efeito da carta dá. O maior tem 9,9
  MB, e o Discord o mostra.

## De onde vieram

- **As reações:** do [ShiroImageAPI](https://github.com/OtagamerZ/ShiroImageAPI), a API de imagens
  do ShiroJBot, de Yago Gimenez (KuuHaKu), no último commit dela (`ace7619`, de 22/09/2021),
  publicados pelo `tools/assets/publish-reactions.sh` do Shoukas. Mudaram só três coisas:
  - `kiss/022.gif` era um WebP animado com nome de GIF e virou um GIF, com os mesmos quadros e
    tempos;
  - `bite` não tinha o `025.gif`, e os GIFs seguintes desceram um número;
  - a pasta `notfound`, a imagem da v3 para uma reação que não existia, ficou de fora.
- **As falas das cartas:** do [ShoukanAssets](https://github.com/OtagamerZ/ShoukanAssets), os
  assets do Shoukan do ShiroJBot, do mesmo autor, no último commit dele (`da7088f`, de 18/06/2024),
  publicados pelo `tools/assets/publish-quotes.sh` do Shoukas, como estavam lá. Vieram os 39 GIFs
  que os efeitos das cartas usam; os outros 10 da pasta `gifs`, que nenhum efeito usa, ficaram de
  fora.

Os GIFs são cenas de animes, e os direitos são dos estúdios deles. O ShiroImageAPI e o
ShoukanAssets não tinham licença.
