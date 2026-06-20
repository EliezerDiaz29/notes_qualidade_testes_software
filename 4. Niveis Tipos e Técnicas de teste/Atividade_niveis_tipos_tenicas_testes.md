# Atividade

## Anote as informações importantes sobre os Princípios, Tipos, Níveis e Técnicas de testes visto nessa aula, coloque exemplo de cada um deles na sua anotação.

---

# Princípios de Teste

## Pergunta: Quais são os princípios de teste?

### 1. O teste mostra a presença de defeitos, não sua ausência

**Princípio:**

Os testes ajudam a encontrar defeitos existentes no sistema, mas não garantem que o software esteja totalmente livre de erros.

**Exemplo:**

Um aplicativo de delivery passou em todos os testes realizados, mas apresentou falha ao processar pedidos feitos durante horários de pico.

### 2. Testes exaustivos são impossíveis

**Princípio:**

Não é possível testar todas as combinações de entradas e cenários existentes em um sistema.

**Exemplo:**

Um sistema de reservas de hotéis possui diferentes datas, quartos, formas de pagamento e perfis de usuários, tornando inviável testar todas as combinações possíveis.

### 3. Testar cedo economiza tempo e dinheiro

**Princípio:**

Encontrar defeitos nas fases iniciais reduz custos e evita retrabalho.

**Exemplo:**

Durante a análise do projeto foi identificado que uma regra de cálculo de comissão estava incorreta, evitando alterações futuras em várias telas e relatórios.

### 4. Defeitos tendem a se agrupar

**Princípio:**

Grande parte dos defeitos geralmente está concentrada em poucos módulos do sistema.

**Exemplo:**

Em um sistema acadêmico, a maioria dos problemas encontrados estava concentrada no módulo de matrícula dos alunos.

### 5. Paradoxo do pesticida

**Princípio:**

Os casos de teste devem ser revisados e atualizados constantemente.

**Exemplo:**

Após vários meses executando os mesmos testes de cadastro, novos erros só foram encontrados quando cenários diferentes passaram a ser avaliados.

### 6. O teste depende do contexto

**Princípio:**

Cada sistema exige estratégias de teste adequadas às suas características e objetivos.

**Exemplo:**

Um aplicativo de mensagens exige mais testes de desempenho e disponibilidade do que um sistema interno de controle de estoque.

### 7. Ausência de erros é uma ilusão

**Princípio:**

Mesmo sem defeitos conhecidos, o sistema pode não atender às necessidades do usuário.

**Exemplo:**

Uma plataforma de cursos funciona corretamente, mas não oferece recursos que os alunos consideram essenciais para o aprendizado.

---

# Níveis de Teste

## Pergunta: Quais são os níveis de teste?

### Teste Unitário

**Princípio:**

Validar pequenas partes do sistema de forma isolada.

**Características:**

- Testa funções, métodos ou classes.
- Facilita a identificação de defeitos.
- Normalmente é executado pelos desenvolvedores.

**Exemplo:**

Validar uma função responsável por calcular a média final de um estudante.

### Teste de Integração

**Princípio:**

Garantir que diferentes componentes do sistema funcionem corretamente em conjunto.

**Características:**

- Avalia a comunicação entre módulos.
- Verifica troca de informações.
- Identifica falhas de integração.

**Exemplo:**

Verificar se os dados inseridos em uma tela de pedidos são corretamente enviados para o sistema de faturamento.

### Teste de Sistema

**Princípio:**

Validar o funcionamento completo do sistema integrado.

**Características:**

- Avalia o sistema como um todo.
- Simula o uso real da aplicação.
- Verifica requisitos funcionais e não funcionais.

**Exemplo:**

Realizar todo o processo de aluguel de um veículo, desde o cadastro do cliente até a emissão do contrato.

### Teste de Aceitação

**Princípio:**

Confirmar que o sistema atende às necessidades do cliente e do negócio.

**Características:**

- Executado próximo da entrega.
- Pode envolver usuários finais.
- Valida requisitos de negócio.

**Exemplo:**

Os funcionários de uma empresa validam um novo sistema de ponto eletrônico antes de sua implantação oficial.

**Tipos de Aceitação:**

- Aceitação do usuário
- Aceitação operacional
- Aceitação contratual
- Teste Alfa
- Teste Beta

---

# Tipos de Teste

## Pergunta: Quais são os tipos de teste?

### Teste Funcional

**Princípio:**

Verificar se as funcionalidades funcionam conforme os requisitos definidos.

**Características:**

- Avalia entradas e saídas.
- Verifica regras de negócio.
- Analisa o comportamento esperado.

**Exemplo:**

