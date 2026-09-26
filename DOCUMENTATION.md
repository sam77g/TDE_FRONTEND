# DOCUMENTAÇÃO PARA COLABORADORES

## 1. Introdução

Este documento define as regras e o fluxo de trabalho que devem ser seguidos pelos colaboradores do projeto.

O objetivo é manter o repositório organizado, evitar conflitos entre os integrantes e estabelecer um padrão para o desenvolvimento e integração das alterações.

As principais regras envolvem:

* organização das branches;
* criação e atualização das branches de trabalho;
* commits;
* Pull Requests;
* revisão das alterações;
* integração do código;
* organização dos arquivos do projeto;
* utilização de HTML5, CSS3 e Bootstrap.

---

## 2. Organização das Branches

O projeto utilizará duas branches principais:

### `main`

A `main` representa a versão **estável** do projeto.

* Não deve receber commits diretamente dos colaboradores.
* As alterações devem chegar à `main` por meio de Pull Requests.
* Deve conter uma versão funcional do projeto.
* É a branch utilizada para a versão final/deploy do projeto.

### `develop`

A `develop` representa a versão **em desenvolvimento** do projeto.

* É utilizada para integrar as funcionalidades desenvolvidas pelos colaboradores.
* Os Pull Requests das branches de funcionalidades devem ser direcionados para `develop`.
* Deve ser mantida funcional sempre que possível.
* Não deve ser utilizada para desenvolver diretamente uma funcionalidade.

### Branches de trabalho

Cada colaborador deve criar uma branch própria para a tarefa que estiver desenvolvendo.

Exemplos:

```bash
feature/navbar
feature/pagina-destinos
feature/footer
feature/formulario-contato
```

Para correções:

```bash
fix/menu-mobile
fix/layout-destinos
fix/formulario
```

---

## 3. Como iniciar uma tarefa

Antes de iniciar uma nova tarefa, atualize a `develop` localmente:

```bash
git checkout develop
git pull origin develop
```

Depois, crie uma nova branch a partir da `develop` atualizada:

```bash
git checkout -b feature/nome-da-tarefa
```

Exemplo:

```bash
git checkout -b feature/navbar
```

A partir desse momento, o desenvolvimento da tarefa deve ser realizado nessa branch.

---

## 4. Regras durante o desenvolvimento

Cada colaborador deve:

1. Trabalhar somente na branch correspondente à sua tarefa.
2. Evitar realizar alterações diretamente na `main`.
3. Evitar realizar alterações diretamente na `develop`.
4. Fazer commits pequenos e relacionados à alteração realizada.
5. Utilizar mensagens de commit seguindo o padrão definido neste documento.
6. Verificar o funcionamento da alteração antes de abrir um Pull Request.
7. Manter a branch atualizada com a `develop` antes de solicitar o merge.

---

## 5. Atualizando a branch antes do Pull Request

Antes de abrir um Pull Request, a branch de trabalho deve ser atualizada com as alterações mais recentes da `develop`.

Primeiro:

```bash
git checkout develop
git pull origin develop
```

Depois, volte para sua branch:

```bash
git checkout feature/nome-da-tarefa
```

E faça o merge da `develop`:

```bash
git merge develop
```

Caso existam conflitos, eles devem ser resolvidos na sua branch antes da abertura do Pull Request.

Após resolver os conflitos:

```bash
git add .
git commit -m "fix: resolve conflitos com develop"
git push
```

---

## 6. Commits

O projeto utilizará o padrão de **Conventional Commits** para manter o histórico do repositório organizado.

### Nova funcionalidade — `feat`

Utilizado quando uma nova funcionalidade é adicionada.

```bash
git commit -m "feat: adiciona página de destinos"
```

### Correção — `fix`

Utilizado para corrigir um problema existente.

```bash
git commit -m "fix: corrige menu mobile"
```

### Documentação — `docs`

Utilizado para alterações na documentação.

```bash
git commit -m "docs: atualiza documentação do projeto"
```

### Estilização — `style`

Utilizado para alterações relacionadas à aparência e formatação do projeto.

```bash
git commit -m "style: ajusta espaçamento dos cards"
```

### Refatoração — `refactor`

Utilizado quando o código é reorganizado sem adicionar uma nova funcionalidade ou corrigir um bug.

```bash
git commit -m "refactor: reorganiza estilos da navbar"
```

---

## 7. Padrão dos commits

Os commits devem:

* descrever claramente o que foi alterado;
* ser relacionados a uma alteração específica;
* evitar mensagens genéricas;
* evitar acumular várias funcionalidades diferentes em um único commit.

### Evite:

```text
alterações
mudanças
teste
final
final agora
correções
```

### Prefira:

```text
feat: adiciona página inicial
fix: corrige menu responsivo
style: ajusta layout dos cards
docs: atualiza documentação
```

---

## 8. Pull Request

Quando a tarefa estiver concluída e testada, o colaborador deve enviar sua branch para o GitHub:

```bash
git push -u origin feature/nome-da-tarefa
```

Depois, deve abrir um **Pull Request** direcionado para:

```text
feature/nome-da-tarefa → develop
```

O Pull Request deve conter uma descrição objetiva informando:

* o que foi desenvolvido;
* quais arquivos foram alterados;
* se houve alguma decisão importante;
* se foram encontrados problemas;
* como a alteração foi testada.

### Exemplo

