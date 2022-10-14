DW-BRA
======

## Introdução

Um Data Warehouse (DW) de conjuntos de dados abertos Brasileiros.

## Implantação e Utilização

### Clone do Repositório

```bash
$ git clone https://github.com/andrespp/dw-bra.git
```

### Configurar os parâmetros de conexões

Para configurar o banco de dados que irá receber o DW, as variáveis do arquivo
`config.ini` devem ser definidas.

### Iniciar o SGBD do DW

```bash
$ docker-compose up -d
```

### Verifica Instalação do Docker

```bash
$ make test
```

### Construir/Atualizar o DW

```bash
$ make setup     # Configura o ambiente
$ make getds     # Download dos datasets
$ make extractds # Extrai datasets compactados
$ make run       # Ambiente de produção (config.ini)
$ make run-dev   # Ambiente de desenvolvimento (config-dev.ini)
```

### Atualizar o DW


```bash
$ make run     # Ambiente de produção (config.ini)
$ make run-dev # Ambiente de desenvolvimento (config-dev.ini)
```

## Desenvolvimento

### Virtual environment

Configurar o ambiente virtual para desenvolvimento local:

```bash
conda env create -f environment.yml
conda activate dwbra
./get_ds.py
./extract_ds.py
./update-dw.py
```

## Referências
