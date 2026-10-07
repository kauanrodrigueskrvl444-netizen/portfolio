# Portfólio, Kauã Rodrigues

Site estático de página única. Sem build, sem dependência e sem framework:
HTML, CSS, SVG embutido e um bloco de script no fim do arquivo.

No ar em [kauarodrigues.netlify.app](https://kauarodrigues.netlify.app/)

```
index.html              o site inteiro
assets/kr.png           monograma KR, favicon e navbar
assets/kaua.jpg         retrato do hero
assets/capa.jpg         imagem de prévia ao compartilhar o link (Open Graph)
assets/grade-chao.svg   grade em perspectiva do fundo
assets/projetos/        prints dos projetos (1280x800, JPG)
```

## Seções

1. Hero, com nome, resumo, botões e stack
2. Projetos, Açaí Ki Delícia em destaque com dois prints e outros três com capa
3. Stack, quatro blocos com o estágio real de cada um
4. Sobre e formação, com as metas
5. Serviços, bloco curto que leva pro site da Rodrigues Soluções Digitais
6. Contato, cinco canais

Títulos em Playfair Display (serifa do logo), corpo em Inter.

## Como mexer

**Contato.** Tudo vem de constantes no fim do `index.html`. Trocar ali atualiza
navbar, cards e rodapé de uma vez.

```js
const WHATSAPP  = "5511932391284";
const EMAIL     = "kauanrodrigueskr90@gmail.com";
const GITHUB    = "https://github.com/kauanrodrigueskrvl444-netizen";
const LINKEDIN  = "https://www.linkedin.com/in/...";
const INSTAGRAM = "https://www.instagram.com/rdkz07/";
```

Canal com valor vazio some da tela em vez de virar link quebrado.

**Medidas e cores.** Ficam em `:root`, no topo do CSS. Espaçamento do hero,
altura dos botões, diâmetro da foto, força do brilho e a paleta inteira.

**Foto.** Substituir `assets/kaua.jpg`. Qualquer proporção serve, o CSS recorta
no círculo. Manter abaixo de 200 KB.

## Animações

Abertura de 2 segundos, entrada escalonada do hero e revelação ao rolar.
Tudo desliga sozinho para quem tem `prefers-reduced-motion` ligado no sistema.
As classes que escondem são aplicadas por JavaScript, nunca no HTML, então sem
script a página aparece inteira em vez de ficar em branco.

## Ver localmente

```
node ../../scripts/servidor-local.js . 4175
```

## Publicar

Push na `main`. O Netlify publica sozinho.

## Pendências

- [ ] Período atual da faculdade e previsão de conclusão
- [ ] Confirmar as três metas (escritas a partir de conversa, marcadas com `CONFIRMAR` no HTML)
- [ ] Email em domínio próprio no lugar do Gmail
- [ ] Domínio próprio apontando para o site
