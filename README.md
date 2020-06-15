# Teste Backend

Leia primeiro todo o projeto, faça sua estimativa de horas para o desenvolvimento e envie um email com o título `[Teste Backend] Estimativa` para rh@nanoincub.com.br

Quando finalizar o teste, publique tudo no seu [Github](https://github.com) e envie um email com o título `[Teste Backend] Finalizado` para rh@nanoincub.com.br contendo o link do repositório do projeto.

## Atenção:

Coloque no `README.md` do seu projeto todas as instruções para conseguirmos executá-lo.

---

## Escopo do projeto

O cliente entrou em contato querendo desenvolver um sistema de bonificação para seus funcionários, para não bonificar os funcionários em forma de dinheiro, ele decidiu desenvolver um sistema onde os funcionários terão um saldo de pontos e esses pontos podem ser convertidos em recarga para celular, compra de produtos, etc.

O MVP proposto é um painel administrativo para gerenciar os funcionários e seus respectivos pontos.

## Missão
Desenvolver um **Painel Administrativo** em **PHP** para gestão de funcionário e bonificação.

## Avaliação

Entre os critérios de avaliação estão:
- Usabilidade
- Criatividade
- Código limpo e organização
- Modelagem de banco de dados
- Lógica de negócio
- Documentação do projeto (readme)

### Especificação

Monte uma base de dados com a seguinte estrutura:

Administrador:
```
id                  int
nome_completo:      string
login:              string
senha:              string
data_criacao:       datetime
data_alteracao:     datetime
```

Funcionario:
```
id                  int
nome_completo:      string
login:              string
senha:              string
saldo_atual:        decimal
data_criacao:       datetime
data_alteracao:     datetime
```

Movimentacao:
```
id                  uuid
tipo_movimentacao   string      entrada|saida
valor:              decimal
observacao:         string  
administrador_id:   int  
data_criacao:       datetime
data_alteracao:     datetime
```

Utilize **MySQL** para armazenar os dados.

---

### Funcionalidades da Aplicação

#### Autenticação

- `Login`

Página de Login com campo usuário e senha. Não precisa ter opção de redefinir senha para este MVP.

---

#### Funcionário

`Listagem de funcionário`

Listagem dos funcionários exibindo o ID, Nome,Saldo atual. A listagem deverá ter paginação.

---

`Visualizar extrato do funcionário`

Na listagem de funcionários, deverá ter um botão para visualizar o extrato do funcionário com todas as transações de seus pontos (Data da transação, Tipo, Valor, Observação).

---

`Cadastro de funcionário`

Formulário de cadastro com os campos do funcionário

---

`Edição de funcionário`

Formulário de edição com os campos do funcionário

---

`Excluir funcionário`

Um botão de deletar na listagem de funcionario onde o administrador poderá excluir o funcionário cadastrado.

---

`Filtro de Pesquisa na Listagem de Funcionário`

A Listagem de Funcionário deverá conter um filtro por **Nome do funcionário** e pela **Categoria**.

---

#### Transação


`Listagem de transações`

Listagem das transações, listando do ultimo para o primeiro. A listagem precisará ter paginação.

---

`Cadastro de transação`

Formulário de cadastro com os campos da transação. O campo observação será um pequeno texto para o administrador informar o motivo, exemplo:

```
tipo:       saida
valor:      24.99pts 
observacao: Recarga de celular
```
ou
```
tipo:       entrada
valor:      100.00pts
observacao: Entrega de projeto antes do prazo
```

---

## Sugestões
Você pode utilizar qualquer framework para auxiliar no desenvolvimento da interface, por exemplo:

[https://getbootstrap.com/docs/3.3/css/](https://getbootstrap.com/docs/3.3/css/)

[https://adminlte.io/themes/AdminLTE/index2.html](https://adminlte.io/themes/AdminLTE/index2.html)

[https://startbootstrap.com/template-overviews/sb-admin-2/](https://startbootstrap.com/template-overviews/sb-admin-2/)


## Dúvida

Se tiver qualquer dúvida sobre esse teste, envie um email com o título `[Teste Backend] O assunto da dúvida` para rh@nanoincub.com.br
