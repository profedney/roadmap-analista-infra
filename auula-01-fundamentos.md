# Aula 01 - Fundamentos de Infraestrutura de TI

## Objetivo da Aula

Compreender os principais componentes da infraestrutura de TI e como eles trabalham juntos para permitir que os usuários utilizem sistemas, internet, e-mail e recursos corporativos.

---

# O que é Infraestrutura de TI?

Infraestrutura de TI é o conjunto de recursos físicos e lógicos que sustentam os serviços de tecnologia de uma organização.

Quando um usuário consegue:

- Fazer login no computador
- Acessar e-mails
- Utilizar o Microsoft Teams
- Navegar na internet
- Imprimir documentos
- Acessar sistemas corporativos

Existe uma infraestrutura trabalhando nos bastidores para tornar isso possível.

---

# Componentes da Infraestrutura

| Componente | Função |
|------------|---------|
| Computador | Estação de trabalho do usuário |
| Rede | Permite a comunicação entre dispositivos |
| Active Directory | Gerencia usuários e autenticação |
| DNS | Traduz nomes em endereços IP |
| DHCP | Distribui endereços IP automaticamente |
| Servidores | Executam aplicações e serviços |
| Microsoft 365 | Serviços de colaboração e produtividade |
| Firewall | Controla e protege o tráfego de rede |
| Backup | Recupera dados em caso de falhas |

---

# Analogia: Infraestrutura como uma Cidade

Para facilitar o entendimento, imagine uma cidade.

| Infraestrutura de TI | Cidade |
|----------------------|---------|
| Computadores | Casas |
| Usuários | Moradores |
| Rede | Ruas |
| DNS | Lista telefônica |
| DHCP | Distribuidor de endereços |
| Active Directory | Prefeitura |
| Firewall | Portaria da cidade |

Assim como uma cidade precisa funcionar de forma organizada para atender seus moradores, a infraestrutura de TI precisa funcionar corretamente para atender os usuários.

---

# Fluxo Básico de Comunicação

```text
Usuário
   ↓
Computador
   ↓
Rede
   ↓
DNS
   ↓
Servidor
   ↓
Aplicação
```

Quando um problema ocorre, o trabalho do analista é identificar em qual etapa a falha aconteceu.

---

# Exemplo Prático

### Situação

Usuário informa:

```text
Não consigo acessar o Outlook.
```

### Possíveis verificações

- O computador possui internet?
- O usuário consegue acessar outros sites?
- A senha está correta?
- A conta está bloqueada?
- Existe licença Microsoft 365 atribuída?
- O serviço Exchange Online está funcionando?

---

# Infraestrutura x Procedimento

Um profissional iniciante normalmente tende a decorar procedimentos.

Exemplo:

```text
Problema de Outlook → Reinstalar Outlook.
```

Um Analista de Infraestrutura pensa diferente:

```text
Problema de Outlook

↓
Rede está funcionando?
↓
DNS está resolvendo?
↓
Usuário autentica?
↓
Licença existe?
↓
Serviço Microsoft está operacional?
```

A diferença está no raciocínio.

---

# Conceito Importante

## Diagnosticar por Camadas

Sempre que receber um chamado, faça perguntas que eliminem possibilidades.

Exemplo:

```text
Usuário não consegue acessar o e-mail.
```

Perguntas úteis:

- A internet funciona?
- Outros usuários possuem o mesmo problema?
- O Teams funciona?
- O Outlook apresenta alguma mensagem de erro?
- O acesso via navegador funciona?

Quanto mais informações você obtém, menor fica a área da investigação.

---

# Resumo da Aula

✅ Infraestrutura é composta por diversos serviços trabalhando em conjunto.

✅ Problemas podem ocorrer em diferentes camadas.

✅ O papel do analista é descobrir onde está a falha.

✅ O objetivo não é decorar procedimentos, mas entender como os componentes se relacionam.

✅ O raciocínio analítico é mais importante que a memorização.

---

# Exercício Prático

## Situação

Um usuário informa:

```text
Não consigo acessar meu e-mail.
```

Qual item deve ser verificado primeiro?

A) Firewall

B) Se possui internet

C) Troca do computador

D) Comprar nova licença

---

# Questionário de Verificação

## Questão 1

O que faz o DNS?

A) Armazena arquivos

B) Entrega IP automaticamente

C) Traduz nomes para endereços IP

D) Cria usuários

---

## Questão 2

O que faz o DHCP?

A) Traduz nomes

B) Entrega IP automaticamente

C) Cria grupos no Active Directory

D) Controla impressoras

---

## Questão 3

Qual serviço normalmente controla usuários e senhas em ambientes Windows corporativos?

A) DHCP

B) DNS

C) Active Directory

D) Outlook

---

## Questão 4

Verdadeiro ou Falso:

```text
Um bom analista de infraestrutura precisa entender a comunicação entre os serviços e não apenas decorar procedimentos.
```

---

## Questão 5

Um usuário foi criado no Active Directory mas não consegue acessar o Microsoft 365.

Cite uma possível causa.

---

# Gabarito

## Exercício Prático

Resposta:

```text
B) Se possui internet
```

Motivo:

Antes de investigar sistemas ou licenças, é importante confirmar se o usuário possui conectividade.

---

## Questão 1

```text
C) Traduz nomes para endereços IP
```

---

## Questão 2

```text
B) Entrega IP automaticamente
```

---

## Questão 3

```text
C) Active Directory
```

---

## Questão 4

```text
Verdadeiro
```

---

## Questão 5

Possíveis respostas:

- Falha de sincronização com Microsoft Entra ID
- Licença Microsoft 365 não atribuída
- Problema no processo de provisionamento
- Falha de replicação

---

# Anotações Pessoais

Utilize este espaço para registrar observações e experiências adquiridas no trabalho.

```text
Data:
Tema:
Aprendizado:
Dúvidas:
```

---

# Próxima Aula

➡️ Aula 02 - Redes: IP, DNS e DHCP
