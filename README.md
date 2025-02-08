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
 

---

# Documento de Requisitos (Sistema de Service Desk) - **Formato Ágil (Scrum)**

## 1. **User Stories - Requisitos Funcionais**

### 1.1 **Criação de Chamados (Tickets)**

- **História de Usuário:**  
  Como **usuário final**, eu quero **poder criar chamados de suporte** para que **eu possa relatar problemas ou solicitações de maneira fácil e organizada**.

- **Critérios de Aceitação:**
  - O sistema deve permitir a criação de chamados via formulário.
  - O formulário deve incluir campos como: título do chamado, descrição, categoria, prioridade e anexos.
  - O usuário pode criar chamados por e-mail ou diretamente pelo portal do sistema.

---

### 1.2 **Atribuição Automática de Chamados**

- **História de Usuário:**  
  Como **gestor de suporte**, eu quero **que os chamados sejam automaticamente atribuídos a equipes ou técnicos responsáveis** para que **os chamados sejam tratados rapidamente sem intervenção manual**.

- **Critérios de Aceitação:**
  - O sistema deve atribuir os chamados automaticamente com base em regras de roteamento (tipo de incidente, prioridade, etc.).
  - Deve ser possível configurar grupos de suporte com especialidades.
  - O sistema deve permitir a reassigenação manual caso necessário.

---

### 1.3 **Gestão de Prioridades**

- **História de Usuário:**  
  Como **técnico de suporte**, eu quero **poder atribuir prioridades aos chamados** para que **os chamados mais críticos sejam tratados primeiro**.

- **Critérios de Aceitação:**
  - O sistema deve permitir definir as prioridades como: Baixa, Média, Alta e Crítica.
  - O técnico pode alterar a prioridade de um chamado.
  - O sistema deve permitir visualizar os chamados por prioridade.

---

### 1.4 **Base de Conhecimento (KB)**

- **História de Usuário:**  
  Como **técnico de suporte**, eu quero **ter acesso à base de conhecimento** para que **eu possa consultar artigos e soluções de problemas comuns**.

- **Critérios de Aceitação:**
  - O sistema deve permitir o acesso à base de conhecimento por técnicos e usuários finais.
  - Os artigos devem ser pesquisáveis e categorizados.
  - O sistema deve sugerir artigos da base de conhecimento durante a criação ou atualização de chamados.

---

### 1.5 **Monitoramento e SLA (Acordo de Nível de Serviço)**

- **História de Usuário:**  
  Como **gestor de TI**, eu quero **monitorar o cumprimento dos SLAs** para que **eu possa garantir que os chamados estão sendo tratados dentro do prazo acordado**.

- **Critérios de Aceitação:**
  - O sistema deve permitir definir SLAs para diferentes tipos de incidentes.
  - O sistema deve gerar alertas quando um SLA estiver prestes a ser violado.
  - Relatórios sobre cumprimento de SLAs devem estar disponíveis para análise.

---

### 1.6 **Comunicação com o Usuário (Notificações)**

- **História de Usuário:**  
  Como **usuário final**, eu quero **ser notificado sobre o andamento do meu chamado** para que **eu possa saber o status e o progresso da minha solicitação**.

- **Critérios de Aceitação:**
  - O sistema deve enviar notificações por e-mail ou SMS quando o status do chamado for alterado.
  - O usuário pode responder às notificações para atualizar o chamado.
  - O técnico pode deixar comentários internos ou externos.

---

### 1.7 **Relatórios e Análises**

- **História de Usuário:**  
  Como **gestor de TI**, eu quero **acessar relatórios detalhados sobre os chamados e o desempenho da equipe de suporte** para que **eu possa tomar decisões baseadas em dados**.

- **Critérios de Aceitação:**
  - O sistema deve gerar relatórios customizáveis com filtros por data, categoria, prioridade, etc.
  - O sistema deve fornecer dashboards em tempo real com KPIs de desempenho.
  - O gestor pode exportar os relatórios para análise externa.

---

### 1.8 **Escalonamento de Chamados**

- **História de Usuário:**  
  Como **técnico de suporte**, eu quero **escalar um chamado para outro nível de suporte** quando **não conseguir resolver o problema dentro do prazo estabelecido ou quando o problema for complexo**.

