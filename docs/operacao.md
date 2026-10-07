# Operação e continuidade

## O que está informado e o que está previsto

**Relato atual:** Ubuntu Server, Docker, Tailscale, código vinculado ao GitHub e conexão provisória para acesso privado. **Evidência de arquivos:** documentos dos projetos e processos de publicação foram lidos; o [catálogo](projetos-e-servicos.md) apresenta somente finalidades e situações. Não foi conferido o estado dos serviços em execução.

**Medidas planejadas:** firewall, separação entre serviços comunitários e administração privada, contas com privilégios conforme necessidade. Implantação, eficácia e regras existentes ainda não foram demonstradas. Backup, restauração, atualizações e monitoramento não têm rotina confirmada.

## Procedimentos propostos, sujeitos à definição institucional

1. Registrar professor responsável, substituto, responsáveis técnicos e autorização explícita de cada aluno administrador. Definir contas individuais, privilégios de sudo por necessidade, autorização na Tailscale, revisão periódica e revogação no encerramento da participação.
2. Inventariar cada serviço antes de admiti-lo: finalidade, responsável, código, dependências, portas, contêineres, armazenamento, dados e exposição administrativa. Hospedagem de projeto não concede conta administrativa no host.
3. Validar regras da VPN, firewall do host e portas Docker a partir de origens permitidas e não permitidas. Conferir também interfaces administrativas embutidas nos sites e bancos, sem presumir que login ou Docker, isoladamente, bastem.
4. Definir backup de bancos, arquivos enviados, volumes e configurações necessárias à recuperação; destino separado, acesso, retenção, frequência e objetivos de perda de dados e tempo de recuperação a acordar. Código no GitHub não substitui backup de dados. Guardar segredos somente em armazenamento restrito apropriado.
5. Planejar restauração de teste, registrar resultado, data e responsável. A existência de backup só poderá ser afirmada após confirmação de execução e recuperabilidade.
6. Definir rotina de atualizações do sistema, imagens e aplicações, janelas de manutenção, validação e retorno à versão anterior. Não há automação de atualização ou deploy local confirmada.
7. Acompanhar uso de CPU, RAM, disco e disponibilidade com ferramentas a escolher. Estabelecer critérios de admissão de novos projetos e ampliação com base em uso medido, sem prometer capacidade simultânea.
8. Documentar energia, cabeamento, ventilação, acesso físico e procedimento de retorno após interrupção. Confirmar proteção elétrica e eventual nobreak.

Esses procedimentos são propostas documentais; nenhum foi executado nesta tarefa.

## Pendências para completar a documentação

| Pendência | Encaminhamento sugerido | Estado / resultado |
| --- | --- | --- |
| Denominação oficial e grafia LAPEA | Responsável institucional | A confirmar |
| Nome completo, cargo, contato e substituto do professor Ronner | Laboratório / gestão do campus | A confirmar |
| Repositório desta documentação e URLs dos projetos | Responsáveis acadêmicos / projetos | Repositório da documentação definido no README; URLs dos projetos a confirmar |
| Inventário físico, versões e eventuais divergências | Administradores autorizados | A confirmar com novo registro datado |
| Interface e identificação do equipamento para cadastro | Laboratório com TI local, em anexo restrito | A preencher |
| Topologia, conexão cabeada definitiva, VLANs, sub-redes e filtros | TI local e Natal | A confirmar |
| Autenticação e causa das interrupções | TI local e Natal | Diagnóstico pendente |
| IP gerenciado e nome DNS interno | TI competente | A definir |
| Contêineres reais, serviços, portas, protocolos e dependências | Responsável de cada projeto e administradores | Inventário restrito de execução pendente |
| Volumes, dados persistentes e dependências externas | Responsáveis técnicos | A confirmar |
| Autorização, revisão e revogação de VPN, contas e sudo | Professores responsáveis e TI | Política a definir |
| Firewall implantado e exposição efetiva Docker | Administradores com TI | Validação pendente |
| Backup, destino, frequência, retenção e restauração | Responsáveis técnicos e institucionais | Rotina não confirmada |
| Atualizações e acompanhamento de disponibilidade | Responsáveis técnicos | Rotina a definir |
| Energia, proteção elétrica, nobreak e condições físicas | Laboratório / TI local | A confirmar |
| Carga esperada e admissão de novos projetos | Responsáveis acadêmicos e técnicos | Definir com base em uso observado |
| Destino e execuções dos workflows; diferença no NUARTE | Responsáveis dos sites | Confirmar sem divulgar secrets |

## Registro de manutenção e revisão

| Data | Responsável | Serviço / documento | Ação ou evidência | Resultado e próxima pendência |
| --- | --- | --- | --- | --- |
| 07/10/2026 | Elaboração documental a partir do contexto | Documentação do servidor | Leitura do relato e arquivos locais; consulta de fontes oficiais | Versão inicial; sem auditoria ou alteração operacional |
| A preencher | A preencher | A preencher | A preencher em canal apropriado | A preencher |

Anexos de cadastro, registros de diagnóstico e listas de identidades autorizadas devem ter acesso restrito. Não publicar credenciais, tokens, chaves, valores de secrets, dados pessoais desnecessários ou detalhes sensíveis de rede. Atualizar a documentação pública com resultados necessários à compreensão, sem copiar anexos operacionais.
