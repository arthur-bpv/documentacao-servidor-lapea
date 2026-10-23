# Infraestrutura educacional do LAPEA — IFRN Campus Mossoró

Documentação técnica e propostas para avaliação da TI e acompanhamento por professores e alunos autorizados. **As solicitações descritas aqui não representam aprovação institucional ou implantação concluída.**

## Dois ambientes, duas finalidades

- **Servidor físico do LAPEA:** ambiente do laboratório destinado a projetos e experimentos internos. Seu inventário e os registros de conectividade constam dos documentos históricos abaixo. Questões de acesso entre redes e Tailscale ainda dependem de diagnóstico.
- **VM institucional no servidor Xeon da TI (proposta):** ambiente a ser solicitado para aprendizagem de Linux, SSH e hospedagem gradual de projetos. O objetivo futuro é atender a comunidade do Campus Mossoró **somente nas redes institucionais autorizadas**, após avaliação e liberações específicas. A VM ainda não foi provisionada.

## Próximos passos

1. Submeter à TI, após revisão do professor Rafael Castro de Souza, a solicitação inicial de VM Linux com acesso administrativo individual e sudo para responsáveis autorizados.
2. Aprender administração Linux e implantação manual de uma aplicação simples, com controles de segurança definidos pela TI.
3. Avaliar Docker, proxy reverso e Coolify de forma incremental, com alunos limitados aos próprios projetos.
4. Solicitar separadamente a avaliação dos fluxos de rede, DNS e HTTPS para publicação institucional.

A VPN é uma **possibilidade a avaliar** desde o primeiro chamado, sem condicionar a criação da VM. Tailscale já é conhecida pela equipe; Fortinet/FortiVPN é referência externa observada na UERN, não solução presumidamente homologada no IFRN.

## Documentação atual provisória

- [Servidor físico LAPEA — estado e objetivos atuais](docs/servidor-fisico-lapea.md)

## Documentos de planejamento novos

- [Plano de evolução da VM institucional no servidor Xeon](docs/vm-institucional/plano-evolucao.md)
- [Minuta do primeiro chamado para criação da VM](docs/solicitacoes/chamado-vm-xeon.md)
- [Planejamento de rede e VPN — duas demandas distintas](docs/solicitacoes/plano-rede-vpn.md)

## Arquivo histórico — proposta anterior (07/10/2026)

**ARQUIVADO:** os documentos abaixo foram preservados em seus caminhos originais para manter links e rastreabilidade, mas receberam aviso explícito de arquivamento. Refletem a proposta antiga de acesso comunitário ao servidor físico e **não devem ser usados como orientação vigente ou como chamado para envio**. A documentação atual é provisória e está nos links acima.

- [Proposta técnica original](docs/proposta-tecnica.md)
- [Inventário e modelos conceituais](docs/infraestrutura.md)
- [Projetos e serviços levantados](docs/projetos-e-servicos.md)
- [Operação prevista e pendências](docs/operacao.md)
- [Minuta anterior de solicitação à TI](docs/solicitacao-ti.md)

## Responsabilidades acadêmicas propostas

- **Professor Rafael Castro de Souza:** articulação da solicitação da VM e acompanhamento das aplicações.
- **Professor Rodrigo Ronner Tertulino da Silva:** articulação das questões de rede, VPN e conectividade.
- **TI:** definição de provisionamento, redes, regras institucionais e condições de segurança.

Os nomes completos foram informados pelo proponente; funções formais, anuência e contatos institucionais ainda deverão ser confirmados antes de protocolar solicitações.

**Segurança documental:** não publicar credenciais, tokens, chaves privadas ou detalhes operacionais restritos. A documentação não substitui análise e autorização institucional.
