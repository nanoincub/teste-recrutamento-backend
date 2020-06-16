# Teste Backend

Leia primeiro todo o projeto, faça sua estimativa de horas para o desenvolvimento e envie um email com o título `[Teste Backend] Estimativa` para rh@nanoincub.com.br

Quando finalizar o teste, publique tudo no seu [Github](https://github.com) e envie um email com o título `[Teste Backend] Finalizado` para rh@nanoincub.com.br contendo o link do repositório do projeto.

## Atenção

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
- Documentação do projeto (`README.md`)

## Especificações

### Banco de dados

Monte uma base de dados em **MySQL** com a seguinte estrutura:

Tabela - `administrador`

```sql
id                  int
nome_completo:      string
login:              string
senha:              string
data_criacao:       datetime
data_alteracao:     datetime    * atualiza automaticamente
                                  sempre que o registro é atualizado
```

Tabela - `funcionario`

```sql
id                  int
nome_completo:      string
login:              string
senha:              string
saldo_atual:        decimal
administrador_id:   int         * administrador que cadastrou este registro
data_criacao:       datetime
data_alteracao:     datetime    * atualiza automaticamente
                                  sempre que o registro é atualizado
```

Tabela - `movimentacao`

```sql

id                  *uuid*
tipo_movimentacao   enum        * [entrada|saida]
valor:              decimal
observacao:         string
funcionario_id      int         * funcionario vinculado a movimentação 
administrador_id:   int         * administrador que cadastrou este registro
data_criacao:       datetime
data_alteracao:     datetime    * atualiza automaticamente
                                  sempre que o registro é atualizado
```

---

### Funcionalidades da Aplicação

#### Autenticação

- Login
    > Página de Login com campo usuário e senha. Não precisa ter opção de redefinir senha para este MVP.

#### Funcionários

1. Listagem de funcionários
    > Listagem dos funcionários exibindo o ID, Nome, Saldo atual, Data de criação.

2. Paginação e filtro de funcionários
    > Na listagem de funcionários, deverá ter paginação e um filtro por **Nome do funcionário** e pela **Data de cadastro**.

3. Visualizar extrato do funcionário
    > Na listagem de funcionários, deverá ter um botão para visualizar o extrato do funcionário com todas as movimentações de seus pontos (Data da movimentação, Tipo, Valor, Observação).

4. Cadastro de funcionários
    > Formulário de cadastro com os campos do funcionário

5. Edição de funcionário
    > Formulário de edição com os campos do funcionário

6. Excluir funcionário
    > Na listagem de funcionários, deverá ter um botão de deletar onde o administrador poderá excluir o funcionário cadastrado com uma confirmação antes da exclusão.

#### Movimentações

1. Listagem de movimentações
    > Listagem das movimentações exibindo, ID, Tipo, Valor, Funcionário, Observação e Data de criação, listando da última para o primeira.

2. Paginação e filtro de movimentações
    > Na listagem de movimentações, deverá ter paginação e um filtro por **Nome do funcionário**, pela **Data de cadastro** e por **Tipo de movimentação**

3. Cadastro de movimentações
    > Formulário de cadastro com os campos da movimentação. O campo observação será um pequeno texto para o administrador informar o motivo, exemplo:

    ```plain
    tipo:       saida
    valor:      24.99
    observacao: Recarga de celular
    ```

    ou

    ```plain
    tipo:       entrada
    valor:      100.00
    observacao: Entrega de projeto antes do prazo
    ```

---

## Sugestões

Você pode utilizar qualquer framework para auxiliar no desenvolvimento da interface, por exemplo:

[https://getbootstrap.com/docs/3.3/css/](https://getbootstrap.com/docs/3.3/css/)

[https://adminlte.io/themes/AdminLTE/index2.html](https://adminlte.io/themes/AdminLTE/index2.html)

[https://startbootstrap.com/template-overviews/sb-admin-2/](https://startbootstrap.com/template-overviews/sb-admin-2/)

## Dúvidas

Se tiver qualquer dúvida sobre esse teste, envie um email com o título `[Teste Backend] O assunto da dúvida` para rh@nanoincub.com.br
