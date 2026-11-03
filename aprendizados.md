# Aprendizados

## HTML semântico
Usar tags que dizem O QUE cada parte da página é, e não como ela aparece.
Não muda nada no visual, mas ajuda leitores de tela, o Google e o CSS.

## As caixas principais
- header: identidade do site (nome, logo). Se repete em todas as páginas.
- main: o conteúdo principal, o motivo da página existir. Só um por página.
- section: um bloco com tema próprio dentro do conteúdo. Geralmente tem um título (h2).
- footer: rodapé, informações finais (contato, direitos).

Teste prático: "esse elemento apareceria igual em todas as páginas do site?"
- Sim → header ou footer
- Não → main

## Regra das caixas
Tags são caixas uma dentro da outra.
A última que abriu é a primeira que fecha.
Não dá para fechar a caixa grande com a pequena ainda aberta.

## Dicas do VS Code
- Shift + Alt + F: formata o documento e organiza o recuo.
  Se ficar estranho, tem tag fora do lugar.
- Tab / Shift + Tab: aumenta ou diminui o recuo das linhas selecionadas.

## O esqueleto do HTML
- <!DOCTYPE html>: avisa ao navegador que é HTML moderno. Sempre a primeira linha.
- <html lang="pt-BR">: caixa que envolve tudo. O lang diz o idioma da página.
- <head>: informações sobre a página. Nada aqui aparece na tela.
- <meta charset="UTF-8">: permite acentos, ç e emojis.
- <meta name="viewport">: faz a página se ajustar à tela do celular.
- <title>: texto da aba do navegador e do resultado no Google.
- <body>: tudo que aparece na tela.

Atalho: digitar ! e apertar Enter gera o esqueleto.
Sempre mudar o lang para pt-BR e o title.

## Treino 1
### ul x ol
- ul: lista com bolinhas. A ordem não importa.
- ol: lista numerada. A ordem importa (passos, etapas).
Teste: "se eu embaralhar os itens, muda o sentido?" Se sim, ol.

### Links entre páginas
- Para ir a outra página da mesma pasta, o href recebe só o nome do arquivo.
  Ex: <a href="index.html">Voltar para o início</a>
- Isso se chama caminho relativo.
- Pensar sempre nos dois sentidos: ida e volta entre as páginas.

### Nomes de arquivo
- Sem acento, sem ç, sem espaço, tudo minúsculo.
- Com acento pode funcionar no meu computador e quebrar no servidor.

### alt da imagem
- Não começar com "imagem de": o leitor de tela já avisa que é imagem.
- Descrever o que aparece de fato na foto.

### Mensagens de commit
- Começar com verbo: Adiciona, Corrige, Altera, Ajusta, Remove.
- Dizer o que o commit faz, de forma curta.

### Trabalho em equipe
- Se achar uma ideia melhor que a do ticket, avisar antes de mudar.
## CSS: o básico
CSS = aparência. HTML = estrutura.
Fica num arquivo separado (style.css) para mudar o site inteiro em um lugar só.

### Conectar o CSS ao HTML
<link rel="stylesheet" href="style.css">
- Vai no <head>, NÃO no <header>.
- Cada página precisa da sua própria linha de link.

### Cuidado com nomes parecidos
- <head>: informações sobre a página (title, charset, link do CSS). Não aparece na tela.
- <header>: cabeçalho visível da página (nome da empresa).
- <title>: texto da aba do navegador.
- <h1>: título grande dentro da página.

### Estrutura de uma regra
seletor {
    propriedade: valor;
}
- Seletor: QUEM vai mudar (aponta para as tags do HTML).
- Propriedade: O QUE vai mudar.
- Valor: COMO vai ficar.
Não esquecer o ; no fim de cada linha e as chaves { }.

### Seletores
- h1 { }: todos os h1.
- h1, h2 { }: vírgula = h1 E h2, com o mesmo estilo.
- footer a { }: espaço = os links que estão DENTRO do footer.
Antes de mudar uma regra, perguntar: "quem mais é afetado por isso?"

### Cores
- Códigos hexadecimais: #2E7D32. Três pares: vermelho, verde e azul.
- Usam números de 0 a 9 e letras de A a F.
- color: cor do texto. background-color: cor do fundo.

### Herança (cascata)
Estilo aplicado numa caixa passa para tudo que está dentro dela.
Ex: font-family no body muda a fonte da página inteira.

### Erros silenciosos
CSS não dá erro: se não entende uma linha, ignora e segue.
Ficar de olho no sublinhado amarelo do VS Code e no número de problemas na aba.

## Modelo de caixa (box model)
Todo elemento é uma caixa com 4 camadas, de dentro para fora:
1. Conteúdo
2. padding: espaço DENTRO da borda
3. border: a
### Truques do COL-7
- Lista sem bolinha: list-style: none; + padding: 0; (sempre juntos)
- Ctrl + F5: recarrega ignorando o cache (cópia antiga guardada pelo navegador)
- Seletor que não encontra nenhum elemento não dá erro: só não faz nada
- Lados: top (cima), bottom (baixo, NÃO é button/botão), left, right
- Tags curtas: a (link), p (parágrafo), ul (lista com bolinha), ol (lista numerada), li (item)
## Modelo de caixa (box model)
Todo elemento é uma caixa com 4 camadas, de dentro para fora:
1. content (conteúdo): o texto, a imagem, o que aparece de fato.
2. padding (preenchimento): espaço DENTRO da borda, em volta do conteúdo.
   Pega a cor de fundo da caixa. Aumentar = a caixa cresce.
3. border (borda): a linha em volta da caixa.
   Ex: border: 2px solid #2E7D32; (espessura, estilo, cor)
4. margin (margem): espaço FORA da borda. É transparente.
   Aumentar = a caixa fica do mesmo tamanho e só afasta os vizinhos.

Analogia: quadro na parede.
- content = a foto
- padding = o fundo branco em volta da foto
- border = a moldura
- margin = o espaço na parede até o próximo quadro

Teste que fiz no .botao:
- padding maior: o botão cresceu, o laranja aumentou.
- margin maior: o botão ficou igual, só se afastou dos outros elementos.

Atalho para ver o box model: F12 > clicar com o botão direito no elemento > Inspecionar > aba Computed.
