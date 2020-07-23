# goesgif

GOES GIF gera um GIF animado com as imagens captadas no dia pelo satélite GOES, disponíveis em https://satelite.inmet.gov.br/

## Instalação

1. clone este repositório (ou baixe o zip, extraia e marque o arquivo `goesgif` como executável)
2. mova o arquivo para um diretório que esteja listado na sua variável de ambiente `$PATH`

## Uso

    ./goesgif área [data]

Onde _área_ =

- AS (América do Sul);
- BR (Brasil);
- CO (Centro-Oeste);
- DF (Distrito Federal);
- N  (Norte);
- NE (Nordeste);
- S  (Sul) ou
- SE (Sudeste)

E _data_ =

- em branco (ou omitido) para hoje ou
- data no formato YYYY-MM-DD

Exemplos:

    ./goesgif BR
    ./goesgif SE 2020-07-22

Nota:

    O GIF gerado para a área/data selecionada será reutilizado em chamadas posteriores se tiver sido gerado há menos de 5 minutos.

## Dependências:

- curl                          https://curl.haxx.se/download.html
- jq                            https://stedolan.github.io/jq/download/
- mpv                           https://mpv.io/installation/
- notify-send (libnotify4)      https://pypi.org/project/notify-send/#files
- base64 (coreutils)            https://ftp.gnu.org/gnu/coreutils/

- ffmpeg (recomendado!)         https://ffmpeg.org/download.html
    ou
- convert (imagemagick)         https://imagemagick.org/script/download.php

## Licença

GNU GPLv3