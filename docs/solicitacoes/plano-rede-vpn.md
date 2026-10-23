# Planejamento de rede e VPN — LAPEA e futura VM

**Estado:** planejamento; não constitui solicitação de abertura de portas nem autorização de uso de VPN.

## 1. Demandas independentes

### A. Servidor físico do LAPEA — diagnóstico atual

O servidor físico é destinado a projetos internos do laboratório. Foram relatadas dificuldades de acesso entre segmentos de rede e falhas intermitentes de conectividade Tailscale, incluindo mensagens como `connection reset by peer`. Há relatos de comportamento diferente conforme a rede utilizada.

**Não se conclui**, sem testes e análise da TI, que exista bloqueio deliberado de VPN, erro específico de firewall ou problema em uma VLAN determinada.

Pedido futuro ao professor Rodrigo Ronner Tertulino da Silva / TI: diagnóstico da conectividade e definição de acesso remoto autorizado, incluindo a possibilidade de manutenção ou substituição da Tailscale por solução institucional adequada.

### B. VM no servidor Xeon — acesso administrativo inicial

A primeira solicitação deve priorizar a criação da VM e um método de SSH seguro aprovado pela TI. A viabilidade de VPN será mencionada como **opção de avaliação**, não como condição para provisionamento.

A equipe conhece Tailscale e políticas de controle de acesso, mas a eventual adoção depende de autorização institucional. Fortinet/FortiVPN é uma referência observada na UERN, **não** uma tecnologia declarada como existente ou homologada no IFRN.

### C. VM — publicação futura

Quando houver aplicações validadas, abrir demanda específica para avaliação de:

- Quais redes e segmentos institucionais podem acessar os projetos.
- Fluxos mínimos necessários até o serviço HTTPS (tipicamente TCP 443), sem presumir liberação universal.
- DNS institucional e estratégia de certificados TLS.
- Isolamento da administração (SSH/painel) em relação ao acesso de usuários finais.
- Monitoramento, registros, responsabilidade operacional e regras de resposta a incidentes.

**Público pretendido:** comunidade do Campus Mossoró, apenas por redes institucionais autorizadas. Eduroam não implica, por si só, autorização de acesso a todos os segmentos internos.

## 2. Divisão acadêmica proposta

- **Rodrigo Ronner Tertulino da Silva:** articulação de redes, VPN, roteamento, DNS e fluxos.
- **Rafael Castro de Souza:** justificativa de aplicações e requisitos de publicação.
- **TI:** decisão técnica e autorização sobre rede, endereçamento, segurança e meios de acesso.

## 3. Segurança mínima

Acesso remoto não deve contornar segmentação institucional. Identidades individuais, revogação, mínimo privilégio, logs e autorização formal continuam necessários com ou sem VPN. Políticas Tailscale SSH não eliminam a necessidade de gestão dos usuários e privilégios sudo na VM.

A documentação pública não deve incluir chaves privadas, tokens, senhas, endereços operacionais sensíveis nem diagramas que revelem detalhes restritos da infraestrutura.
