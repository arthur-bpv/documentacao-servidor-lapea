# Servidor físico do LAPEA — situação provisória atual

**Estado:** documentação de planejamento, baseada em relatos e inventário histórico; pendente de verificação presencial e validação pela TI.  
**Finalidade atual:** atividades e projetos internos do laboratório, **não** publicação de aplicações para todo o campus.

## Equipamento e software

Conforme levantamento anterior (07/10/2026), o equipamento é um **HP Compaq Elite 8300 SFF**, com **Intel Core i5-3570**, aproximadamente **15 GiB de RAM utilizável**, disco de **250 GB comerciais** e Ubuntu Server. Docker e Tailscale foram relatados como ferramentas utilizadas. Versões, estado dos serviços e armazenamento livre exigem nova coleta. Consultar o [inventário histórico arquivado](infraestrutura.md) para a origem dos dados.

## Rede: problema ainda em diagnóstico

O equipamento utiliza uma conexão de laboratório em segmento diferente daquele acessado por parte das estações, com relatos de falta de comunicação entre VLANs. O acesso via Tailscale apresentou falhas intermitentes, incluindo `connection reset by peer`, com comportamento variável conforme a rede de origem. Esses sintomas **não identificam por si só** a causa.

A demanda atual é obter **diagnóstico e orientação de acesso administrativo seguro e autorizado**, em articulação com a TI e o professor **Rodrigo Ronner Tertulino da Silva**. Não há pedido atual para abrir o servidor físico à comunidade do campus, liberar tráfego indiscriminado entre VLANs ou contornar restrições institucionais.

## Uso e operação

- Manter experimentos e projetos de interesse interno do LAPEA.
- Confirmar inventário, serviços efetivamente ativos, versões, contas autorizadas e condições de acesso.
- Definir rotinas mínimas de atualização, cópia de segurança e recuperação.
- Registrar resultados de testes de conectividade com a TI sem publicar credenciais, endereços sensíveis ou regras internas.

O [catálogo histórico de projetos](projetos-e-servicos.md) contém exemplos levantados anteriormente, **não** uma lista validada de serviços ativos. A futura [VM institucional](vm-institucional/plano-evolucao.md) é uma iniciativa independente e será o ambiente proposto para a eventual oferta acadêmica ao campus.
