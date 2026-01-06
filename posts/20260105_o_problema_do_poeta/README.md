# O problema do poeta

Esse projeto tem como objetivo consolidar a resolução de um problema linear aplicado ao Manejo Florestal conhecido como "O Problema do Poeta", proposto pelo professor [Júlio Eduardo Arce](https://buscatextual.cnpq.br/buscatextual/visualizacv.do;jsessionid=8FC7A28443BA38A7421C46CD1E2C9058.buscatextual_0) (UFPR) em sua apostila de Programação Linear para Fins Florestais.

A ideia aqui é utilizar ferramentas de Python para modelar e resolver o problema, de maneira didática e aproveitando todos os recursos oferecidos pela ferramenta [Quarto](https://quarto.org/).

# Pré-requisitos

Antes de começar, você precisa ter instalado:

* **Python ≥ 3.12**
* **uv** (gerenciador de dependências Python)
* **Quarto** (ferramenta para criação de relatórios)

# Instalando o uv

Se você ainda não tem o `uv` instalado, execute:

**macOS e Linux:**

```
curl -LsSf https://astral.sh/uv/install.sh | sh
```

**Windows:**

```
powershell -ExecutionPolicy ByPass -c "irm https://astral.sh/uv/install.ps1 | iex"
```

Após a instalação, reinicie o terminal e verifique:

```
uv --version
```

Para mais informações sobre a instalação do `uv`, consultar na documentação oficial: [Installation | uv](https://docs.astral.sh/uv/getting-started/installation/#__tabbed_1_1)

# Instalando o Quarto

Acessar o site da ferramenta e realizar o download do instalador de acordo com o seu sistema operaiconal: [Get Started – Quarto](https://quarto.org/docs/get-started/)

# Instalando as dependências do projeto

1. Clone este repositório com o código abaixo ou realize o download manualmente pelo github
2. Crie o ambiente virtual e estale as dependências (esse código é rodado diretamente no terminal):

```
uv sync
```

Esse comando:

* cria automaticamente um ambiente virtual
* instala todas as dependências definidas em `pyproject.toml`, ou seja, irá realizar o download dos pacotes (e solver, nesse caso) utilizado no projeto
* respeita o arquivo `uv.lock`, que faz o controle das versões das bibliotecas

# Observações importantes

* Não use `pip install` diretamente — o gerenciamento de dependências é feito exclusivamente via `uv`
* Caso utilize solvers externos (ex: GLPK, GUROBI,), eles **não são instalados automaticamente** e devem estar disponíveis no sistema. No repositório do projeto existe o executável do solver CBC
* Não tem scrips python nesse projeto, ele roda diretamente dentro do documento quarto, arquivo `ìndex.qmd`.
