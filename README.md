# A Aventura da Aniversariante

Jogo de aniversário da Vitória: na manhã do aniversário, o escudeiro Lucas some e deixa pistas pela vila. Ela anda pelo mapa (toque no chão), cumpre um desafio com cada um dos 5 moradores, junta os 5 pedaços da carta e, no alto do castelo, encontra o prêmio: o próprio escudeiro, com a carta inteira e alguns vales.

No ar em https://aniversario.lucasjrdev.com

Nasceu como cópia da [Jornada da Aniversariante](https://github.com/lucasjuniordev/jornada-da-aniversariante) (a vila, os personagens e as artes); aqui não tem perguntas para adivinhar nem API.

## Roteiro

Tudo o que aparece na história fica no topo do `<script>` de `public/index.html`, no bloco **ROTEIRO**: prólogo, falas dos moradores, charadas, os 5 pedaços da carta e o final (título, prêmio e vales). Para mudar um texto, é só editar ali.

| Capítulo | Morador | Desafio |
| --- | --- | --- |
| 1 | Bilheteiro | 3 charadas de múltipla escolha |
| 2 | Relojoeira | parar o ponteiro na faixa dourada 3 vezes (fica mais rápido) |
| 3 | Cozinheira | pegar 10 ingredientes de bolo em 40 s, sem cebola, pimenta ou alho |
| 4 | Mercador | jogo da memória com 6 pares |
| 5 | Arauto | repetir a sequência das gemas (3 rodadas) |

O progresso fica salvo no navegador dela. Artes: Google Flow (mapa, personagens, retratos e a cena final). Som: `public/sons/fanfarra.mp3` ("Success Fanfare Trumpets", freesound_community no Pixabay).

## Rodar e publicar

Abrir `public/index.html` no navegador, ou `npx wrangler dev`. Cloudflare Workers só com assets estáticos; o Workers Builds publica cada push na `main`. O site fica fora das buscas (`noindex` e `X-Robots-Tag`).
