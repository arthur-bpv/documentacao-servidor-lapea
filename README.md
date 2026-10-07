# Servidor educacional do LAPEA — IFRN Campus Mossoró

Documentação técnica para avaliação da TI de Natal, em articulação com a TI do campus, e continuidade por professores e alunos autorizados. Versão inicial: 7 de outubro de 2026. **Proposta em análise, sem aprovação institucional registrada.**
O servidor oferece um ambiente local compartilhado para hospedar, testar e demonstrar projetos e atividades práticas. A prioridade é permitir que a comunidade na rede autorizada do campus acesse serviços educacionais, mantendo a administração privada por Tailscale.

## Situação atual e resultado solicitado

Segundo o proponente, a conexão provisória permite acesso por Tailscale, mas usuários da Eduroam não alcançam os serviços. Um teste anterior com a aplicação Laravel teve sucesso em diferentes laboratórios pela Eduroam; isso não representa a conectividade atual.

Solicita-se à TI avaliar conectividade estável sem autenticação pessoal interativa recorrente, endereço IP gerenciado, DNS interno e comunicação controlada nas portas necessárias. A implementação e a escolha da rede cabem à TI. Não há solicitação de exposição geral na internet pública.

## Documentos

- [Proposta técnica e responsabilidades](docs/proposta-tecnica.md)
- [Inventário e modelos conceituais](docs/infraestrutura.md)
- [Projetos, serviços e acessos](docs/projetos-e-servicos.md)
- [Operação prevista e pendências](docs/operacao.md)
- [Texto para chamado à TI](docs/solicitacao-ti.md)

## Responsáveis e evidências

Responsável institucional indicado: professor Rone, informado pelo proponente como responsável pelo laboratório e diretor de pesquisas do campus. Nome completo, cargo oficial e contato institucional: **a confirmar**. A administração técnica cabe a professores responsáveis e alunos expressamente autorizados.

A base principal é o arquivo `Contexto_Codex_Documentacao_Servidor_LAPEA.md`, fornecido na raiz do workspace. Os dados da imagem de inventário foram transcritos nesse contexto; a imagem original não foi inspecionada nesta elaboração. Foram lidos documentos e configurações versionadas dos projetos locais, sem inspeção do estado de execução do servidor, auditoria de rede ou teste de acesso.

Repositório dedicado à documentação: [arthur-bpv/documentacao-servidor-lapea](https://github.com/arthur-bpv/documentacao-servidor-lapea). Os repositórios dos projetos foram preservados. Credenciais, identificadores de rede e dados operacionais restritos devem permanecer em anexos institucionais, fora de eventual publicação pública.
