# Script de Criação de Usuários e Permissões Linux

Script Bash desenvolvido para automatizar a criação de diretórios, grupos e usuários em um ambiente Linux, além de configurar permissões de acesso aos diretórios.

##  Objetivo

Automatizar tarefas básicas de administração de usuários e permissões no Linux, utilizando Bash.

O script realiza:

* Criação de diretórios;
* Criação de grupos;
* Criação de usuários;
* Associação dos usuários aos seus respectivos grupos;
* Definição do proprietário e grupo dos diretórios;
* Configuração das permissões de acesso.

##  Diretórios

O script cria os seguintes diretórios:

```text
/publico
/adm
/ven
/sec
```

### Permissões

| Diretório  | Grupo     | Permissão |
| ---------- | --------- | --------- |
| `/adm`     | `GRP_ADM` | `770`     |
| `/ven`     | `GRP_VEN` | `770`     |
| `/sec`     | `GRP_SEC` | `770`     |
| `/publico` | —         | `777`     |

Os diretórios `/adm`, `/ven` e `/sec` pertencem ao usuário `root` e aos seus respectivos grupos.

##  Grupos

Foram criados três grupos:

```text
GRP_ADM
GRP_VEN
GRP_SEC
```

Os usuários são adicionados aos grupos correspondentes durante a criação.

## 🛠️ Tecnologias e comandos

O projeto utiliza:

* Bash
* Linux
* `mkdir`
* `groupadd`
* `useradd`
* `chown`
* `chmod`
* `openssl`

##  Como executar

O script deve ser executado com privilégios administrativos.

```bash
chmod +x script.sh
sudo ./script.sh
```

Como o script cria usuários, grupos e diretórios diretamente no sistema, é necessário executá-lo como `root` ou utilizando `sudo`.

##  Observações

Este projeto foi desenvolvido como exercício prático de administração Linux e automação com Bash.

As senhas utilizadas no script são apenas para fins de laboratório e aprendizado. Em um ambiente real, não é recomendado armazenar senhas diretamente no código.

##  Conceitos praticados

* Gerenciamento de usuários Linux
* Gerenciamento de grupos
* Permissões de arquivos e diretórios
* Proprietário e grupo (`chown`)
* Permissões (`chmod`)
* Automação de tarefas administrativas com Bash
