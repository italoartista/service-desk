# Documento de Requisitos: Sistema de Service Desk

## 1. **Requisitos Funcionais**

### 1.1 **Criação de Chamados (Tickets)**

- **Descrição:** O sistema deve permitir que os usuários registrem chamados (tickets) para relatar incidentes ou solicitações. Esses chamados devem ser categorizados de acordo com o tipo de serviço (ex: TI, RH, Facilities).
- **Objetivo:** Facilitar a solicitação de suporte ou atendimento, organizando a demanda de forma eficiente.
- **Detalhamento:**
  - O usuário deve poder preencher um formulário com informações sobre o problema.
  - O formulário deve incluir campos como: título do chamado, descrição detalhada, categoria, prioridade, e anexos (screenshots, logs).
  - Chamados podem ser criados por e-mail ou diretamente pelo portal do sistema.

### 1.2 **Atribuição Automática de Chamados**

- **Descrição:** O sistema deve ser capaz de atribuir automaticamente os chamados para os técnicos ou equipes responsáveis, com base em critérios definidos, como tipo de problema e prioridade.
- **Objetivo:** Agilizar o processo de triagem e direcionamento dos chamados.
- **Detalhamento:**
  - Definir regras de roteamento baseadas em categorias de incidentes ou solicitações.
  - Permitir a configuração de grupos de suporte, cada um com suas especialidades.
  - Atribuição de chamado deve ser feita automaticamente, mas com possibilidade de reassigenação manual por supervisores.

### 1.3 **Gestão de Prioridades**

- **Descrição:** O sistema deve permitir a definição e gestão de prioridades dos chamados, com base no impacto e urgência, possibilitando que chamados mais críticos sejam tratados de forma prioritária.
- **Objetivo:** Garantir que os problemas mais urgentes sejam tratados com a máxima atenção.
- **Detalhamento:**
  - Definir diferentes níveis de prioridade (Ex: Baixa, Média, Alta, Crítica).
  - Possibilidade de alterar a prioridade de um chamado com base em reavaliação.
  - Visualização de chamados por prioridade em relatórios e dashboards.

### 1.4 **Base de Conhecimento (KB)**

- **Descrição:** O sistema deve contar com uma base de conhecimento acessível tanto pelos técnicos quanto pelos usuários, contendo artigos de resolução de problemas comuns.
- **Objetivo:** Reduzir o tempo de resolução de chamados e aumentar a eficiência do suporte.
- **Detalhamento:**
  - Artigos devem ser criados, revisados e atualizados por equipes de suporte.
  - Artigos devem ser categorizados e pesquisáveis, com palavras-chave.
  - Integração com os chamados, permitindo que o técnico sugira artigos da KB durante a interação com o usuário.

### 1.5 **Monitoramento e SLA (Acordo de Nível de Serviço)**

- **Descrição:** O sistema deve permitir o monitoramento do tempo de resposta e resolução dos chamados, garantindo que os SLAs (Service Level Agreements) sejam atendidos.
- **Objetivo:** Assegurar que os chamados sejam resolvidos dentro do tempo acordado com o cliente ou usuário.
- **Detalhamento:**
  - Definir SLAs específicos por tipo de incidente e prioridade.
  - Notificação automática para técnicos e gestores quando os SLAs estiverem prestes a ser violados.
  - Relatórios de cumprimento de SLA, com métricas de tempo de resposta e resolução.

### 1.6 **Comunicação com o Usuário (Notificações)**

- **Descrição:** O sistema deve permitir a comunicação contínua entre o usuário e o técnico durante a vida útil do chamado.
- **Objetivo:** Manter o usuário informado sobre o andamento do seu chamado e fornecer atualizações.
- **Detalhamento:**
  - Envio de notificações automáticas por e-mail ou SMS sobre o status do chamado (aberto, em andamento, fechado).
  - O usuário deve poder responder diretamente às notificações, o que atualiza automaticamente o chamado no sistema.
  - O técnico deve poder deixar comentários internos ou externos para atualização.

### 1.7 **Relatórios e Análises**

- **Descrição:** O sistema deve fornecer relatórios detalhados sobre a performance do suporte, como tempos médios de resolução, chamados por categoria, etc.
- **Objetivo:** Ajudar gestores a analisar o desempenho do time de suporte e tomar decisões baseadas em dados.
- **Detalhamento:**
  - Relatórios personalizáveis com filtros por data, tipo de incidente, time de suporte, prioridade, etc.
  - Análise de tendências, como aumento no número de chamados em determinados períodos.
  - Dashboards em tempo real com métricas-chave de desempenho (KPIs).

