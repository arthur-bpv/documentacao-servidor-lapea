# Proposta técnica

## Finalidade e justificativa

O LAPEA pretende oferecer um ambiente para alunos e professores hospedarem, testarem e demonstrarem projetos integradores, serviços e ideias. Outras pessoas poderão experimentar as funcionalidades durante aulas, demonstrações e avaliações, sem nova contratação de nuvem ou implantação central para cada experimento.

O ambiente Linux apoia práticas de administração de sistemas, aplicações, contêineres, bancos de dados e comunicação cliente-servidor. Segundo o proponente, a maioria das estações do campus utiliza Windows. Centralizar ambientes de execução pode reduzir instalações repetidas de dependências, XAMPP e máquinas virtuais nas estações, complementando as ferramentas disponíveis; Windows também atende ao desenvolvimento e Linux não é requisito universal dos projetos.

A plataforma desktop é um ponto de partida. Uso observado e demanda futura poderão fundamentar ampliação de memória, processamento ou infraestrutura, conforme viabilidade institucional. Não há aquisição aprovada nem capacidade de usuários simultâneos demonstrada.

## Problema atual, conforme relato

O campus utiliza diferentes VLANs. O laboratório tem acesso a uma rede associada à Eduroam e a outra VLAN descrita como mais permissiva, vinculada a um roteador do laboratório. Os identificadores, sub-redes, roteamento e filtros não foram fornecidos. A associação exata entre SSID, autenticação, rede cabeada e VLAN depende de confirmação pela TI.

O servidor já esteve na conexão identificada como Eduroam. Autenticação por matrícula e senha e perdas frequentes de internet motivaram sua retirada. Não foi diagnosticado o mecanismo de autenticação nem a causa das interrupções. Na alternativa em outra VLAN, o proponente observa internet disponível, mas ausência de acesso ao servidor pelos usuários da Eduroam. A conexão atual é provisória e permite Tailscale; sua topologia não foi detalhada.

**Experiência anterior:** a aplicação do pacote Laravel foi acessada com sucesso em diferentes laboratórios pela Eduroam, segundo o proponente. Esse teste demonstra uma experiência relatada, não funcionamento na configuração atual.

## Requisitos para avaliação da TI

| Requisito | Resultado necessário | Decisão de implementação |
| --- | --- | --- |
| Conectividade estável | Equipamento conectado sem autenticação interativa pessoal recorrente | TI avalia solução para servidor, exceção de autenticação ou alternativa equivalente |
| Comunicação controlada | Eduroam e outras redes expressamente autorizadas alcançam somente serviços publicados | TI define rede e fluxos entre redes; não é obrigatório usar a VLAN dos usuários |
| Endereço gerenciado | Endereço estável, sem conflitos | Reserva DHCP ou estático coordenado com o plano institucional |
| DNS interno | Nome amigável resolvível pelas estações autorizadas | TI define nome e domínio; não há reserva confirmada |
| Administração privada | SSH, terminal e painéis restritos acessíveis somente por VPN autorizada | Responsáveis e TI validam permissões e exposição efetiva |
| Uso de Tailscale | Acesso remoto privado conforme políticas institucionais | TI avalia condições e conectividade de saída, conforme [infraestrutura](infraestrutura.md) |

Não se pede liberação indiscriminada entre VLANs nem de todas as portas. Portas e protocolos dependem do inventário por serviço e da decisão da TI. Não se solicita DNS público, publicação WAN, proxy de navegação ou saída alternativa para contornar políticas institucionais. O nome interno não necessariamente resolverá pela VPN fora do campus.

## Responsabilidades propostas

| Parte | Responsabilidade a validar |
| --- | --- |
| Responsável institucional | Revisar solicitação, autorizar administradores e projetos, definir substituto e contatos |
| Professores e alunos autorizados | Inventariar serviços, implantar controles aprovados, manter atualizações, backups e registros de operação |
| TI do campus | Articular levantamento físico e diagnóstico local com Natal |
| TI de Natal | Avaliar viabilidade, rede, endereçamento, DNS, fluxos e condições para VPN conforme suas atribuições |
| Responsável de cada projeto | Informar finalidade, portas, dependências, persistência e critérios de validação |

Segundo o proponente, DNS e DHCP institucionais são administrados em Natal e a TI local não possui permissão para as alterações necessárias. A distribuição oficial das atribuições deve ser confirmada. Hospedar ou usar um serviço não concede acesso administrativo ao sistema operacional; participação na VPN não concede sudo automaticamente.

## Validação após eventual implementação

A TI e os responsáveis devem registrar: resolução DNS e acesso ao serviço de teste pela Eduroam e redes autorizadas; bloqueio de SSH e painéis restritos nessas origens; acesso administrativo por identidade VPN autorizada; rejeição de identidades não autorizadas; exposição real das portas Docker; estabilidade da conexão no período de observação acordado. Não foram executados esses testes nesta elaboração. Pendências e responsáveis estão em [operação](operacao.md).
