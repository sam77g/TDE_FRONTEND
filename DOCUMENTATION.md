**DOCUMENTAÇÃO PARA COLABORATORES**
================================

# Introdução
Neste documento será abordado como devem ser commitadas as mudanças, as branchs que podem ser alteradas, a estrutura a seguir seguidado e as normas

### COMO DEVO PARTICIPAR ?
Qualquer um que queira contribuir deve seguir as seguintes __regras__ :
- **Antes do commit/Pull Request** : 
    ```bash 
        git checkout develop
        git pull origin develop
        git checkout feature/navbar
        git merge develop

- Quando for trabalhar no projeto, trabalhe em uma branch separada (ex: FEATURE/navbar )
- Apenas der pull request quando terminar a feature ou fix
    - A sua pull request será analisada e incorporada ao projeto ( merge )
- Siga as **Conventional Commits**
    - Nova funcionalidade :   ``` git commit -m "feat: adiciona página de destinos" ```
    - Correção : ```git commit -m "fix: corrige menu mobile" ```
    - Documentação : ``` git commit -m "docs: atualiza documentação do projeto" ```
    - Refatoração : ``` git commit -m "refactor: reorganiza componentes da navbar" ```
