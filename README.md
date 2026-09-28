# TDE FRONTEND

Landing page institucional para uma empresa de viagens e turismo, desenvolvida como trabalho acadêmico (TDE) da disciplina de **Front-End**, ministrada pelo Prof. Gean Trabuco.

![Status](https://img.shields.io/badge/status-em%20desenvolvimento-yellow)
![Versão](https://img.shields.io/badge/vers%C3%A3o-v0.2.0--beta-blue)
![HTML5](https://img.shields.io/badge/HTML5-E34F26?logo=html5&logoColor=white)
![CSS3](https://img.shields.io/badge/CSS3-1572B6?logo=css3&logoColor=white)
![Bootstrap](https://img.shields.io/badge/Bootstrap-5.3.8-7952B3?logo=bootstrap&logoColor=white)
![Licença](https://img.shields.io/badge/licen%C3%A7a-MIT-green)

---

## Sumário

1. [Sobre o Projeto](#1-sobre-o-projeto)
2. [Funcionalidades](#2-funcionalidades)
3. [Tecnologias Utilizadas](#3-tecnologias-utilizadas)
4. [Estrutura do Projeto](#4-estrutura-do-projeto)
5. [Pré-requisitos](#5-pré-requisitos)
6. [Como Executar](#6-como-executar)
7. [Versionamento](#7-versionamento)
8. [Fluxo de Desenvolvimento](#8-fluxo-de-desenvolvimento)
9. [Status do Projeto](#10-status-do-projeto)
10. [Licença](#11-licença)

---

## 1. Sobre o Projeto

O **TDE Frontend** é um projeto front-end estático que consiste em uma landing page para uma empresa fictícia de turismo, denominada **Emerald**. A página apresenta a proposta da empresa, seus principais destinos no Brasil e um canal de contato para o planejamento de viagens.

O projeto tem finalidade acadêmica e busca aplicar, de forma prática, os conceitos de estruturação semântica com HTML5, estilização com CSS3, construção de layouts responsivos com Bootstrap 5 e organização de trabalho colaborativo com Git e GitHub.

## 2. Funcionalidades

- **Barra de navegação responsiva**, fixa no topo, com menu lateral (*offcanvas*) em dispositivos móveis.
- **Seção Hero** com imagem de fundo, chamada principal e botão de acesso direto aos pacotes.
- **Seção "Sobre Nós"**, com apresentação da empresa e imagem ilustrativa.
- **Seção "Nossos destinos"**, com apresentação de Rio de Janeiro, Brasília e Salvador em cartões com layouts distintos.
- **Seção de contato (CTA)**, com chamada para ação e link direto de e-mail.
- **Rodapé** com informações de autoria e atalhos de navegação.
- **Layout adaptável** a diferentes tamanhos de tela (*desktop*, *tablet* e *mobile*), com *media queries* específicas.

## 3. Tecnologias Utilizadas

| Tecnologia | Finalidade |
| ---------- | ---------- |
| **HTML5** | Estruturação semântica do conteúdo |
| **CSS3** | Estilização personalizada, variáveis CSS e *media queries* |
| **Bootstrap 5.3.8** | Grid, componentes (navbar, offcanvas, botões) e responsividade |
| **Bootstrap Icons 1.13.1** | Biblioteca de ícones |
| **Google Fonts** | Fontes tipográficas do projeto |
| **JavaScript** | Arquivo reservado para comportamentos futuros |

> O Bootstrap, o Popper e o Bootstrap Icons são carregados por meio de **CDN** (jsDelivr).

## 4. Estrutura do Projeto

```text
TDE_FRONTEND/
├── src/
│   ├── img/                 # Imagens utilizadas nas seções da página
│   ├── js/
│   │   └── script.js        # Scripts do projeto (reservado)
│   ├── style/
│   │   └── style.css        # Estilos personalizados
│   └── index.html           # Página principal
├── DOCUMENTATION.md         # Guia para colaboradores
├── LICENSE                  # Licença MIT
└── README.md                # Documentação geral do projeto
```

## 5. Pré-requisitos

- Navegador web atualizado (Google Chrome, Mozilla Firefox, Microsoft Edge ou Safari).
- Conexão com a internet, necessária para o carregamento do Bootstrap, dos ícones e das fontes via CDN.
- *(Opcional)* [Git](https://git-scm.com/) para clonagem do repositório.
- *(Opcional)* Editor de código, como o [Visual Studio Code](https://code.visualstudio.com/), com a extensão **Live Server**.

## 6. Como Executar

1. Clone o repositório:

   ```bash
   git clone https://github.com/<usuario>/TDE_FRONTEND.git
   ```

2. Acesse o diretório do projeto:

   ```bash
   cd TDE_FRONTEND
   ```

3. Execute a aplicação por uma das opções abaixo:

   **Opção A — Abertura direta:** abra o arquivo `src/index.html` no navegador.

   **Opção B — Live Server (VS Code):** clique com o botão direito em `src/index.html` e selecione **Open with Live Server**.

   **Opção C — Servidor local com Python:**

   ```bash
   cd src
   python -m http.server 8000
   ```

   Em seguida, acesse `http://localhost:8000` no navegador.

> Por se tratar de um projeto estático, não há etapa de instalação de dependências ou de compilação.

## 7. Versionamento

O projeto adota **Git Tags** e **GitHub Releases** para identificar seus marcos de desenvolvimento.

| Versão | Descrição |
| ------ | --------- |
| `v0.1.0-alpha` | Estrutura inicial utilizando HTML5 |
| `v0.2.0-beta` | Implementação de CSS3 e Bootstrap 5 |
| `v1.0.0` | Versão final para *deploy* e apresentação |

As versões publicadas não devem ser alteradas. Correções em versões já publicadas devem originar uma nova versão. Os detalhes do procedimento de criação de tags estão descritos em [`DOCUMENTATION.md`](./DOCUMENTATION.md).

## 8. Fluxo de Desenvolvimento

O desenvolvimento segue um fluxo baseado em *branches* e *Pull Requests*, detalhado em [`DOCUMENTATION.md`](./DOCUMENTATION.md). Em resumo:

- **`main`**: versão estável, destinada ao *deploy*. Não recebe *commits* diretos.
- **`develop`**: versão em desenvolvimento, na qual as funcionalidades são integradas.
- **`feature/*` e `fix/*`**: *branches* de trabalho, criadas a partir da `develop`.

```text
feature/nome-da-tarefa ──► Pull Request ──► develop ──► main
```

**Padrão de commits:** [Conventional Commits](https://www.conventionalcommits.org/pt-br/v1.0.0/).

| Prefixo | Uso |
| ------- | --- |
| `feat` | Nova funcionalidade |
| `fix` | Correção de problema |
| `docs` | Alteração na documentação |
| `style` | Alteração visual ou de formatação |
| `refactor` | Reorganização de código sem alteração de comportamento |

Exemplo:

```bash
git commit -m "feat: adiciona seção de destinos"
```

Todo Pull Request deve ser revisado por outro integrante da equipe antes da integração.


## 9. Status do Projeto

🚧 **Em desenvolvimento** — etapa `v0.2.0-beta` (HTML5, CSS3 e Bootstrap 5).

Itens pendentes identificados para as próximas etapas:

- [x] Consolidar o `index.html`, removendo os blocos duplicados de estrutura (`<head>` e `<body>`).
- [x] Padronizar os nomes e os caminhos dos arquivos de imagem referenciados no HTML.
- [x] Reposicionar o `@import` de fontes no início do `style.css`.
- [ ] Implementar os comportamentos em `script.js`, caso necessários.
- [ ] Executar a revisão final, os testes de responsividade e a validação dos links.
- [ ] Publicar a versão `v1.0.0` e realizar o *deploy*.

## 10. Licença

Este projeto está licenciado sob a **Licença MIT**. Consulte o arquivo [`LICENSE`](./LICENSE) para mais informações.