### 1.8 **Escalonamento de Chamados**

- **Descrição:** O sistema deve permitir o escalonamento de chamados para níveis superiores quando a resolução não for possível dentro do tempo estabelecido ou em casos mais complexos.
- **Objetivo:** Garantir que problemas mais difíceis ou que não podem ser resolvidos rapidamente sejam tratados adequadamente.
- **Detalhamento:**
  - Definir níveis de escalonamento (Ex: Nível 1, Nível 2, Nível 3).
  - O sistema deve permitir a transferência do chamado entre diferentes níveis com registro completo da interação.
  - Notificação de escalonamento para os gestores e responsáveis.

### 1.9 **Gestão de Recursos de TI**

- **Descrição:** O sistema deve ter integração com a gestão de recursos de TI (como hardware e software) para registrar e associar problemas a equipamentos ou ferramentas específicas.
- **Objetivo:** Melhorar o rastreamento de incidentes relacionados a recursos e facilitar a resolução.
- **Detalhamento:**
  - Permitir associar chamados a equipamentos, softwares ou outros recursos da empresa.
  - Registrar histórico de manutenção e incidentes associados a cada recurso.
  - Relatórios sobre falhas recorrentes em determinados equipamentos.

### 1.10 **Acesso e Permissões de Usuários**

- **Descrição:** O sistema deve permitir controle de acesso baseado em funções, garantindo que os usuários acessem apenas as informações relevantes para seu trabalho.
- **Objetivo:** Proteger dados sensíveis e garantir que cada usuário tenha acesso adequado aos recursos do sistema.
- **Detalhamento:**
  - Definir funções como Administrador, Técnico, Usuário Final, Gestor.
  - Controle de permissões por função (Ex: técnicos podem editar chamados, mas usuários finais só podem visualizar).
  - Auditoria de ações realizadas por cada usuário.

---

## 2. **Requisitos Não Funcionais**

### 2.1 **Escalabilidade**

- **Descrição:** O sistema deve ser escalável para suportar o crescimento da empresa e o aumento do número de chamados.
- **Objetivo:** Garantir que o sistema consiga lidar com grandes volumes de dados e usuários sem comprometer o desempenho.
- **Detalhamento:**
  - Arquitetura do sistema deve permitir a adição de novos servidores ou recursos sem interrupções.
  - O sistema deve ser capaz de suportar picos de utilização, como durante grandes campanhas de suporte ou novos lançamentos de tecnologia.

### 2.2 **Segurança**

- **Descrição:** O sistema deve garantir a segurança dos dados, protegendo as informações pessoais e sensíveis de usuários e técnicos.
- **Objetivo:** Proteger contra acessos não autorizados e garantir a confidencialidade dos dados.
- **Detalhamento:**
  - Implementação de criptografia em dados sensíveis (como senhas e informações pessoais).
  - Autenticação multi-fator para acesso ao sistema.
  - Políticas de backup regular e recuperação de dados.

### 2.3 **Usabilidade**

- **Descrição:** O sistema deve ser fácil de usar, com uma interface amigável para todos os tipos de usuários (técnicos, gestores, e usuários finais).
- **Objetivo:** Garantir que o sistema seja eficiente e que a curva de aprendizado seja mínima.
- **Detalhamento:**
  - Interface intuitiva, com fácil navegação entre as funcionalidades.
  - Treinamento mínimo necessário para o uso diário do sistema.
  - Documentação de ajuda online e FAQs.

### 2.4 **Desempenho**

- **Descrição:** O sistema deve garantir alta performance, com tempos de resposta rápidos para consultas e interações, mesmo com um grande número de usuários simultâneos.
- **Objetivo:** Assegurar que o sistema funcione sem lentidão ou quedas, mesmo em ambientes de alto tráfego.
- **Detalhamento:**
  - O tempo de resposta das páginas deve ser inferior a 2 segundos para ações comuns.
  - O sistema deve suportar mais de 1.000 usuários simultâneos sem comprometer o desempenho.

### 2.5 **Disponibilidade**

- **Descrição:** O sistema deve ter alta disponibilidade, com mínimo tempo de inatividade e tolerância a falhas.
- **Objetivo:** Garantir que o serviço esteja disponível 24/7 para todos os usuários da empresa.
- **Detalhamento:**
  - O sistema deve ter uma taxa de disponibilidade superior a 99,9%.
  - Implementação de redundância e failover em servidores para minimizar o impacto de falhas.
  - Monitoramento contínuo do sistema para detectar problemas antes que impactem os usuários.
