# Aula 02 - Redes na Prática (IP, DNS e DHCP)

## Objetivo da Aula

Compreender os conceitos fundamentais de redes utilizados diariamente por profissionais de suporte e infraestrutura.

Ao final desta aula você deverá ser capaz de:

- Entender o que é um endereço IP.
- Identificar a função do DHCP.
- Identificar a função do DNS.
- Compreender o papel do Gateway.
- Executar diagnósticos básicos de conectividade.
- Utilizar comandos fundamentais de troubleshooting.

---

# O que é uma Rede?

Uma rede é um conjunto de dispositivos conectados entre si para compartilhar informações e recursos.

Exemplos de dispositivos:

- Computadores
- Notebooks
- Impressoras
- Servidores
- Celulares
- Switches
- Roteadores

Quando você acessa um servidor, uma impressora ou um site, está utilizando a rede.

---

# O que é um Endereço IP?

Todo dispositivo conectado a uma rede precisa possuir um identificador único chamado **endereço IP**.

Exemplo:

| Equipamento | IP |
|------------|------------|
| Computador | 192.168.1.10 |
| Impressora | 192.168.1.20 |
| Servidor | 192.168.1.100 |

Podemos comparar o IP ao endereço de uma residência.

Sem endereço, não é possível localizar o destino.

---

# O que é DHCP?

DHCP significa:

**Dynamic Host Configuration Protocol**

Sua função é fornecer automaticamente:

- Endereço IP
- Máscara de Rede
- Gateway
- Servidor DNS

Sem DHCP, seria necessário configurar essas informações manualmente em cada equipamento.

---

# Exemplo de Configuração Recebida do DHCP

```text
IP:        192.168.1.100
Máscara:   255.255.255.0
Gateway:   192.168.1.1
DNS:       8.8.8.8
```

---

# O que é Gateway?

O Gateway é a "porta de saída" da rede.

Quando o computador deseja acessar algo fora da rede local, ele encaminha a solicitação para o Gateway.

Exemplo:

```text
Rede Local
192.168.1.0/24

Gateway
192.168.1.1
```

Fluxo simplificado:

```text
Computador
      ↓
Gateway
      ↓
Internet
```

---

# O que é DNS?

DNS significa:

**Domain Name System**

Sua função é traduzir nomes em endereços IP.

Por exemplo:

```text
www.microsoft.com
```

é convertido para um endereço IP que permite ao computador localizar o servidor correto.

---

# Exemplo Prático

Você digita:

```text
www.google.com
```

O computador pergunta ao DNS:

```text
Qual o IP do Google?
```

O DNS responde com um endereço IP e a comunicação é estabelecida.

---

# Problemas Comuns de DNS

Situação:

```text
Usuário informa que a internet está funcionando,
mas nenhum site abre.
```

Testes:

```cmd
ping 8.8.8.8
```

Resultado:

```text
Sucesso
```

Teste:

```cmd
ping google.com
```

Resultado:

```text
Falha
```

Possível causa:

✅ Problema de DNS

---

# Comandos Fundamentais

## Ver Configuração de Rede

```cmd
ipconfig
```

Exibe o endereço IP atual do computador.

---

## Ver Configuração Completa

```cmd
ipconfig /all
```

Exibe:

- IP
- Máscara
- Gateway
- DNS
- DHCP
- Endereço MAC

---

## Testar Comunicação

```cmd
ping 8.8.8.8
```

Verifica se existe comunicação com outro equipamento.

---

## Verificar Resolução DNS

```cmd
nslookup google.com
```

Consulta o DNS para descobrir o IP associado a um nome.

---

## Limpar Cache DNS

```cmd
ipconfig /flushdns
```

Remove registros DNS armazenados localmente.

---

# Sequência de Diagnóstico

Quando um usuário informa:

```text
Estou sem internet.
```

Utilize o seguinte roteiro:

### Passo 1

Verificar conexão física ou Wi-Fi.

---

### Passo 2

Verificar endereço IP.

```cmd
ipconfig
```

---

### Passo 3

Testar Gateway.

```cmd
ping <gateway>
```

Exemplo:

```cmd
ping 192.168.1.1
```

---

### Passo 4

Testar acesso externo.

```cmd
ping 8.8.8.8
```

---

### Passo 5

Testar DNS.

```cmd
ping google.com
```

ou

```cmd
nslookup google.com
```

---

# Exemplo de Chamado

## Relato do Usuário

```text
Consigo acessar as pastas da empresa,
mas nenhum site abre.
```

## Raciocínio

- Rede local funcionando ✅
- Usuário possui IP ✅
- Comunicação interna funcionando ✅
- Investigar acesso externo ✅
- Verificar DNS ✅

Possível causa:

```text
Falha de DNS
```

---

# Resumo da Aula

- Todo dispositivo na rede precisa de um endereço IP.
- O DHCP distribui configurações de rede automaticamente.
- O DNS traduz nomes em endereços IP.
- O Gateway conecta a rede local a outros destinos.
- Diagnósticos devem seguir uma sequência lógica.
- Comandos básicos podem resolver grande parte dos chamados de rede.

---

# Exercício Prático

## Situação

Um usuário informa:

```text
Consigo acessar as pastas da empresa,
mas nenhum site da internet abre.
```

Qual item você investigaria primeiro?

A) Impressora

B) Monitor

C) DNS e conectividade externa

D) Memória RAM

---

# Questionário de Verificação

## Questão 1

Qual comando exibe as configurações completas da rede?

A) ping

B) nslookup

C) ipconfig /all

D) net use

---

## Questão 2

Qual é a principal função do DNS?

A) Criar usuários

B) Traduzir nomes em endereços IP

C) Distribuir endereços IP

D) Compartilhar arquivos

---

## Questão 3

Um computador consegue executar:

```cmd
ping 8.8.8.8
```

mas não consegue executar:

```cmd
ping google.com
```

Qual a causa mais provável?

A) Impressora

B) Monitor

C) DNS

D) Mouse

---

## Questão 4

O que pode acontecer se o servidor DHCP estiver indisponível?

A) O Teams é removido

B) O usuário pode não receber um IP válido

C) O Active Directory é excluído

D) O Outlook é desinstalado

---

## Questão 5

Um usuário informa:

```text
Consigo acessar recursos internos da empresa,
mas nenhum site externo abre.
```

Explique qual seria sua linha inicial de investigação.

---

# Gabarito

EP.C

1.C

2.B

3.C

4.B

5.Conectividade externa / Gateway / DNS

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

➡️ Aula 03 - Active Directory
