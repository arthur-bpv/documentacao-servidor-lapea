# Solicitação de avaliação à TI

**Estado:** minuta pronta para revisão pelo responsável institucional e inclusão em chamado. Não enviada; sem aprovação registrada.

**Assunto sugerido:** Avaliação de conectividade, endereço gerenciado e DNS interno para servidor educacional do LAPEA — Campus Mossoró

À equipe de TI de Natal, em articulação com a TI do Campus Mossoró,

Solicitamos avaliação de viabilidade para disponibilizar, na rede institucional autorizada do campus, serviços educacionais hospedados no servidor do laboratório provisoriamente identificado como LAPEA. O responsável institucional indicado é o professor Ronner; nome completo, denominação oficial do cargo, contato e nome oficial do laboratório serão confirmados antes do encaminhamento.

O equipamento serve de ambiente compartilhado para testes, aulas, demonstrações e projetos. Os usos incluem sites do NEABI e NUARTE em testes, uma aplicação Laravel para atividades de banco de dados, proposta de cálculos químicos, prática didática de FTP e estudos de multiplayer em jogo educacional. Os estados de implantação variam e estão registrados no [catálogo](projetos-e-servicos.md).

Segundo o proponente, o servidor foi retirado da conexão identificada como Eduroam após dificuldades de autenticação por matrícula e senha e interrupções de internet. A causa técnica e o mecanismo de autenticação não foram diagnosticados. A alternativa em outra VLAN oferece internet, mas usuários da Eduroam não alcançam o equipamento. Atualmente, uma conexão provisória permite acesso por Tailscale. Houve teste anterior bem-sucedido da aplicação Laravel a partir de diferentes laboratórios pela Eduroam; esse acesso não está disponível na configuração atual.

Solicitamos avaliar e definir:

1. **Conectividade estável:** solução institucional adequada a servidor, sem dependência de autenticação pessoal interativa recorrente. Uma exceção de autenticação foi cogitada pelo proponente, mas solução equivalente definida pela TI é aceita.
2. **Rede e comunicação controlada:** permitir que usuários da Eduroam e outras redes expressamente autorizadas alcancem os serviços educacionais nas portas necessárias. A TI poderá escolher rede de servidores, comunicação controlada entre VLANs ou alternativa compatível; não se exige a mesma VLAN dos usuários nem liberação ampla entre redes.
3. **Endereço IP estável e gerenciado:** reserva DHCP ou endereço estático formalmente coordenado com o plano institucional, conforme decisão da TI.
4. **DNS institucional interno:** nome amigável resolvível pelas estações autorizadas, em domínio e convenção escolhidos pela TI. Nome e domínio ainda não estão definidos. Não se solicita DNS público; resolução pela VPN fora do campus será tratada separadamente.
5. **Fluxos e controles:** acesso comunitário somente a serviços publicados; SSH, terminal e painéis administrativos restritos a pessoas autorizadas por VPN. A lista efetiva de portas e protocolos será completada por serviço com os responsáveis, incluindo as particularidades de FTP e multiplayer. Não se solicita abertura de todas as portas.
6. **Condições de uso da Tailscale:** avaliar compatibilidade com políticas institucionais e conectividade necessária ao acesso privado de professores e alunos autorizados, inclusive fora do campus. Pode haver conexão direta ou retransmissão; não se pressupõe peer-to-peer permanente. Participação na VPN não concede sudo.

Não se solicita exposição geral na internet pública, proxy de navegação ou saída alternativa para internet. Firewall e controles de acesso são medidas pretendidas, ainda sem implementação e validação comprovadas. Os responsáveis deverão verificar especialmente a exposição de portas publicadas por Docker.

O equipamento informado é uma plataforma desktop com Intel Core i5-3570, quatro núcleos e quatro threads, aproximadamente 15 GiB de RAM utilizável e disco de 250 GB comerciais. Ubuntu 26.04.1 LTS e kernel Linux 7.0.0-38-generic foram transcritos do inventário fornecido em 07/10/2026, sem verificação direta nesta elaboração. O [inventário completo](infraestrutura.md) preserva a origem e os limites dos dados.

Segundo o proponente, DNS e DHCP são administrados em Natal e a TI local não pode efetuar diretamente as alterações necessárias. Solicitamos análise conjunta para definir solução, condições de implantação, informações adicionais e responsáveis pela validação. A proposta é complementar à hospedagem oficial dos sites e não pede alteração desse ambiente ou dos fluxos de publicação existentes.

## Informações a completar antes do envio

| Campo | Valor |
| --- | --- |
| Solicitante e contato institucional | A preencher pelo campus |
| Responsável institucional e cargo oficial | Professor Rone; nome completo, cargo e contato a confirmar |
| Denominação oficial do laboratório | LAPEA, provisório; a confirmar |
| Localização física para atendimento | A preencher em canal restrito |
| Identificação e interface de rede do equipamento | Anexo restrito a preencher |
| Situação da conexão provisória e evidências das interrupções | Anexo restrito, a levantar com TI local |
| Serviço inicial para validar acesso | A escolher com os responsáveis |
| Portas, protocolos e origens por serviço | Inventário operacional a completar pelos responsáveis e encaminhar à TI por canal apropriado |
| IP e DNS | A definir pela TI |

## Critérios propostos para validação conjunta

- Conexão estável sem autenticação pessoal interativa recorrente, em período de observação acordado.
- IP gerenciado e resolução DNS interna a partir das redes autorizadas.
- Acesso ao serviço de teste pela Eduroam e demais origens aprovadas.
- Administração acessível pela VPN a identidades autorizadas e bloqueada nas origens comunitárias.
- Portas Docker verificadas e somente fluxos acordados acessíveis.
- Resultado, limitações e pendências registrados com a TI e os responsáveis.

A confirmação de informações complementares pode ocorrer durante a análise; as pendências não pressupõem aprovação nem substituem o levantamento técnico. Este texto deve ser revisado pelo responsável institucional antes de encaminhamento. Nenhum chamado foi aberto nesta tarefa.
