# Floresta Sombria 

Um carrossel interativo que conta lendas do folclore brasileiro — do Curupira à Matinta Perera, passando pelo Boto Cor-de-Rosa, Mapinguari, Sereia Iara e Caipora.

Feito com HTML, CSS e JavaScript puro, sem frameworks ou bibliotecas externas.

## O que rolou por aqui

Esse projeto começou como um experimento de carrossel, e ao longo do caminho fui ajustando um monte de coisa até ficar do jeito que queria. As principais mudanças:

### Bugs que apareceram (e foram resolvidos)

- **Auto-play fantasma** — o slide avançava sozinho porque duas variáveis (`timeAutoNext` e `runAutoRun`) simplesmente não tinham sido declaradas. O navegador gritava `ReferenceError` e ninguém entendia por quê.
- **Thumbnail desaparecendo** — quando você clicava pra passar o slide, a primeira prévia sumia e depois voltava do nada. Era uma animação CSS que reiniciava do zero toda vez que o JavaScript mexia nos elementos.
- **Barra laranja sem sentido** — tinha uma barrinha de progresso que ficava enchendo e depois sumia, mas o slide não esperava ela terminar. Decidi tirar de vez.
- **Transição voltando** — no "voltar", o card ficava meio perdido, tentando se esconder atrás da imagem principal. Ajustei as camadas e as animações pra ficar suave dos dois lados.

### O que melhoramos

- **Transições mais suaves** — tanto indo pra frente quanto voltando, os slides e thumbnails se movem juntos, sem aquele pulo estranho.
- **Código mais limpo** — variáveis sem uso foram embora, animation keys que não serviam pra nada foram deletadas, e o JavaScript ficou mais direto.
- **Responsividade** — as thumbnails agora se adaptam em telas menores (celular), sem quebrar o layout.
- **Acessibilidade** — todas as imagens ganharam `alt` descritivo, e a indentação do HTML foi organizada.
- **Carregamento** — as primeiras imagens são pré-carregadas pra não ficar aquele flash branco na primeira vez.

### O que saiu

- Auto-play
- Barra de progresso laranja
- Código morto (keyframes e variáveis que não eram usadas)
- Thumbnail duplicada e descriptions vazias no HTML

## Como usar

Só abrir o `index.html` no navegador. Não precisa instalar nada.

```
git clone https://github.com/JanesDays/Floresta.Sombria.git
cd Floresta.Sombria
start index.html
```

## Tecnologias

- HTML5 — estrutura semântica
- CSS3 — animações, flexbox, variáveis, responsivo
- JavaScript — manipulação do DOM, eventos, temporizadores

## Sobre

Projeto feito como parte do aprendizado em desenvolvimento web, unindo técnica com a riqueza das lendas brasileiras. Se quiser trocar uma ideia sobre o código ou sugerir melhorias, fica à vontade.
