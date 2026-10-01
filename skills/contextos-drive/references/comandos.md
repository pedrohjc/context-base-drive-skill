# Fluxos de uso

## init

Objetivo: vincular a base pessoal e verificar acesso. Não significa começar a salvar toda a conversa.

1. Reutilize a pasta já indicada pelo usuário na sessão ou configuração. Se faltar, pergunte se existe uma base e solicite o link da pasta própria ou o destino para uma nova base.
2. Verifique conexão, leitura e ferramentas de escrita sem gravar conteúdo de teste.
3. Para base existente, leia INSTRUCOES e INDEX e preserve a estrutura. Para base nova, consulte configuracao.md. `/init` isolado autoriza iniciar a configuração, não criar documentos. Um pedido como `/init criar nova base nesta pasta: LINK` autoriza a estrutura inicial no destino indicado.
4. Entregue link verificado da base, capacidades verificadas e orientação personalizada para futuras conversas. Configuração é específica de cada assistente; não afirme persistência sem suporte do ambiente.

## busca ASSUNTO

Objetivo: recuperar contexto relevante, sem modificar a base.

Use o assunto escrito no pedido. Se omitido e a conversa deixar o tema claro, use esse tema; caso contrário, pergunte o que buscar. Consulte índice e documentos pertinentes, inclusive assuntos relacionados quando necessários. Responda com resumo útil, links dos documentos efetivamente lidos, datas relevantes e lacunas materiais. Não reproduza informações sem relação com a pergunta. Busca vazia não autoriza criar entrada nem contexto.

## salvar ASSUNTO

Objetivo: gravar ou atualizar o contexto do tema indicado. Esse pedido é autorização explícita para a gravação desse tema e a atualização da sua entrada no INDEX.

Use o tema indicado ou, quando inequívoco, o tema atual da conversa. Se houver vários assuntos e o pedido não delimitar qual salvar, peça a delimitação antes de gravar. Não inclua toda a conversa automaticamente. Releia o documento existente, preserve conteúdo útil, incorpore decisões atuais e cumpra o fluxo de gravação em SKILL.md. Não peça confirmação adicional para uma atualização já autorizada e com destino claro. Respeite as confirmações exigidas pelo produto.

Ao terminar, informe o documento e a atualização do índice. Sem escrita disponível, entregue texto para salvar manualmente e deixe claro que o Drive não foi alterado.

## ajuda

Mostre os três fluxos principais, exemplos curtos e o estado conhecido da configuração. Não acesse o Drive apenas para mostrar ajuda e não afirme conexão atual sem verificar.

## Exemplos

`contextos-drive init minha base fica nesta pasta: LINK`

`contextos-drive init criar nova base nesta pasta do meu Drive: LINK`

`contextos-drive busca planejamento de carreira`

`contextos-drive salvar decisões do projeto atual`

`contextos-drive ajuda`
