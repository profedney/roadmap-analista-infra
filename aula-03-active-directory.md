# Aula 03 - Active Directory

## Objetivo da Aula

Compreender os conceitos fundamentais do Active Directory (AD), sua importância em ambientes corporativos e como ele é utilizado para gerenciar usuários, computadores, grupos e permissões.

Ao final desta aula você deverá ser capaz de:

- Entender o que é o Active Directory.
- Compreender o conceito de domínio.
- Entender o papel das OUs.
- Entender a importância dos grupos.
- Conhecer o funcionamento básico das GPOs.
- Entender a integração entre AD e Microsoft 365.

---

# O que é o Active Directory?

O Active Directory (AD) é um serviço da Microsoft utilizado para centralizar o gerenciamento de identidades e recursos dentro de uma organização.

Ele armazena informações sobre:

- Usuários
- Computadores
- Grupos
- Impressoras
- Servidores
- Políticas de segurança

Em vez de administrar cada computador individualmente, o administrador realiza o gerenciamento de forma centralizada.

---

# Exemplo Prático

Imagine uma empresa com 500 colaboradores.

Sem Active Directory:

- Cada computador teria usuários locais.
- As senhas seriam administradas individualmente.
- O controle de permissões seria complexo.

Com Active Directory:

✅ Um único usuário pode acessar diversos recursos.

✅ As permissões são controladas centralmente.

✅ As políticas são aplicadas automaticamente.

---

# O que é um Domínio?

Um domínio é uma estrutura lógica que centraliza a autenticação dos usuários.

Exemplos:

```text
EMPRESA\edney
```

ou

```text
edney@empresa.com
```

Ao realizar login no computador corporativo, o usuário normalmente está autenticando contra o domínio da empresa.

---

# Fluxo Simplificado de Autenticação

```text
Usuário
    ↓
Computador
    ↓
Active Directory
    ↓
Validação da Senha
    ↓
Acesso Concedido
```

Se a senha estiver correta e a conta estiver habilitada, o acesso será permitido.

---

# O que são OUs?

OU significa:

**Organizational Unit (Unidade Organizacional)**

As OUs servem para organizar objetos dentro do Active Directory.

---

## Exemplo de Estrutura

```text
MODULAR
│
├── TI
├── RH
├── Financeiro
├── Comercial
├── Usuários
├── Computadores
└── Impressoras
```

Essa organização facilita a administração do ambiente.

---

# Benefícios das OUs

- Melhor organização.
- Aplicação de políticas específicas.
- Delegação de administração.
- Facilidade na localização de objetos.

---

# O que são Grupos?

Grupos são utilizados para gerenciar permissões de forma centralizada.

Ao invés de conceder acesso individualmente:

❌ João

❌ Maria

❌ Pedro

Criamos um grupo:

```text
FINANCEIRO_LEITURA
```

E adicionamos os usuários a ele.

---

# Vantagens dos Grupos

- Menor esforço administrativo.
- Padronização de acessos.
- Facilidade para auditorias.
- Controle simplificado de permissões.

---

# O que é uma GPO?

GPO significa:

**Group Policy Object**

É um conjunto de configurações aplicadas automaticamente aos computadores e usuários.

---

## Exemplos de GPO

- Definir papel de parede corporativo.
- Instalar impressoras automaticamente.
- Mapear unidades de rede.
- Bloquear o Painel de Controle.
- Impedir instalação de programas.
- Configurar políticas de senha.

---

# Exemplo Prático de GPO

Usuário faz login.

Automaticamente:

```text
Drive Z: é mapeado.
Impressora do setor é instalada.
Políticas de segurança são aplicadas.
```

Tudo sem necessidade de configuração manual.

---

# Active Directory e Microsoft 365

Em muitas empresas existe integração entre o Active Directory local e o Microsoft 365.

Fluxo comum:

```text
Active Directory Local
          ↓
Microsoft Entra Connect
          ↓
Microsoft Entra ID
          ↓
Microsoft 365
```

---

# Exemplo Real

Situação:

```text
Usuário criado no Active Directory.
```

Após algumas horas:

```text
Usuário não aparece no Microsoft 365.
```

Possíveis causas:

- Falha de sincronização.
- Serviço Entra Connect parado.
- Erro de configuração.
- Problema de provisionamento.

---

# Objetos Mais Comuns do Active Directory

| Objeto | Função |
|----------|----------|
| Usuário | Representa uma pessoa |
| Computador | Representa uma estação ou servidor |
| Grupo | Centraliza permissões |
| OU | Organiza objetos |
| GPO | Aplica configurações |
| Contato | Armazena informações de contato |

---

# Situações Comuns no Suporte

## Redefinir Senha

Chamado:

```text
Esqueci minha senha.
```

Ação:

```text
Reset de senha no Active Directory.
```

---

## Desbloquear Usuário

Chamado:

```text
Minha conta está bloqueada.
```

Ação:

```text
Unlock Account.
```

---

## Adicionar Acesso

Chamado:

```text
Usuário precisa acessar pasta Financeiro.
```

Ação:

```text
Adicionar usuário ao grupo adequado.
```

---

## Verificar Sincronização

Chamado:

```text
Usuário criado no AD não aparece no Microsoft 365.
```

Ação:

```text
Verificar sincronização do Entra Connect.
```

---

# Resumo da Aula

- O Active Directory centraliza o gerenciamento de usuários e recursos.
- O domínio controla autenticação e identidade.
- As OUs organizam os objetos.
- Os grupos facilitam o gerenciamento de permissões.
- As GPOs aplicam configurações automaticamente.
- O AD pode sincronizar informações com o Microsoft 365.

---

# Exercício Prático

## Situação

Você criou um usuário no Active Directory.

Após duas horas:

```text
O login Windows funciona.
O usuário não aparece no Microsoft 365.
```

Qual componente deve ser investigado primeiro?

A) Monitor

B) Impressora

C) Entra Connect / Sincronização

D) Memória RAM

---

# Questionário de Verificação

## Questão 1

Qual é a principal função do Active Directory?

A) Navegar na internet

B) Centralizar identidades e recursos

C) Fazer backup

D) Criar planilhas

---

## Questão 2

O que é uma OU?

A) Um antivírus

B) Uma estrutura de organização dentro do Active Directory

C) Um servidor DNS

D) Uma licença Microsoft

---

## Questão 3

Qual a principal vantagem dos grupos?

A) Organizar permissões de forma centralizada

B) Aumentar a velocidade da internet

C) Substituir o DHCP

D) Criar impressoras

---

## Questão 4

O que é uma GPO?

A) Um antivírus

B) Uma política aplicada automaticamente aos usuários ou computadores

C) Um servidor de e-mail

D) Um endereço IP

---

## Questão 5

Cite uma situação comum de suporte que envolva:

- Active Directory
- Grupo
- GPO
- Sincronização Microsoft 365

Explique como o problema pode estar relacionado a um desses componentes.

---

# Gabarito

EP.C

1.B

2.B

3.A

4.B

5.Resposta discursiva

---

# Anotações Pessoais

```text
Data:

Tema:

Aprendizado:

Dúvidas:

Observações:
```

---

# Próxima Aula

➡️ Aula 04 - Como Funciona a Autenticação no Active Directory
