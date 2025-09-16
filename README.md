# Entendendo sobre Segurança e Identidade na Azure

Este repositório contém o resumo das lições aprendidas no laboratório sobre **Segurança e Identidade no Microsoft Azure**, incluindo conceitos fundamentais, boas práticas e ferramentas disponíveis.

---

## 🔑 Microsoft Entra ID (antigo Azure Active Directory)

- Serviço de gerenciamento de identidades e acesso baseado em nuvem.
- Responsável por representar e autenticar usuários, grupos e dispositivos.
- Permite sincronização com ambientes **on-premises** para manter a consistência das identidades.
- Principais recursos:
  - **Autenticação** (login dos usuários).
  - **Logon único (SSO)** para múltiplos aplicativos.
  - **Gerenciamento de dispositivos e aplicativos**.
  - **Colaboração B2B (Business-to-Business)**.
  - **Suporte a identidades externas (Google, Facebook, etc.)**.

### Fluxo de Sincronização
- Usuários e grupos locais podem ser sincronizados para o Entra ID através do **Microsoft Entra Connect**.
- Sincronização automática mantém as credenciais e permissões alinhadas.

### Gerenciamento de usuários
- Contas de usuário podem ser restauradas em até **30 dias** após exclusão.
- **SSPR (Self-Service Password Reset):** permite redefinição de senha sem depender do suporte técnico.
- Convites em massa para usuários externos podem ser realizados via **CSV**.
- É possível personalizar o domínio para uso do nome da empresa.

---

## 🔒 Autenticação e Autorização

- **Autenticação:** valida a identidade do usuário ou serviço (quem é você).
- **Autorização:** define o que o usuário ou serviço pode fazer (permissões).

### Autenticação Multifator (MFA)
- Requer dois ou mais métodos de verificação (senha + SMS, token, app, cartão).

### Identidades Externas
- **B2B:** colaboração com parceiros e fornecedores usando contas externas.
- **B2C:** integração com consumidores em aplicativos publicados.

---

## 🎯 Acesso Condicional

- Define regras baseadas em:
  - Associação a usuários ou grupos.
  - Localização do IP.
  - Tipo de dispositivo.
  - Aplicativo.
  - Detecção de risco.

Permite reforçar a segurança de acordo com o contexto do login.

---

## 🛠️ RBAC – Controle de Acesso Baseado em Função

- Permite **gerenciamento granular de permissões**.
- Segue o princípio do **menor privilégio** (dar apenas o acesso necessário).
- O permissionamento pode ser:
  - Em **nível de recurso**.
  - Em **grupo de recursos**.
  - Em **assinatura**.
- **Permissões são herdáveis**: se concedidas em um Resource Group, todos os recursos dentro dele também herdam.

> Diferença importante:
> - **Roles (Entra ID):** relacionadas a identidades e permissões administrativas.  
> - **RBAC (Azure):** relacionadas a recursos da nuvem (criação, exclusão, gerenciamento).

---

## 🛡️ Confiança Zero (Zero Trust)

- Modelo moderno de segurança que **não confia em nada por padrão**, mesmo dentro da rede corporativa.
- Compara-se ao modelo clássico que apenas restringia o perímetro da rede.
- No Zero Trust:
  - Identidade e acesso estão no centro da proteção.
  - Cada solicitação é validada e monitorada.

---

## 🏰 Defesa em Profundidade

- Estratégia em camadas para proteger ativos digitais.
- Proteções aplicadas em:
  - Segurança física
  - Identidade e acesso
  - Perímetro
  - Rede
  - Computação
  - Aplicativos
  - Dados

---

## 🛡️ Microsoft Defender for Cloud

- Serviço nativo de segurança do Azure.
- Funcionalidades:
  - **Recomendações de segurança**.
  - **Detecção e bloqueio de malware**.
  - **Análise e identificação de ataques potenciais**.
  - **Controle Just-in-Time** para portas de acesso.
- **Multicloud e híbrido:** pode monitorar ambientes AWS, GCP e locais.
- Integração com **DevOps** (GitHub, GitLab, Azure DevOps).
- Envio de alertas para **e-mail, Teams, Slack**, etc.
- Versões:
  - **Foundational (gratuito):** validação básica e recomendações de segurança.
  - **Planos pagos:** proteção avançada para VMs, storage, containers, bancos de dados, APIs, etc.

---

## 📊 Logs e Monitoramento

- O Entra ID permite consultar e analisar:
  - Local de login.
  - ID do usuário.
  - Data e hora.
  - Se o acesso ocorreu pelo portal ou por aplicativos.
- **Health:** exibe relatórios de disponibilidade (SLA).

---

## ✅ Conclusão

Durante este laboratório, aprendi como o **Microsoft Azure** lida com **identidade, acesso e segurança**, usando uma abordagem em camadas e ferramentas como **Microsoft Entra ID, RBAC, Acesso Condicional e Defender for Cloud**.  
Esses recursos juntos fortalecem a proteção de dados e garantem que apenas as pessoas certas tenham o acesso adequado aos recursos certos.
