![Kauê · Ferramentas para música e comunidades](assets/header.svg)

Sou o Kauê. Gosto da parte da programação em que uma ideia vira algo que dá para abrir e usar. Tenho trabalhado com bots de atendimento para Discord, automações e cardápios digitais. O projeto que estou desenvolvendo em público agora nasceu de uma pergunta: como voltar direto ao verso que eu quero ensaiar?

### Contracanto

Escolha um verso e a música volta até ele. O Contracanto transforma uma letra marcada em LRC em uma sala de ensaio que roda no navegador. A demo tem uma letra em português e doze segundos de acompanhamento instrumental.

**[Tocar a demo](https://ykauttiz.github.io/discord-lyrics-sync/)** · [Ver o código](https://github.com/ykauttiz/discord-lyrics-sync) · [Histórico de mudanças](https://github.com/ykauttiz/discord-lyrics-sync/blob/main/CHANGELOG.md)

**Por dentro do projeto**  
O Python organiza as marcações da letra e exporta legendas WebVTT. No navegador, o JavaScript acompanha a posição real do áudio para atualizar o verso depois de uma pausa ou de um salto na faixa. A interface usa HTML e CSS. Os testes cobrem desde refrões com timestamps repetidos até letras que contêm caracteres de marcação.

<details><summary>English</summary>

I’m Kauê. I build tools for music and online communities. My current project, Contracanto, turns a timestamped lyric sheet into an offline rehearsal room. Pick a line to seek, slow down the recording, or export WebVTT captions. [Try the instrumental demo](https://ykauttiz.github.io/discord-lyrics-sync/).

</details>