- **Critérios de Aceitação:**
  - O sistema deve permitir o escalonamento de chamados para níveis superiores (ex: Nível 2, Nível 3).
  - O sistema deve registrar todo o histórico de interações ao escalar um chamado.
  - Notificações automáticas devem ser enviadas para os gestores e equipes responsáveis.

---

### 1.9 **Gestão de Recursos de TI**

- **História de Usuário:**  
  Como **gestor de TI**, eu quero **associar chamados a recursos de TI específicos** para que **eu possa rastrear problemas relacionados a equipamentos ou softwares da empresa**.

- **Critérios de Aceitação:**
  - O sistema deve permitir associar chamados a recursos específicos (computadores, servidores, softwares, etc.).
  - Deve ser possível consultar o histórico de manutenção e incidentes de cada recurso.
  - Relatórios sobre falhas recorrentes devem ser gerados.

---

### 1.10 **Acesso e Permissões de Usuários**

- **História de Usuário:**  
  Como **administrador do sistema**, eu quero **configurar permissões de acesso baseadas em funções** para que **cada usuário tenha acesso apenas às funcionalidades necessárias para seu trabalho**.

- **Critérios de Aceitação:**
  - O sistema deve permitir criar e gerenciar funções de usuários (Admin, Técnico, Usuário Final, etc.).
  - Permissões devem ser configuráveis para cada função, permitindo acessar, editar ou visualizar funcionalidades específicas.
  - O sistema deve manter um log de auditoria para todas as ações realizadas pelos usuários.

---

## 2. **User Stories - Requisitos Não Funcionais**

### 2.1 **Escalabilidade**

- **História de Usuário:**  
  Como **administrador de infraestrutura**, eu quero **que o sistema seja escalável** para que **ele possa crescer junto com a empresa, suportando um aumento no número de usuários e chamados sem perda de desempenho**.

- **Critérios de Aceitação:**
  - O sistema deve permitir adicionar novos servidores sem afetar a operação.
  - O desempenho do sistema deve se manter estável durante picos de uso (ex: mais de 1.000 usuários simultâneos).
  - O sistema deve ser capaz de lidar com um grande volume de dados e transações.

---

### 2.2 **Segurança**

- **História de Usuário:**  
  Como **usuário final**, eu quero **que meus dados sejam protegidos contra acessos não autorizados** para que **minhas informações pessoais e de segurança estejam sempre seguras**.

- **Critérios de Aceitação:**
  - O sistema deve utilizar criptografia para proteger dados sensíveis.
  - A autenticação multi-fator deve ser implementada para o acesso ao sistema.
  - O sistema deve ter backups regulares e planos de recuperação de dados em caso de falhas.

---

### 2.3 **Usabilidade**

- **História de Usuário:**  
  Como **usuário final**, eu quero **ter uma interface intuitiva e fácil de usar** para que **eu possa navegar pelo sistema sem dificuldades**.

- **Critérios de Aceitação:**
  - O sistema deve ser fácil de navegar, com uma interface limpa e organizada.
  - A curva de aprendizado para usuários novos deve ser mínima.
  - O sistema deve ter uma seção de ajuda e FAQs acessíveis a partir de qualquer página.

---

### 2.4 **Desempenho**

- **História de Usuário:**  
  Como **usuário final**, eu quero **que o sistema tenha um tempo de resposta rápido** para que **eu possa interagir com ele sem frustração ou atrasos**.

- **Critérios de Aceitação:**
  - O tempo de resposta de cada ação no sistema deve ser inferior a 2 segundos.
  - O sistema deve carregar as páginas rapidamente, mesmo com muitos dados.
  - O desempenho deve ser mantido com um número alto de usuários simultâneos.

---

### 2.5 **Disponibilidade**

- **História de Usuário:**  
  Como **usuário final**, eu quero **que o sistema esteja disponível 24/7** para que **eu possa acessar e registrar chamados a qualquer momento**.

- **Critérios de Aceitação:**
  - O sistema deve ter uma disponibilidade de 99,9% ou superior.
  - Deve haver redundância e failover para garantir a continuidade do serviço.
  - O sistema deve ser monitorado constantemente para identificar falhas antes que afetem os usuários.

---

