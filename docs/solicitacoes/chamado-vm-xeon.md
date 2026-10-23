# Minuta — solicitação de máquina virtual institucional

**Estado:** rascunho para revisão e eventual encaminhamento pelo professor Rafael; não protocolado.  
**Destinatário:** equipe de TI competente do IFRN Campus Mossoró, com eventual articulação com instâncias sistêmicas conforme fluxo institucional.  
**Assunto sugerido:** Solicitação de máquina virtual Linux para atividades acadêmicas do LAPEA

Prezados(as),

Solicitamos a avaliação e, se tecnicamente viável, o provisionamento de uma máquina virtual Linux na infraestrutura institucional mantida pela TI, em servidor físico Xeon, para apoiar atividades acadêmicas de desenvolvimento de software, administração de sistemas e aprendizagem de hospedagem de aplicações no âmbito do LAPEA, Campus Mossoró.

A proposta prevê **implantação gradual**. Inicialmente, o ambiente será utilizado por equipe restrita e autorizada para aprender e praticar acesso SSH, administração básica de Linux, configuração de serviços e execução de aplicações de teste. Em etapas posteriores, conforme capacitação da equipe e autorização da TI, pretende-se estudar contêineres (Docker), automação de implantação (possivelmente Coolify) e disponibilização de projetos acadêmicos à comunidade do campus, exclusivamente nas redes institucionais autorizadas.

Como referência inicial, sugerimos **2 vCPU, 4 GiB de RAM e 80 GiB de armazenamento**, sujeitos à disponibilidade, aos padrões adotados e ao dimensionamento definido pela TI. Solicitamos orientação sobre a distribuição Linux adequada, endereçamento, acesso administrativo e mecanismos institucionais de backup e recuperação.

Conforme diálogo preliminar relatado pela equipe proponente, está prevista a disponibilização de **acesso sudo a administradores autorizados do LAPEA**. Solicitamos formalizar as condições desse acesso, a identificação individual dos responsáveis e as regras de segurança e suporte aplicáveis.

Para a administração remota, solicitamos também **orientação e avaliação de viabilidade**, sem constituir requisito impeditivo ao provisionamento, quanto ao uso de VPN institucional ou de solução como Tailscale, com acesso restrito e autorização expressa da TI. Caso isso não seja viável nesta etapa, seguiremos o procedimento de acesso SSH indicado pela equipe de TI.

**Não solicitamos neste primeiro momento** a abertura geral de serviços web, liberação de comunicação entre VLANs, acesso pela Eduroam, registros DNS ou exposição à internet. Eventuais necessidades de conectividade para aplicações e publicação institucional serão detalhadas em solicitação específica após a consolidação do ambiente de testes.

Como referências acadêmicas para o acompanhamento, propomos o **professor Rafael**, nas questões de desenvolvimento e aplicações, e o **professor Rodrigo Ronner**, nas questões de redes e conectividade, sujeitos à anuência e designação institucional.

Agradecemos a avaliação de viabilidade e as orientações sobre o procedimento de criação da VM, as condições de acesso e as responsabilidades de operação.

Atenciosamente,

**[Nome e identificação do solicitante institucional — preencher]**  
**[Vínculo/setor e contato institucional — preencher]**

---

## Notas internas antes do protocolo

- Confirmar o nome completo, a anuência e o vínculo do professor Rafael.
- Confirmar a designação e os dados oficiais do professor Rodrigo Ronner.
- Confirmar o setor e o canal corretos para o chamado.
- Não afirmar que a VM já foi aprovada ou criada.
- Anexar, se conveniente, o [plano de evolução](../vm-institucional/plano-evolucao.md).
