# A Aventura da Aniversariante

Jogo de aniversário da Vitória: na manhã do aniversário, o escudeiro Lucas some e deixa pistas pela vila. Ela anda pelo mapa em tela cheia (joystick, setas/WASD ou toque no chão, com colisão nas construções e a câmera seguindo), cumpre um desafio com cada um dos 8 moradores, junta os 8 pedaços da carta e, no alto do castelo, encontra o prêmio: o próprio escudeiro, com a carta inteira e alguns vales.

No ar em https://aniversario.lucasjrdev.com

Nasceu como cópia da [Jornada da Aniversariante](https://github.com/lucasjuniordev/jornada-da-aniversariante) (a vila, os personagens e as artes); aqui não tem perguntas para adivinhar nem API.

## Roteiro

Tudo o que aparece na história fica no topo do `<script>` de `public/index.html`, no bloco **ROTEIRO**: prólogo, falas dos moradores, charadas, palavras, versículos, os 8 pedaços da carta e o final (título, prêmio e vales). Para mudar um texto, é só editar ali.

Os moradores são a família, cada um lembrando o que fez no casamento (01/08/2026): o caminho da vila até o castelo é como o caminho até o altar.

| Capítulo | Quem | No casamento | Desafio |
| --- | --- | --- | --- |
| 1 | Seu Diego, pai da noiva | entrou com ela | 3 charadas (uma clássica e duas do casamento) |
| 2 | Dona Fran, mãe da noiva | entrou com ela (A Thousand Years) | parar o ponteiro na faixa dourada 3 vezes |
| 3 | Randerson, irmão e padrinho | padrinhos entraram com Amigo, Estou Aqui | desembaralhar ACASO, MILHÕES e INFINITO |
| 4 | Radmila, irmã e madrinha (mãe do Theo) | madrinha | quebra-cabeça 3x3 com o quadro do casal |
| 5 | Henrique, pajem da placa | placa "lá vem a noiva" e alianças com o Theo | jogo da memória com 6 pares |
| 6 | Pastora Luzia, pastora e cantora | celebrou e cantou Bondade de Deus | repetir a melodia das gemas (3 rodadas) |
| 7 | Pastor Lucas, pastor metodista ("Graça e Paz!") | celebrou | completar 3 versículos de 1 Coríntios 13 |
| 8 | Cayo, o padrinho mais top (arauto do castelo) | padrinho | pegar 10 ingredientes de bolo em 40 s |

Pela vila também passeiam o Theo, o Snow (cachorro) e a Paçoca (gata): toque neles para ver o que dizem. A ordem da lista `NPCS` é a ordem dos capítulos. Theo, Snow e o Pastor Lucas já têm desenho feito no Google Flow a partir de fotos; os outros ainda usam os desenhos antigos dos moradores até chegarem as fotos. Se a personagem não consegue ir reto até alguém (uma construção no meio), ela passa antes por pontos da estrada de pedras (`ESTRADA`).

O progresso fica salvo no navegador dela. Artes: Google Flow (mapa, personagens, retratos e a cena final). Som: `public/sons/fanfarra.mp3` ("Success Fanfare Trumpets", freesound_community no Pixabay).

## Rodar e publicar

Abrir `public/index.html` no navegador, ou `npx wrangler dev`. Cloudflare Workers só com assets estáticos; o Workers Builds publica cada push na `main`. O site fica fora das buscas (`noindex` e `X-Robots-Tag`).
