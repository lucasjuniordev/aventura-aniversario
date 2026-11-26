# A Aventura da Aniversariante

Jogo de aniversário da Vitória: na manhã do aniversário, o escudeiro Lucas some e deixa pistas pela vila. Ela anda pelo mapa em tela cheia (joystick, setas/WASD ou toque no chão, com colisão nas construções e a câmera seguindo), cumpre um desafio com cada um dos 8 moradores, junta os 8 pedaços da carta e, no alto do castelo, encontra o prêmio: o próprio escudeiro, com a carta inteira e alguns vales.

No ar em https://aniversario.lucasjrdev.com

Nasceu como cópia da [Jornada da Aniversariante](https://github.com/lucasjuniordev/jornada-da-aniversariante) (a vila, os personagens e as artes); aqui não tem perguntas para adivinhar nem API.

## Roteiro

Tudo o que aparece na história fica no topo do `<script>` de `public/index.html`, no bloco **ROTEIRO**: prólogo, falas dos moradores, charadas, palavras do poeta, versículos, os 8 pedaços da carta e o final (título, prêmio e vales). Para mudar um texto, é só editar ali.

| Capítulo | Morador | Desafio |
| --- | --- | --- |
| 1 | Seu Bento, o Bilheteiro | 3 charadas de múltipla escolha |
| 2 | Dona Cida, a Relojoeira | parar o ponteiro na faixa dourada 3 vezes (fica mais rápido) |
| 3 | Dom Otávio, o Poeta | desembaralhar 3 palavras do casamento (ACASO, MILHÕES, INFINITO) |
| 4 | Lia, a Jardineira | quebra-cabeça 3x3 com o quadro do casal no jardim (trocar peças) |
| 5 | Tia Rosa, a Cozinheira | pegar 10 ingredientes de bolo em 40 s, sem cebola, pimenta ou alho |
| 6 | Tomé, o Mercador | jogo da memória com 6 pares |
| 7 | Pastor Lucas, pastor metodista ("Graça e Paz!") | completar 3 versículos de 1 Coríntios 13 |
| 8 | Gaspar, o Arauto | repetir a sequência das gemas (3 rodadas) |

Pela vila também passeiam o Theo, o Snow (cachorro) e a Paçoca (gata): toque neles para ver o que dizem. A ordem dos moradores na lista `NPCS` é a ordem dos capítulos. Theo, Snow e o Pastor Lucas são pessoas (e cachorro) de verdade, desenhados no Google Flow a partir de fotos.

O progresso fica salvo no navegador dela. Artes: Google Flow (mapa, personagens, retratos e a cena final). Som: `public/sons/fanfarra.mp3` ("Success Fanfare Trumpets", freesound_community no Pixabay).

## Rodar e publicar

Abrir `public/index.html` no navegador, ou `npx wrangler dev`. Cloudflare Workers só com assets estáticos; o Workers Builds publica cada push na `main`. O site fica fora das buscas (`noindex` e `X-Robots-Tag`).
