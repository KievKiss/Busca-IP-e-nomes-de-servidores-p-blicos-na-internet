
# Aplicação de Linha de Comando - Busca IPs e Nomes de Servidores

Esta é uma aplicação em Go que oferece uma interface de linha de comando para buscar IPs e os nomes de servidores de um determinado host na internet.

## Funcionalidades

A aplicação possui dois comandos principais:

1. **ip**: Busca e exibe os IPs associados a um host.
2. **servidores**: Busca e exibe os servidores de nomes (DNS) associados a um host.

## Requisitos

Para executar esta aplicação, você precisará ter o Go instalado em sua máquina.

### Instalação do Go

Siga as instruções de instalação do Go disponíveis [aqui](https://golang.org/doc/install).

## Como Usar

### Clonando o Repositório

Clone o repositório contendo o código da aplicação:

```bash
git clone https://github.com/KievKiss/Busca-IP-e-nomes-de-servidores-publicos-na-internet.git
```

### Compilação e Execução

Para compilar e executar a aplicação, siga os passos abaixo:

1. Compile a aplicação:

   ```bash
   go build -o app
   ```

2. Execute a aplicação:

   ```bash
   ./app <comando> --host <hostname>
   ```

### Exemplos de Uso

1. **Buscar IPs de um host**

   Use o comando `ip` para buscar os IPs associados a um host. O host padrão é `devbook.com.br`, mas você pode especificar outro usando a flag `--host`.

   ```bash
   ./app ip --host google.com
   ```

   Saída esperada:

   ```
   172.217.29.142
   2800:3f0:4001:805::200e
   ```

2. **Buscar Servidores de Nomes (DNS)**

   Use o comando `servidores` para listar os servidores de nomes (DNS) associados a um host. Também aqui o host padrão é `devbook.com.br`, mas você pode especificar outro usando a flag `--host`.

   ```bash
   ./app servidores --host google.com
   ```

   Saída esperada:

   ```
   ns1.google.com.
   ns2.google.com.
   ```

## Estrutura do Projeto

O projeto contém dois arquivos principais:

- `app.go`: Contém a definição da aplicação de linha de comando, seus comandos e flags.
- `main.go`: O ponto de entrada da aplicação, que inicializa e executa o aplicativo.

## Dependências

A aplicação utiliza a biblioteca [urfave/cli](https://github.com/urfave/cli) para facilitar a criação da interface de linha de comando.

Você pode instalar as dependências usando o comando:

```bash
go get github.com/urfave/cli
```
## By Kiev