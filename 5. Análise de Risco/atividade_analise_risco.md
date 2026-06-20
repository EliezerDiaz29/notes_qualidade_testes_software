# Atividade - Análise de Risco

## Pergunta: Documente as questões de Análise de Risco apresentadas nos exercícios.

---

# Cenário 1 - Interrupção Temporária do Serviço devido a Manutenção Programada

## Descrição

O serviço é temporariamente interrompido para realizar manutenção programada, afetando temporariamente a acessibilidade, mas sem danos permanentes.

### Probabilidade

C - Possível

### Impacto

2 - Tolerável

### Matriz de Risco

2C - Baixo

### Testes Utilizados

- Teste de disponibilidade
- Teste de infraestrutura
- Teste de sistema
- Teste de regressão

### Estratégia de Mitigação

Planejar a manutenção em horários de menor utilização, informar os usuários antecipadamente e manter plano de rollback caso ocorram falhas durante a manutenção.

### Tipos de Risco

#### Técnico

- Indisponibilidade temporária do serviço
- Falhas durante atualizações
- Problemas de infraestrutura

#### Humano

- Falhas na execução dos procedimentos
- Comunicação inadequada com os usuários

#### Negócio

- Interrupção temporária das operações
- Reclamações dos usuários

---

# Cenário 2 - Vulnerabilidade de Segurança Descoberta em uma Dependência de Terceiros

## Descrição

Uma vulnerabilidade crítica é descoberta em uma biblioteca de terceiros usada pelo aplicativo, permitindo ataques de hackers para acessar dados sensíveis dos usuários.

### Probabilidade

D - Provável

### Impacto

5 - Crítico

### Matriz de Risco

5D - Muito Alto

### Testes Utilizados

- Teste de segurança
- Teste de vulnerabilidade
- Teste de penetração (Pentest)
- Teste de integração
- Análise estática de código

### Estratégia de Mitigação

Monitorar constantemente as dependências utilizadas, aplicar correções imediatamente, utilizar ferramentas de detecção de vulnerabilidades e implementar autenticação e criptografia adequadas.

### Tipos de Risco

#### Técnico

- Exposição de dados sensíveis
- Acesso não autorizado
- Execução de código malicioso

#### Humano

- Falta de atualização das dependências
- Configurações inseguras

#### Negócio

- Vazamento de dados
- Multas e penalidades legais
- Perda de credibilidade da empresa

---

# Cenário 3 - Erro de Interface do Usuário que Causa Confusão entre os Usuários

## Descrição

Uma alteração na interface do usuário causa confusão entre os usuários, mas não afeta a funcionalidade básica do aplicativo.

### Probabilidade

C - Possível

### Impacto

3 - Moderado

### Matriz de Risco

3C - Médio

### Testes Utilizados

- Teste funcional
- Teste de usabilidade
- Teste exploratório
- Teste de aceitação

### Estratégia de Mitigação

Realizar avaliações de usabilidade, coletar feedback dos usuários e validar alterações de interface antes da publicação.

### Tipos de Risco

#### Técnico

- Problemas de navegação
- Inconsistências visuais
- Dificuldade de utilização

#### Humano

- Interpretação incorreta de comandos
- Aumento de erros operacionais

#### Negócio

- Insatisfação dos usuários
- Aumento de chamados de suporte

---

# Cenário 4 - Falha em Processo de Backup de Dados

## Descrição

Uma falha no processo de backup de dados resulta na perda de uma quantidade significativa de dados dos usuários.

### Probabilidade

D - Provável

### Impacto

5 - Crítico

### Matriz de Risco

5D - Muito Alto

### Testes Utilizados

- Teste de recuperação
- Teste de continuidade de negócios
- Teste de integração
- Teste de sistema
- Teste de segurança

### Estratégia de Mitigação

Implementar backups automáticos, realizar testes periódicos de restauração, manter cópias redundantes e monitorar continuamente os processos de backup.

### Tipos de Risco

#### Técnico

- Corrupção de dados
- Falhas de armazenamento
- Erros na restauração

#### Humano

- Configuração incorreta dos backups
- Exclusão acidental de informações

#### Negócio

- Perda de dados críticos
- Prejuízos financeiros
- Danos à reputação da organização

---

# Cenário 5 - Ataque de Phishing aos Usuários do Aplicativo

## Descrição

Usuários recebem mensagens fraudulentas que simulam comunicações oficiais da empresa com o objetivo de roubar credenciais e informações pessoais.

### Probabilidade

D - Provável

### Impacto

5 - Crítico

### Matriz de Risco

5D - Muito Alto

### Testes Utilizados

- Teste de segurança
- Teste de autenticação
- Teste de engenharia social
- Teste de vulnerabilidade

### Estratégia de Mitigação

Implementar autenticação multifator (MFA), realizar campanhas de conscientização, monitorar atividades suspeitas e disponibilizar canais para denúncia de tentativas de fraude.

### Tipos de Risco

#### Técnico

- Roubo de credenciais
- Comprometimento de contas
- Exposição de informações sensíveis

#### Humano

- Usuários clicam em links maliciosos
- Compartilhamento involuntário de senhas

#### Negócio

- Vazamento de dados
- Perda de confiança dos clientes
- Danos financeiros e reputacionais

---

# Resumo da Matriz de Risco

| Cenário | Probabilidade | Impacto | Matriz | Classificação |
|----------|----------|----------|----------|----------|
| Interrupção por Manutenção | C | 2 | 2C | Baixo |
| Vulnerabilidade em Dependência | D | 5 | 5D | Muito Alto |
| Erro de Interface | C | 3 | 3C | Médio |
| Falha em Backup | D | 5 | 5D | Muito Alto |
| Ataque de Phishing | D | 5 | 5D | Muito Alto |