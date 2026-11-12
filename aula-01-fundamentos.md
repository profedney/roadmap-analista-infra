# Aula 01 - Fundamentos de Infraestrutura de TI

## Objetivo da Aula

Compreender os principais componentes da infraestrutura de TI e como eles trabalham juntos para permitir que usuários utilizem computadores, internet, e-mail, sistemas corporativos e demais recursos tecnológicos.

---

# O que é Infraestrutura de TI?

Infraestrutura de TI é o conjunto de recursos físicos e lógicos responsáveis por suportar os serviços tecnológicos de uma organização.

Quando um usuário consegue:

- Fazer login no computador
- Acessar e-mails
- Navegar na internet
- Utilizar o Microsoft Teams
- Imprimir documentos
- Acessar sistemas corporativos

Existe uma infraestrutura funcionando nos bastidores para possibilitar essas atividades.

---

# Componentes da Infraestrutura

| Componente | Função |
|------------|---------|
| Computador | Estação de trabalho do usuário |
| Rede | Comunicação entre dispositivos |
| Servidores | Hospedam serviços e aplicações |
| Active Directory | Gerencia usuários e autenticação |
| DNS | Traduz nomes para endereços IP |
| DHCP | Distribui endereços IP automaticamente |
| Microsoft 365 | Serviços de produtividade e colaboração |
| Firewall | Protege e controla o tráfego de rede |
| Backup | Permite recuperação de dados |

---

# Analogia: Infraestrutura Como uma Cidade

Para facilitar o entendimento, imagine uma cidade:

| Infraestrutura de TI | Cidade |
|----------------------|---------|
| Computador | Casa |
| Usuário | Morador |
| Rede | Rua |
| DNS | Lista telefônica |
| DHCP | Distribuidor de endereços |
| Active Directory | Prefeitura |
| Firewall | Portaria |
| Servidores | Prédios públicos |

Assim como uma cidade depende de ruas, endereços e serviços para funcionar, uma empresa depende da infraestrutura de TI.

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

Quando algo não funciona, o objetivo do analista é descobrir em qual etapa ocorreu a falha.

---

# Exemplo Prático

## Situação

Um usuário informa:

```text
Não consigo acessar o Outlook.
```

Possíveis verificações:

- O computador possui acesso à internet?
- Outros sites funcionam?
- O usuário consegue entrar no Teams?
- A senha está correta?
- A conta está bloqueada?
- Existe licença atribuída?
- O serviço Microsoft está operacional?

---

# Infraestrutura x Decoração de Procedimentos

Um profissional iniciante normalmente pensa:

```text
Outlook não abre → Reinstalar Outlook.
```

Um Analista de Infraestrutura pensa:

```text
Outlook não abre
        ↓
Rede funcionando?
        ↓
DNS funcionando?
        ↓
Usuário autentica?
        ↓
Licença atribuída?
        ↓
Exchange Online disponível?
```

O foco deve ser entender o funcionamento dos serviços e não apenas decorar procedimentos.

---

# Diagnóstico por Camadas

Sempre elimine possibilidades através de perguntas.

Exemplo:

```text
O usuário não consegue acessar o e-mail.
```

Perguntas úteis:

- A internet funciona?
- Apenas este usuário está afetado?
- Outros serviços Microsoft funcionam?
- O acesso web funciona?
- Existe alguma mensagem de erro?

Quanto mais informações coletadas, mais rápido será o diagnóstico.

---

# Resumo da Aula

- Infraestrutura é composta por vários serviços trabalhando juntos.
- Problemas podem ocorrer em diferentes camadas.
- O papel do analista é identificar onde está a falha.
- Entender o funcionamento dos componentes é mais importante do que decorar procedimentos.
- Um bom diagnóstico começa pela coleta de informações.

---

# Exercício Prático

## Situação

Um usuário informa:

```text
Não consigo acessar meu e-mail.
```

Qual item deve ser verificado primeiro?

**A)** Firewall

**B)** Se possui internet

**C)** Troca do computador

**D)** Comprar nova licença

---

# Questionário de Verificação

## Questão 1

O que faz o DNS?

**A)** Armazena arquivos

**B)** Entrega IP automaticamente

**C)** Traduz nomes para endereços IP

**D)** Cria usuários

---

## Questão 2

O que faz o DHCP?

**A)** Traduz nomes

**B)** Entrega IP automaticamente

**C)** Cria grupos no Active Directory

**D)** Controla impressoras

---

## Questão 3

Qual serviço normalmente controla usuários e senhas em ambientes Windows corporativos?

**A)** DHCP

**B)** DNS

**C)** Active Directory

**D)** Outlook

---

## Questão 4

Verdadeiro ou Falso:

```text
Um bom analista de infraestrutura precisa entender a
comunicação entre os serviços e não apenas decorar procedimentos.
```

---

## Questão 5

Um usuário foi criado no Active Directory mas não consegue acessar o Microsoft 365.

Cite uma possível causa.

---

# Gabarito

EP.B

1.C

2.B

3.C

4.V

5.Sincronização / Licença

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

➡️ Aula 02 - Redes: IP, DNS e DHCP
