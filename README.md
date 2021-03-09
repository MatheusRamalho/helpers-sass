# SVGS ICONS

Pacote de ícones encontrado na net, fiz toda organização, adição de classes, id e acessibilidade, 
Criei arquivos dos icones separados e um arquivo com todos os icones, existe tbm um preview para visualização dos icones para facilitar a utilização. 

O arquivo com todos os svgs juntos não é um svg sprite ainda, ainda não consegui gerar o mesmo. Estou pesquisando para ver como gerar, pois acredito que ele
é o melhor formato de utlização já que permite personalizar o icone em questão de cores, mesmo não sendo necessário incluir no seu código todo o código do svg.

## FORMAS DE UTILIZAR

### 1° FORMA - SASS

Utilizando os icones svg somente via sass/css, são utlizados em formato background-image.
O arquivo sass já possui todo os icones em forma de classes e uma estilização padrão que é chamada em todos os icones. 
Para utilizar dessa forma, basta utlizar o código abaixo no html, apenas incluindo a classe no atributo span.

``` <span class="icon__CLASS-ICON"></span> ```

### 2° FORMA - SPRITE

Para utilizar os icones nesse formato, deve chamar esse código html onde deseja usar esse icone. 
A tag svg possibilita chamar o arquivo svg sem pŕecisar importar todo o código e permite a personalização do svg.
A tag use consta o caminho do arquivo svg em si, como se fosse importar tipo a 3° forma.

``` <svg class="icon__svg" fill="currentColor"> ```
```     <use xlink:href="CAMINHO DO ARQUIVO ICONS.SVG#ID-DO-ICON"/> ```
``` </svg> ```

### 3° FORMA - IMAGEM

Importar o icone svg em formato de imagem, uma forma mais conhecida, porém com maior limitação.
Não é possivél modificar os atributos do svg como cores como é possivél na 2° forma.

``` <img class="icon__svg" src="CAMINHO DO ARQUIVO" alt="."> ```

### OBS

Precisa incluir esse código sass para que os svgs tenham uma estilização padrão.
Para as 2° e 3° forma.

```.icon__svg { ```
```    width: 1.875rem; ```
```    height: 1.875rem; ```
```    display: inline-block; ```
```    background-repeat: no-repeat; ```
```} ```