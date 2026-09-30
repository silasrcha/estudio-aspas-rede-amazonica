# Estúdio Aspas Rede Amazônica

Monta o card de citação do debate da Rede Amazônica | Globo sobre foto: cole o
texto, escolha branco, azul ou escuro, envie a foto e baixe o PNG.

```bash
py -3 servidor.py        # http://localhost:8797
```

## Medidas

Vêm do Figma "DA Mídia — MR 2026", página "silas - edição", os três
ASPAS-DEBATE-29.09 (2549:525 branco, 2550:584 azul, 2550:611 escuro), cada um
num grupo com os dois adereços do topo. Estão em auto-layout: Conteúdo com
padding 35 / 57 / 41 / 72 e gap 37; o card de 808 cresce para baixo e a barra
lateral estica junto.

Diferenças em relação aos outros estúdios de aspas:

- o canto de baixo à direita tem raio 125 (os outros três, 25);
- o bloco do veículo encosta em 751, não em 741, e tem duas linhas de tamanhos
  diferentes: DEBATE em 27 e "REDE AMAZÔNICA | GLOBO" em 24 com entreletra −5%;
- os dois adereços do canto de cima à direita vêm do Figma como um SVG só
  (89 × 49), desenhado por cima do card e subindo 24,4 acima dele — por isso a
  posição do card reserva esse espaço.

O card fica em Work Sans com entreletra de −4% no texto: sem isso a quebra de
linha sai diferente do Figma.

## Prévia

Rolagem do mouse dá zoom na foto em volta do cursor; arrastar em cima do card
move ele só na vertical, com uma travadinha na posição padrão (80%) e uma guia
que só aparece durante o arraste; arrastar fora do card move a foto.

## Histórico

Os últimos 20 cards baixados ficam no IndexedDB do navegador
(`estudio-aspas-rede-amazonica`), com texto, cor, formato, foto (reduzida a
3000px) e ajustes. Clicar numa miniatura reabre o card; baixar de novo atualiza
o mesmo item. Cada pessoa vê o próprio histórico — o Pages não tem servidor.

## Autossuficiente

Nenhuma chamada externa. Fontes do card, foto de perfil e adereço embutidos no
`index.html`; a Encode Sans da interface vem de `ativos/fontes/`.
