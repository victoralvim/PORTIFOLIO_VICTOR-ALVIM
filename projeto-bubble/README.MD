# 🏗️ Gestão de Orçamentos: Bubble.io + Engenharia de Software

## 🎯 Objetivo
Desenvolver uma aplicação web de gestão utilizando a Inteligência Artificial do Bubble como acelerador, aplicando rigorosamente os fundamentos de engenharia de software para garantir segurança, escalabilidade e governança.

## 🔗 Link da Aplicação
[Acessar Versão de Teste](https://victrosittino-35167.bubbleapps.io/version-test?debug_mode=true)

---

## 📚 Metodologia e Boas Práticas Aplicadas

### 1. Análise Crítica e Atuação Humana
* **IA como Rascunho:** A inteligência artificial foi utilizada apenas para gerar o *Blueprint* inicial. A engenharia de software real ocorreu na refatoração.
* **Auditoria de Código:** Lógicas confusas de permissão e "visões de colaborador" geradas pela IA foram descartadas e reescritas manualmente para evitar falhas estruturais.

### 2. Arquitetura e Modelagem de Dados
* **Planejamento Prévio:** Estrutura de banco de dados documentada antes do desenvolvimento visual.
* **Otimização de Relações:** Referenciamento direto entre tabelas. Aplicação da regra estrita de evitar listas de dados em entidades pai que possam ultrapassar 100 itens.
* **Prevenção de Hardcode (Option Sets):** Uso de conjuntos de opções para *Status*, eliminando strings soltas e garantindo a integridade dos dados.

### 3. Front-end e Usabilidade (UX/UI)
* **Layout Responsivo:** Refatoração da interface utilizando conceitos de Flexbox (Row, Column, Alignments).
* **Correção de Fluxo de Navegação:** Implementação de links de retorno ("Voltar ao início") no rodapé, eliminando "becos sem saída" na navegação e garantindo que o usuário sempre tenha um ponto de saída ou retorno fácil.
* **Hierarquia Visual:** Ajuste de elementos estruturais para garantir que as informações de orçamento sejam legíveis em diferentes dispositivos.

### 4. Segurança e Privacidade (Privacy by Design)
* **Mitigação OWASP Top 10:** Remoção imediata da regra padrão `Publicly visible` de todas as tabelas sensíveis.
* **Isolamento de Dados:** Implementação da regra estrita `This Orçamento's Creator is Current User` na aba *Data > Privacy*. Isso impede o vazamento de dados no lado do cliente.

### 5. Desempenho e Otimização de Custos
* **Eficiência de Buscas (WUs):** Consultas ao banco de dados (`Do a search for`) restritas aos *Repeating Groups*. Consultas em células individuais foram eliminadas para otimizar o consumo de Workload Units.
* **Controle de APIs:** Configuração de limites técnicos (`max_tokens`) para proteger o sistema contra custos abusivos em integrações externas.

### 6. Governança e Controle (Anti-Shadow IT)
* **Organização Visual:** Workflows categorizados por cores (Ex: Verde para Sucesso, Vermelho para Exclusão).
* **Documentação In-Platform:** Utilização rigorosa do recurso *Notes* para documentar fluxos complexos, facilitando a manutenção futura.
