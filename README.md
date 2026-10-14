# Shoukas-Assets

Os assets do Shoukas que ficam online, fora do repositório do código. Por enquanto, são os GIFs das
reações (abraçar, beijar...), que o bot mostra num embed, pelo link.

## Organização

`reactions/<reação>/<NNN>.gif`: os GIFs de cada reação, numerados a partir de 000, sem buracos. As
reações têm os nomes dos comandos: `bite`, `blush`, `cry`, `dance`, `facedesk`, `hug`, `kiss`,
`laugh`, `nope`, `pat`, `punch`, `run`, `slap` e `stare`.

## Como o bot os usa

O link de um GIF é
`https://raw.githubusercontent.com/<dono>/<repositório>/<commit>/reactions/<reação>/<NNN>.gif`,
com o commit fixado no código do Shoukas:

- um GIF novo só aparece quando o Shoukas passa a apontar para o commit que o trouxe;
- o link de um GIF já postado nunca muda.

O Discord guarda uma cópia de cada imagem que mostra, e o GitHub só é lido na primeira vez.

## As regras de um GIF

São as do `check_sizes.sh` da v3: um GIF de verdade, de pelo menos 400×200 pixels e no máximo 8
MB. Um GIF novo entra no fim da pasta da reação, com o próximo número.

## De onde vieram

Do [ShiroImageAPI](https://github.com/OtagamerZ/ShiroImageAPI), a API de imagens do ShiroJBot, de
Yago Gimenez (KuuHaKu), no último commit dela (`ace7619`, de 22/09/2021), publicados pelo
`tools/assets/publish-reactions.sh` do Shoukas. Mudaram só três coisas:

- `kiss/022.gif` era um WebP animado com nome de GIF e virou um GIF, com os mesmos quadros e
  tempos;
- `bite` não tinha o `025.gif`, e os GIFs seguintes desceram um número;
- a pasta `notfound`, a imagem da v3 para uma reação que não existia, ficou de fora.

Os GIFs são cenas de animes, e os direitos são dos estúdios deles. O ShiroImageAPI não tinha
licença.
