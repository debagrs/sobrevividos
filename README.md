# Sobrevividos

Mostra virtual de História da Arte I, Bacharelado em Desenho Industrial, UFSM, semestre 2026/2.
Concepção e curadoria: Profa. Dra. Débora Aita Gasparetto.

## Os três atos

1. **Constelações**: a plataforma de montagem de imagens ([constelacoes-gray.vercel.app](https://constelacoes-gray.vercel.app/)).
2. **Redesenhar**: desenhos feitos só a partir da descrição escrita por um colega, sem ver a obra de partida.
3. **Atlas Mnemosyne**: os painéis da turma e as peças de design que nasceram deles.

Depois dos atos vêm os podcasts, as pessoas que participaram e um spoiler do próximo semestre.

## Estrutura

```
index.html   página única: estilos, conteúdo e scripts
img/         desenhos do Redesenhar, já enquadrados (redesenho-01.jpg a redesenho-17.jpg)
audio/       lugar da gravação do texto curatorial
```

É um site estático: não tem etapa de build. No Vercel, importe o repositório com o preset **Other** e publique.

## Como editar o conteúdo

O conteúdo fica num bloco no início do `<script>` do `index.html`, marcado como `CONTEÚDO DA MOSTRA`:

- `OBRAS`: desenhos do Ato II. Para cada um, preencha `autoria` e `obraDePartida`. Quando preenchidos, eles aparecem na legenda.
- `ATLAS`: atlas do Ato III, com título, autoria, pergunta, trecho do texto crítico, até 7 imagens do painel e a peça projetada.
- `PESSOAS`: retrato, nome e links de quem participou.
- `PODCASTS`: episódios. Com `link` vazio, o episódio abre a pasta da disciplina.
- `AUDIO_CURADORIA`: caminho da gravação do texto curatorial, por exemplo `"audio/curadoria.mp3"`. Com o campo vazio, a leitura usa a voz do navegador.

Uma imagem nova vai para `img/`, e o caminho entra na lista, por exemplo `img/atlas-ana-01.jpg`.
