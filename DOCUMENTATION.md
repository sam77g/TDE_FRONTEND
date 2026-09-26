**DOCUMENTAÇÃO PARA COLABORATORES**
================================

# Introdução
Neste documento será abordado como devem ser commitadas as mudanças, as branchs que podem ser alteradas, a estrutura a seguir seguidado e as normas

### COMO DEVO PARTICIPAR ?
Qualquer um que queira contribuir deve seguir as seguintes __regras__ :
1. **Antes do commit/Pull Request** : Antes de abrir seu PR, você deve atualizar sua branch. 
    ```bash 
        git checkout develop
        git pull origin develop
        git checkout feature/navbar
        git merge develop
    ```

2. Quando for trabalhar no projeto, trabalhe em uma branch separada (ex: FEATURE/navbar )
3. Apenas der pull request quando terminar a feature ou fix
    - A sua pull request será analisada e incorporada ao projeto ( merge )
4. Siga as **Conventional Commits**
    - Nova funcionalidade :   ``` git commit -m "feat: adiciona página de destinos" ```
    - Correção : ```git commit -m "fix: corrige menu mobile" ```
    - Documentação : ``` git commit -m "docs: atualiza documentação do projeto" ```
    - Refatoração : ``` git commit -m "refactor: reorganiza componentes da navbar" ```
5. Branchs : 
    - __Main__ : Branch principal, onde será feito o deploy do projeto
    - __Produção__ : Branch de desenvolvimento, onde todos devem e podem commit e fazer os pull request
        - Nessa Branch você terá que seguir as dicas no tópico 4 e 2.
        - Crie a branch que você está desenvolvendo e dê o pull request para o merge nesta branch
    