Confirmar se a recuperação de senha envia corretamente o e-mail para o usuário.

### Teste Não Funcional

**Princípio:**

Avaliar atributos de qualidade do sistema.

**Características:**

- Analisa desempenho.
- Avalia segurança.
- Verifica usabilidade e confiabilidade.

**Exemplo:**

Avaliar quanto tempo uma página leva para carregar com 500 acessos simultâneos.

### Teste Caixa-Branca

**Princípio:**

Validar a lógica interna e a estrutura do código.

**Características:**

- Requer acesso ao código-fonte.
- Analisa caminhos de execução.
- Mede cobertura de código.

**Exemplo:**

Verificar se todas as condições de um método de cálculo de impostos foram executadas.

### Teste de Regressão

**Princípio:**

Garantir que alterações não prejudiquem funcionalidades já existentes.

**Características:**

- Executado após mudanças.
- Verifica funcionalidades antigas.
- Muito utilizado em manutenção.

**Exemplo:**

Após uma atualização no sistema de pagamentos, validar se a emissão de notas fiscais continua funcionando corretamente.

---

# Técnicas de Teste

## Pergunta: Quais são as técnicas de teste?

### Particionamento de Equivalência

**Princípio:**

Agrupar entradas semelhantes para reduzir a quantidade de testes sem perder cobertura.

**Características:**

- Divide os dados em classes.
- Reduz esforço de teste.
- Mantém eficiência da validação.

**Exemplo:**

Campo que aceita notas de 0 a 10.

- Classe inválida: -1
- Classe válida: 7
- Classe inválida: 11

### Análise de Valor Limite

**Princípio:**

Testar valores próximos dos limites permitidos.

**Características:**

- Foca nos extremos das entradas.
- Identifica falhas de validação.
- Complementa o particionamento.

**Exemplo:**

Campo que aceita idade entre 18 e 60 anos.

- 18
- 19
- 59
- 60

### Tabela de Decisão

**Princípio:**

Organizar regras de negócio complexas em combinações de condições e resultados.

**Características:**

- Facilita a análise de cenários.
- Reduz ambiguidades.
- Melhora a cobertura dos testes.

**Exemplo:**

Liberação de acesso baseada em usuário ativo e senha correta.

### Transição de Estado

**Princípio:**

Validar mudanças de comportamento conforme o estado atual do sistema.

**Características:**

- Analisa estados possíveis.
- Verifica transições válidas.
- Avalia regras de mudança.

**Exemplo:**

Status de um chamado técnico.

- Aberto
- Em atendimento
- Resolvido
- Encerrado

### Caso de Uso

**Princípio:**

Testar o sistema com base nos cenários reais de utilização.

**Características:**

- Simula ações dos usuários.
- Valida fluxos completos.
- Baseado em requisitos.

**Exemplo:**

Fluxo de compra em uma loja virtual.

- Adicionar produto ao carrinho
- Informar endereço
- Efetuar pagamento

### Suposição de Erro

**Princípio:**

Utilizar experiências anteriores para prever possíveis falhas.

**Características:**

- Baseada no conhecimento do testador.
- Focada em áreas críticas.
- Complementa outras técnicas.

**Exemplo:**

Testar a inserção de emojis, símbolos e textos muito longos em campos de observação.

### Teste Exploratório

**Princípio:**

Explorar o sistema livremente em busca de comportamentos inesperados.

**Características:**

- Não segue roteiro rígido.
- Baseado na experiência.
- Permite descobrir defeitos não previstos.

**Exemplo:**

Explorar um aplicativo bancário recém-desenvolvido procurando comportamentos inesperados durante a navegação.

### Teste Baseado em Checklist

**Princípio:**

Utilizar uma lista de verificações para garantir cobertura mínima dos testes.

**Características:**

- Fácil aplicação.
- Padroniza validações.
- Evita esquecimentos.

**Exemplo:**

Checklist de Cadastro de Cliente.

- Campos obrigatórios
- CPF válido
- E-mail válido
- Mensagens de confirmação

---

# Conceitos Importantes

## Pergunta: Qual a diferença entre erro, defeito e falha?

### Erro

**Princípio:**

É uma ação humana incorreta durante o desenvolvimento.

**Exemplo:**

O analista documentou incorretamente uma regra de cálculo de frete.

### Defeito (Bug)

**Princípio:**

É um problema existente no software causado por um erro humano.

**Exemplo:**

O sistema calcula frete grátis para pedidos que não atingiram o valor mínimo exigido.

### Falha

**Princípio:**

É o comportamento incorreto percebido durante a execução do sistema.

**Exemplo:**

Durante uma compra, o valor do frete exibido ao cliente está incorreto.