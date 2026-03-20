# DeployDash
Automação de Infraestrutura como Código (IaC) para provisionamento de usuários, grupos e permissões em sistemas Linux via Shell Script.

#  Infraestrutura como Código: Script de Criação de Usuários e Permissões

Este projeto faz parte de um desafio prático de Linux. O objetivo é automatizar a criação de toda a infraestrutura de usuários, grupos, diretórios e permissões de um sistema Linux utilizando **Shell Script**.

## Objetivo do Projeto

Criar um script que possa ser executado em qualquer nova instalação Linux, deixando a máquina pronta para uso com:
- Grupos de departamentos (ADM, VEN, SEC).
- Usuários específicos associados aos seus respectivos grupos.
- Diretórios de departamentos com permissões restritas.
- Um diretório público acessível a todos.

---

## 🛠️ Estrutura do Script (`iac1.sh`)

O script realiza as seguintes etapas:
1. **Limpeza:** Remove diretórios e grupos criados anteriormente (para garantir um estado limpo).
2. **Diretórios:** Cria as pastas `/publico`, `/adm`, `/ven` e `/sec`.
3. **Grupos:** Cria os grupos `GRP_ADM`, `GRP_VEN` e `GRP_SEC`.
4. **Usuários:** Cria 9 usuários com senhas criptografadas e os adiciona aos grupos corretos.
5. **Permissões:** - Define o `root` como dono de todos os diretórios.
   - Define os grupos como proprietários de suas respectivas pastas.
   - Aplica a permissão `770` (acesso total apenas para dono e grupo) nas pastas restritas.
   - Aplica a permissão `777` na pasta pública.

---

##  Como executar o projeto

### Pré-requisitos
- Uma máquina Linux (Ubuntu, Debian, CentOS, etc.).
- Permissões de superusuário (root).

### Passo a passo
1. Clone este repositório:
   ```bash
   git clone [https://github.com/SEU_USUARIO/linux-projeto1-iac.git](https://github.com/SEU_USUARIO/linux-projeto1-iac.git)
