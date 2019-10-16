# Guia de Contribuição  

Você deve seguir o guia de contribuição em seu projeto para as métricas serem coletadas corretamente nesse projeto.

* *Fork* do repositório (apenas para usuários externos)
* Criar [*issues*](CONTRIBUTING.md#política-de-issues)
* [*Labels*] ()
* Criar [*branchs*](CONTRIBUTING.md#política-de-branches)
* Seguir a política de [*commits*](CONTRIBUTING.md#política-de-commits)
* Submeter [*Pull Request*](CONTRIBUTING.md#política-de-merges-e-pull-requests)


### Política de Issues

As *issues* devem possuir título, descrição, *labels*,  *milestone* (a *sprint* que deve ser concluída) e caso possua *estimated*(puntuação) para as *issues* pontuadas.

Para criação de issue o [template Issue](issue_template.md) deve ser seguido.

![Issue Example](/img/issue_example.gif)

### Política de Labels

As labels são essenciais para a extração das métricas e da documentação dos requisitos do projeto.

As Labels usadas no projeto são:


### Política de Branches  

#### *master*

A branch *master* é a branch de produção, onde ficará a versão estável do projeto. Ela estará bloqueada para commits e para pushs.
Veja a política de merges no tópico [Merges para *master*](CONTRIBUTING.md#merges-para-master).

#### *development*

A branch *development* é a branch de desenvolvimento, onde o trabalho das outras branchs será unificado e onde será criada uma versão estável para mesclar com a *master*.
Assim como a *master* ela está bloqueada para commits e pushs.
Veja a política de merges no tópico [Merges para development](CONTRIBUTING.md#merges-para-development)
merges para *development*</a> .

#### Nome das Branches  

As branchs de desenvolvimento de features serão criadas a partir da branch *development* com a nomenclatura padrão `x_nome_da_issue`, onde o `x` representa o código de rastreio da issue.

### Política de Commits

Os commits devem ser feitos usando o parâmetro `-s` para indicar sua assinatura no commit.

```
git commit -s
```
A issue em questão deve ser citada no commit, para isso, basta adicionar `#<numero_da_issue>`.

```
 #5 Fazendo guia de contribuição
```

** \*\*Por padrão, o caracter `#` define uma linha de comentário no arquivo da mensagem do commit. Para resolver este problema, use o commando:**
```
git config --local core.commentChar '!'
```

https://docs.gitlab.com/ee/user/project/issues/managing_issues.html  

Exemplo de comentário do commit:
```
Fix #5 Finalizando guia de contribuição do projeto
```

Para commits que incluem uma pequena mudança em uma issue que já teve sua resolução encerrada, deve-se iniciar a mensagem do commit com `HOTFIX #<numero_da_issue> <mensagem>`

Exemplo de comentário do commit:
```
HOTFIX #5 Atualizando guia de contribuição do projeto
```

### Política de Merges Requests

#### Merge Requests

Merge requests devem ser feitos para a branch *master* e para a *development* seguindo as regras e os passos do tópico [*Merges para master*](CONTRIBUTING.md#merges-para-master). No conteúdo do pull request deve haver uma descrição clara do que foi feito.

Deve ser seguido o [template Pull Request](docs/pull_request_template.md).

##### Work in Progress

Caso haja a necessidade de atualizar a branch *master* antes de concluir a issue, o nome do pull request deve conter WIP:<X_nome_da_branch> para que a branch não seja deletada.

#### Merges para *master* e *development*
Os merges para *master* deverão ser feitos quando a funcionalidade ou refatoração estiverem de acordo com os seguintes aspectos:  
- Funcionalidade ou refatoração concluída;
- *Build* do Travis passando;
- Progredir ou manter a porcentagem de cobertura de teste;
- Funcionalidade revisada por algum outro membro.

Para fazer um merge para *master* os passos a serem seguidos são:  
- `git checkout branch_de_trabalho`;
- `git pull --rebase origin master`;
- `git push origin branch_de_trabalho`;
- Abrir merge request via interface GitLab;
- Aguardar Code Review.


##### Code Review


##### Cobertura de testes


#### Tag's

<!-- Explicar tag's -->
