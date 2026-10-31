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