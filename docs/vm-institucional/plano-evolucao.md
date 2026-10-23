# VM institucional no servidor Xeon — plano de evolução

**Estado:** proposta de planejamento, sem provisionamento ou aprovação formal registrados.  
**Instituição:** IFRN — Campus Mossoró; LAPEA.  
**Infraestrutura pretendida:** máquina virtual hospedada em servidor físico Xeon sob gestão da TI. A configuração exata do equipamento, o hipervisor e a disponibilidade de recursos dependem de confirmação da TI. **Xeon não é o nome de um servidor chamado “Zion”.**

## 1. Contexto e separação de ambientes

Existem dois ambientes com finalidades diferentes:

1. **Servidor físico do LAPEA:** equipamento do laboratório para experimentação e projetos internos. Sua conectividade entre segmentos institucionais e o acesso remoto por Tailscale apresentam questões ainda não diagnosticadas conclusivamente; serão tratados em solicitação específica de redes.
2. **VM institucional no servidor Xeon da TI:** ambiente pretendido para aprendizado de administração Linux e hospedagem gradual de aplicações acadêmicas. A longo prazo, poderá atender a comunidade do Campus Mossoró **somente nas redes institucionais autorizadas**, nunca por pressuposição de exposição à internet pública.

Não se deve descrever a VM como existente ou os projetos futuros como implantados.

## 2. Responsáveis propostos

- **Professor Rafael (programação):** interlocução acadêmica sobre a VM, projetos, desenvolvimento e, futuramente, contêineres e implantação.
- **Professor Rodrigo Ronner (redes):** interlocução acadêmica sobre acesso administrativo, conectividade, VPN, DNS e fluxos institucionais.
- **TI do campus e demais instâncias competentes:** provisionamento, infraestrutura, políticas de rede e condições de segurança conforme atribuições institucionais.
- **Equipe autorizada do LAPEA:** administração do sistema operacional com sudo, conforme entendimento preliminar relatado pelo proponente, ainda sujeito à formalização de contas, responsáveis e limites de atuação.

Os professores e alunos não precisam dominar antecipadamente as tecnologias propostas; capacitação e documentação fazem parte do projeto. Cargos, anuência e responsabilidades oficiais serão confirmados antes de protocolar solicitações.

## 3. Evolução incremental

| Fase | Objetivo | Entregável / critério de avanço |
| --- | --- | --- |
| 1 — Provisionamento | Obter VM Linux e acesso administrativo aprovado | VM criada, contas individuais, SSH funcional, sudo conforme autorizado, regras básicas de manutenção e recuperação acordadas |
| 2 — Fundamentos | Aprender Linux, SSH, permissões, serviços, logs, Docker e Compose | Aplicação simples de teste acessível apenas à equipe/rede de testes autorizada; documentação reproduzível |
| 3 — Automação | Avaliar Coolify, integração Git e pipelines | Piloto controlado, revisão das permissões do painel, segredos protegidos e processo de rollback |
| 4 — Oferta institucional | Atender projetos acadêmicos do Campus Mossoró | Avaliação de capacidade, segurança, DNS, HTTPS e regras de comunicação entre redes em chamado posterior |

As fases não têm prazos fixados. Segurança, backups e gestão de acessos não devem ser adiados se a TI os exigir desde o provisionamento.

## 4. Requisitos iniciais a negociar

- Linux Server LTS ou distribuição aprovada pela TI.
- Dimensionamento **indicativo**: 2 vCPU, 4 GiB RAM, 40 GiB de armazenamento, sujeito à disponibilidade e revisão.
- IP privado gerenciado e conectividade suficiente para atualizações autorizadas.
- Acesso SSH individual, preferencialmente por chaves, com privilégios sudo apenas para administradores designados.
- Orientação da TI sobre backup/snapshot, restauração, manutenção e tratamento de incidentes.
- Nenhuma abertura de portas de aplicações para toda a comunidade nesta fase.
- Possibilidade de estudar Docker futuramente, após avaliação das regras de virtualização e segurança.

## 5. Acesso remoto e VPN: avaliação, não exigência

A equipe já utiliza Tailscale em outros ambientes e possui experiência prática com políticas de acesso. Solicita-se que a TI **avalie**, sem condicionar a criação da VM, a viabilidade de uma VPN institucional ou de uma solução como Tailscale para administração restrita.

Tailscale SSH e suas políticas podem simplificar o controle de acesso remoto, mas **não substituem** a definição de identidades, usuários Linux, privilégios sudo, revogação e registros. Não se pressupõe que Fortinet/FortiVPN esteja homologada no IFRN; trata-se apenas de referência externa conhecida na infraestrutura da UERN. Nenhuma VPN será instalada ou usada para contornar controles institucionais sem autorização.

Se a VPN não for viável inicialmente, o SSH deve seguir o método aprovado pela TI. A liberação de fluxos para outras VLANs, Eduroam, DNS e HTTPS será objeto de avaliação/chamado próprio.

## 6. Direção técnica futura: Docker e Coolify

A proposta é primeiro aprender a executar e manter uma aplicação manualmente, depois usar contêineres e, somente após isso, experimentar Coolify. A plataforma pode integrar repositórios e automatizar deploys, mas possui permissões sensíveis sobre o host e o mecanismo de contêineres.

**Modelo desejado:** alunos administram somente seus projetos; professores e administradores autorizados gerenciam a plataforma. Os limites reais dos papéis do Coolify devem ser verificados na versão adotada antes de conceder acessos. A escolha do proxy (Traefik gerenciado pelo Coolify, Nginx ou outra solução) também permanece aberta.

## 7. Pendências para validação

- Confirmar recursos disponíveis, hipervisor, sistema operacional e regras de uso da VM.
- Confirmar titulares de contas sudo, política de autenticação e acesso emergencial da TI.
- Definir responsabilidade por backup, retenção, restauração, atualizações e logs.
- Verificar restrições a Docker, contêineres privilegiados e publicação de portas.
- Solicitar avaliação de VPN sem pressupor autorização.
- Em fase futura, identificar redes de origem autorizadas, DNS, certificados TLS, HTTPS e critérios de homologação das aplicações.
- Verificar normas internas de segurança, proteção de dados e uso de rede com a TI; este documento não representa aprovação de conformidade.