```text
## O que foi feito

- Criada a navbar principal;
- Adicionados links para as páginas;
- Adicionado comportamento responsivo utilizando Bootstrap.

## Testes

- Testado em desktop;
- Testado em resolução mobile;
- Verificado funcionamento dos links.

## Observações

Nenhum problema conhecido.
```

---

## 9. Revisão do Pull Request

Nenhum Pull Request deve ser integrado imediatamente sem uma revisão.

Outro integrante do grupo deve verificar:

* se a funcionalidade está funcionando;
* se a alteração não prejudica outras páginas;
* se o código está organizado;
* se os arquivos estão no local correto;
* se o Bootstrap está sendo utilizado corretamente;
* se existem erros de HTML ou CSS;
* se a alteração atende ao objetivo da tarefa.

Se houver problemas, o responsável pela branch deve corrigi-los antes do merge.

Após a aprovação, o Pull Request poderá ser integrado à `develop`.

---

## 10. Merge

O fluxo de integração será:

```text
feature/nome-da-tarefa
          |
          | Pull Request
          v
       develop
          |
          | versão integrada
          v
         main
```

As branches de funcionalidades **não devem ser integradas diretamente à `main`**.

A `main` receberá as alterações depois que elas forem integradas e testadas na `develop`.

---

## 11. Organização do trabalho do grupo

O projeto possui quatro colaboradores.

Cada integrante deve receber tarefas específicas para evitar que duas pessoas trabalhem simultaneamente na mesma parte do projeto sem necessidade.

Exemplo:

| Integrante | Responsabilidades                        |
| ---------- | ---------------------------------------- |
| Pessoa 1   | Estrutura geral e integração             |
| Pessoa 2   | Navbar e componentes de navegação        |
| Pessoa 3   | Páginas e conteúdo                       |
| Pessoa 4   | Footer, responsividade e ajustes visuais |

A divisão acima é apenas um exemplo. As tarefas reais devem ser definidas de acordo com as necessidades do projeto.

---

## 12. HTML, CSS e Bootstrap

Como o projeto utiliza **HTML5, CSS3 e Bootstrap**, os colaboradores devem seguir algumas regras de organização.

### HTML

* Utilizar elementos semânticos quando apropriado.
* Manter uma estrutura de HTML organizada.
* Evitar código duplicado desnecessariamente.
* Utilizar indentação consistente.
* Utilizar atributos `alt` nas imagens.

Exemplo:

```html
<section class="container">
    <h2>Destinos</h2>

    <div class="row">
        ...
    </div>
</section>
```

### CSS

Os estilos personalizados devem ficar nos arquivos CSS definidos pelo projeto.

Evite utilizar CSS inline sem necessidade:

```html
<div style="margin-top: 20px;">
```

Prefira classes:

```html
<div class="espacamento-topo">
```

E no CSS:

```css
.espacamento-topo {
    margin-top: 20px;
}
```

### Bootstrap

O Bootstrap deve ser utilizado para os componentes e recursos definidos no projeto, como:

* Grid;
* containers;
* botões;
* cards;
* navbar;
* responsividade;
* espaçamento;
* componentes visuais.

Evite recriar manualmente, com CSS, funcionalidades que já são fornecidas adequadamente pelo Bootstrap.

---

## 13. Conflitos de código

Conflitos podem ocorrer quando duas branches modificam a mesma parte de um arquivo.

Quando ocorrer um conflito:

1. Não apague alterações sem verificar o que foi desenvolvido.
2. Identifique qual alteração deve permanecer.
3. Converse com o responsável pela alteração quando houver dúvida.
4. Resolva o conflito na sua própria branch.
5. Teste o projeto após resolver o conflito.
6. Faça um commit registrando a resolução.

Exemplo:

```bash
git checkout feature/nome-da-tarefa
git merge develop
```

Depois de resolver os conflitos:

```bash
git add .
git commit -m "fix: resolve conflitos com develop"
git push
```

---

## 14. Antes de abrir um Pull Request

Utilize esta lista de verificação:

* [ ] A tarefa foi concluída.
* [ ] A página/funcionalidade foi testada.
* [ ] Não existem erros aparentes no HTML.
* [ ] O CSS está funcionando corretamente.
* [ ] A responsividade foi verificada.
* [ ] As alterações da `develop` foram incorporadas à branch.
* [ ] Os commits seguem o padrão definido.
* [ ] Não existem arquivos desnecessários.
* [ ] Não existem senhas, tokens ou informações sensíveis.
* [ ] O Pull Request possui uma descrição clara.

---

## 15. Fluxo resumido

O fluxo padrão para qualquer colaborador será:

```text
1. Atualizar develop
        ↓
2. Criar branch da tarefa
        ↓
3. Desenvolver
        ↓
4. Fazer commits
        ↓
5. Atualizar branch com develop
        ↓
6. Testar
        ↓
7. Push da branch
        ↓
8. Abrir Pull Request
        ↓
9. Revisão
        ↓
10. Merge → develop
        ↓
11. Testes de integração
        ↓
12. Merge → main
```

---

## 16. Regra principal

O objetivo do fluxo não é criar burocracia, mas manter o projeto organizado e permitir que os quatro integrantes trabalhem simultaneamente sem sobrescrever o trabalho uns dos outros.

Sempre que houver dúvida sobre uma alteração que possa afetar o trabalho de outro integrante, a decisão deve ser discutida antes de realizar o merge.
