# Teste Backend

Leia primeiro todo o projeto, faça sua estimativa de horas para o desenvolvimento e envie um email com o
título `[Teste Backend] Estimativa` para rh@nanoincub.com.br

Quando finalizar o teste, publique tudo no seu [Github](https://github.com) e envie um email com o
título `[Teste Backend] Finalizado` para rh@nanoincub.com.br contendo o link do repositório do projeto

## Atenção:

Coloque no `README.md` do seu projeto todas as instruções para conseguirmos executá-lo.


## Missão
- Desenvolver um **Painel Administrativo** em **PHP** para gestão de Produto
- Faça validações nos campos, todos os campos são obrigatórios


### Especificação

Monte uma base de produto com a seguinte estrutura:

Produto:
```
nome:               string
preco:              string
quantidade_estoque: int
categoria_id:       int
data_criacao:       datetime
data_alteracao:     datetime
```

Categoria de produto:
```
nome:               string
data_criacao:       datetime
data_alteracao:     datetime
```

Utilize **MySQL** para armazenar os dados.

### Funcionalidades da Aplicação

- `Login`

Página de Login com campo usuário e senha.

---

`Listagem de Produto`

Listagem dos produtos exibindo o ID, Nome,Categoria, Preco e Quantidade de Estoque. A listagem deverá ter paginação.

---

`Cadastro de Produto`

Formulário de cadastro com os campos do produto

---

`Edição de Produto`

Formulário de edição com os campos do produto

---

`Excluir Produto`

Um botão de deletar na listagem de produtos onde o usuário poderá excluir o produto cadastrado.

---

`Filtro de Pesquisa na Listagem de Produto`

A Listagem de Produto deverá conter um filtro por **Nome do Produto** e pela **Categoria**.

---

`Listagem de Categoria de Produto`

Listagem das categorias do produtos apenas com paginação.

---

`Cadastro de Categoria de Produto`

Formulário de cadastro com os campos da categoria do produto

---

`Edição de Categoria de Produto`

Formulário de edição com os campos da categoria do produto

---

`Excluir  Categoria de Produto`

Um botão de deletar na listagem de categorias de produtos onde o usuário poderá excluir a categoria cadastrada.

---

## Dica
VocÊ pode utilizar algum framework para auxiliar no desenvolvimento da interface, por exemplo:

[https://getbootstrap.com/docs/3.3/css/](https://getbootstrap.com/docs/3.3/css/)

[https://adminlte.io/themes/AdminLTE/index2.html](https://adminlte.io/themes/AdminLTE/index2.html)

[https://startbootstrap.com/template-overviews/sb-admin-2/](https://startbootstrap.com/template-overviews/sb-admin-2/)


### Framework PHP desejado
[CodeIgniter 3.x](https://github.com/bcit-ci/CodeIgniter) (*Opcional*)

## Dúvida

Se tiver qualquer dúvida sobre esse teste, envie um email com o título `[Teste Backend] O assunto da dúvida` para rh@nanoincub.com.br
