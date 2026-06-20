# Atividade

## Com base em uma rotina de CRUD de usuários (incluindo a função Login) em um sistema Web simples, faça o BDD das rotinas do sistema (CRUD + Login).

## Anote também os princípios de teste.

---

# BDD : CRUD de Usuários e Login

## Funcionalidade : Login

### Cenário 1 : Login com sucesso

**Dado** que estou na tela de login e possuo uma conta cadastrada

**Quando** informo um e-mail e senha válidos e clico em "Entrar"

**Então** o sistema deve autenticar o usuário e redirecioná-lo para a página inicial.

### Cenário 2 : Senha incorreta

**Dado** que estou na tela de login

**Quando** informo um e-mail válido e uma senha incorreta

**Então** o sistema deve exibir uma mensagem informando que as credenciais são inválidas.

### Cenário 3 : E-mail não informado

**Dado** que estou na tela de login

**Quando** deixo o campo e-mail vazio e clico em "Entrar"

**Então** o sistema deve solicitar o preenchimento do campo obrigatório.

### Cenário 4 : Senha não informada

**Dado** que estou na tela de login

**Quando** deixo o campo senha vazio e clico em "Entrar"

**Então** o sistema deve solicitar o preenchimento da senha.

### Cenário 5 : Conta bloqueada

**Dado** que minha conta está bloqueada

**Quando** tento realizar login com credenciais válidas

**Então** o sistema deve impedir o acesso e informar que a conta está bloqueada.

---

# Funcionalidade : Cadastro de Usuário (Create)

### Cenário 1 : Cadastro realizado com sucesso

**Dado** que estou na tela de cadastro de usuários

**Quando** preencho todos os campos obrigatórios corretamente e clico em "Salvar"

**Então** o sistema deve cadastrar o usuário e exibir a listagem atualizada.

### Cenário 2 : E-mail duplicado

**Dado** que já existe um usuário cadastrado com determinado e-mail

**Quando** tento cadastrar outro usuário utilizando o mesmo e-mail

**Então** o sistema deve impedir o cadastro e exibir uma mensagem de erro.

### Cenário 3 : Nome obrigatório

**Dado** que estou na tela de cadastro

**Quando** deixo o campo nome vazio e clico em "Salvar"

**Então** o sistema deve informar que o nome é obrigatório.

### Cenário 4 : E-mail inválido

**Dado** que estou cadastrando um novo usuário

**Quando** informo um e-mail em formato inválido

**Então** o sistema deve impedir o cadastro e informar o erro.

### Cenário 5 : Senha fora do padrão

**Dado** que estou cadastrando um usuário

**Quando** informo uma senha menor que o mínimo permitido

**Então** o sistema deve impedir o cadastro e informar a regra de validação.

---

# Funcionalidade : Consulta de Usuários (Read)

### Cenário 1 : Exibir usuários cadastrados

**Dado** que existem usuários cadastrados no sistema

**Quando** acesso a tela de listagem

**Então** o sistema deve exibir todos os usuários cadastrados.

### Cenário 2 : Buscar usuário por nome

**Dado** que existem usuários cadastrados

**Quando** realizo uma busca pelo nome do usuário

**Então** o sistema deve exibir apenas os registros correspondentes.

### Cenário 3 : Nenhum usuário encontrado

**Dado** que não existem usuários cadastrados

**Quando** acesso a listagem

**Então** o sistema deve exibir uma mensagem informando que não existem registros.

### Cenário 4 : Paginação da listagem

**Dado** que existem muitos usuários cadastrados

**Quando** acesso a tela de consulta

**Então** o sistema deve exibir os registros paginados.

### Cenário 5 : Busca por e-mail

**Dado** que existe um usuário cadastrado

**Quando** realizo uma busca utilizando seu e-mail

**Então** o sistema deve exibir o usuário correspondente.

---

# Funcionalidade : Alteração de Usuário (Update)

### Cenário 1 : Atualização com sucesso

**Dado** que existe um usuário cadastrado

**Quando** altero seus dados e clico em "Salvar"

**Então** o sistema deve atualizar as informações corretamente.

### Cenário 2 : E-mail inválido na alteração

**Dado** que estou editando um usuário

**Quando** informo um e-mail inválido

**Então** o sistema deve impedir a atualização.

### Cenário 3 : E-mail já utilizado

**Dado** que existe outro usuário cadastrado

**Quando** tento alterar o e-mail para um endereço já utilizado

**Então** o sistema deve impedir a alteração.

### Cenário 4 : Nome não informado

**Dado** que estou alterando um usuário

**Quando** removo o nome e clico em "Salvar"

**Então** o sistema deve informar que o campo é obrigatório.

### Cenário 5 : Atualização de múltiplos dados

**Dado** que existe um usuário cadastrado

**Quando** altero nome, telefone e e-mail

**Então** o sistema deve salvar todas as alterações com sucesso.

---

# Funcionalidade : Exclusão de Usuário (Delete)

### Cenário 1 : Exclusão com sucesso

**Dado** que existe um usuário cadastrado

**Quando** clico em "Excluir" e confirmo a operação

**Então** o sistema deve remover o usuário da base de dados.

### Cenário 2 : Cancelamento da exclusão

**Dado** que existe um usuário cadastrado

**Quando** clico em "Excluir" e cancelo a confirmação

**Então** o sistema não deve remover o usuário.

### Cenário 3 : Usuário inexistente

**Dado** que o usuário já foi removido anteriormente

**Quando** tento excluí-lo novamente

**Então** o sistema deve informar que o registro não foi encontrado.

### Cenário 4 : Exclusão bloqueada por dependências

**Dado** que o usuário possui vínculos com outros registros

**Quando** tento excluí-lo

**Então** o sistema deve impedir a exclusão e informar o motivo.

### Cenário 5 : Registro da exclusão

**Dado** que existe um usuário cadastrado

**Quando** realizo sua exclusão

**Então** o sistema deve registrar a operação em log ou histórico.

---

# Princípios de Teste

## 1 : O teste mostra a presença de defeitos, não sua ausência

Os testes ajudam a encontrar falhas, porém não garantem que o sistema esteja totalmente livre de defeitos.

## 2 : Testes exaustivos são impossíveis

Não é viável testar todas as combinações possíveis de entradas e cenários existentes em um sistema.

## 3 : Testar cedo economiza tempo e dinheiro

Encontrar defeitos nas fases iniciais reduz custos de correção e retrabalho.

## 4 : Defeitos tendem a se agrupar

Grande parte dos erros geralmente está concentrada em poucas funcionalidades ou módulos.

## 5 : Paradoxo do pesticida

Executar sempre os mesmos testes reduz a capacidade de identificar novos defeitos, exigindo atualização constante dos cenários.

## 6 : O teste depende do contexto

A estratégia de testes deve variar de acordo com o tipo de sistema, tecnologia e objetivos do projeto.

## 7 : Ausência de erros é uma ilusão

Um sistema pode não apresentar defeitos conhecidos e ainda assim não atender às necessidades do usuário ou do negócio.
