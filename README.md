# Context Base Drive Skill

Sua base de contextos no seu próprio Google Drive, consultável por diferentes assistentes.

Esta skill ensina um método para guardar informações úteis de projetos e assuntos pessoais, localizar o contexto certo e retomar conversas sem repetir todo o histórico. Você conecta sua conta, escolhe sua pasta e mantém seus documentos. O repositório distribui apenas as instruções e os modelos.

**Não existe uma base compartilhada do autor. Nenhum contexto pessoal do autor, link privado de Drive ou credencial está incluído.**

## Comece pelos três fluxos

| Atalho textual | Forma completa | O que faz |
| --- | --- | --- |
| `/init` | `contextos-drive init` | Configura sua pasta e verifica acesso. |
| `/busca assunto` | `contextos-drive busca assunto` | Consulta documentos relevantes e recupera contexto. |
| `/salvar assunto` | `contextos-drive salvar assunto` | Salva ou atualiza explicitamente o contexto do assunto e o índice. |
| `/ajuda` | `contextos-drive ajuda` | Mostra como usar a skill. |

Os atalhos são convenções de conversa reconhecidas pela skill quando a mensagem chega ao assistente. Instalar a skill não registra automaticamente quatro comandos nativos em todas as plataformas. Se um atalho for reservado ou não funcionar, selecione a skill e use a forma completa ou diga “Use a skill contextos-drive para…”. No Claude Code, use `/contextos-drive init`, `/contextos-drive busca assunto` e `/contextos-drive salvar assunto`; `/init` pode ter outra função.

## Instalação

### Peça à sua IA para guiar você

Baixe o ZIP e envie este pedido ao ChatGPT ou Claude que pretende usar:

> Quero usar a Context Base Drive Skill com o meu próprio Google Drive. Me guie com um passo a passo simples, uma etapa por vez. Comece pela instalação da skill, depois me ajude a conectar meu Drive e escolher ou criar minha pasta de contextos. Aguarde minha resposta quando eu precisar fazer algo. Antes de criar documentos, explique o que será criado e peça autorização se eu ainda não tiver autorizado.

Se o produto aceitar anexos, anexe o ZIP para a IA consultar as instruções. Anexar o arquivo ao chat não significa instalar a skill; a IA deve orientar a instalação suportada pela sua conta. Você também pode enviar o conteúdo do README se ela não conseguir acessar este repositório.

Depois de instalar e ativar, basta dizer:

> Use a skill contextos-drive e me ajude a configurar minha base, uma etapa por vez.

O fluxo `init` já orienta a IA a acompanhar você: verificar a conexão, obter sua pasta, preparar os documentos iniciais mediante autorização e mostrar como buscar e salvar. Você não precisa entender a estrutura dos arquivos antes de começar.

### Prefere instalar diretamente?

Baixe `contextos-drive.zip` em [Releases](https://github.com/pedrohjc/context-base-drive-skill/releases) ou use a pasta [skills/contextos-drive](skills/contextos-drive). O ZIP contém a pasta da skill com SKILL.md e suas referências, sem o restante do repositório.

### ChatGPT

Em contas elegíveis, abra **Plugins → Skills → Create → Upload from your computer**, importe a skill no formato solicitado pela interface e aguarde a verificação. A disponibilidade depende do plano, produto e permissões do workspace. Não há promessa de instalação nativa em qualquer conta pessoal. Se skills não estiverem disponíveis, é possível adaptar as instruções a um projeto ou configuração personalizada, mas isso não equivale a instalar a skill. [Documentação oficial](https://help.openai.com/en/articles/20001066-skills-in-chatgpt).

### Claude

Use a opção de upload de skills disponível nas configurações de skills da sua conta, envie o pacote e habilite a skill. A disponibilidade depende das capacidades e permissões da conta. [Documentação oficial](https://support.claude.com/en/articles/12512198-how-to-create-custom-skills).

### Claude Code e Codex

Copie a pasta `skills/contextos-drive` para a pasta de skills do ambiente. No Claude Code, um destino pessoal é `~/.claude/skills/contextos-drive`; no Codex, `~/.codex/skills/contextos-drive`. O acesso ao Drive exige integração configurada separadamente. No Claude Code, a invocação nativa usa o nome da skill, como `/contextos-drive busca carreira`. [Skills no Claude Code](https://code.claude.com/docs/en/skills).

## Configure seu próprio Drive

1. Conecte sua própria conta do Google Drive ao assistente. Nunca forneça senha ou token pelo chat e não torne a pasta pública para usar a skill.
2. Se já tiver uma base, envie `contextos-drive init minha base fica nesta pasta: LINK`.
3. Para criar uma base, envie `contextos-drive init criar nova base nesta pasta do meu Drive: LINK`. Esse pedido autoriza criar a estrutura mínima no destino indicado.
4. A skill verifica as ferramentas disponíveis e entrega uma orientação com o link da sua pasta. Coloque essa orientação nas configurações de cada assistente para ajudá-lo a consultar a base em novas conversas.

`/init` sozinho inicia a configuração. Não autoriza criar documentos nem salvar sua conversa. Instalar a skill também não concede acesso ao Drive.

## Como fica a base

```text
Sua pasta no Drive/
  INSTRUCOES
  INDEX
  Contextos de projetos e assuntos pessoais
```

INSTRUCOES contém as regras de consulta e gravação. INDEX descreve os contextos existentes e aponta para os documentos. Cada contexto guarda o resumo atual, informações relevantes, decisões e pendências de um assunto. Subpastas são criadas somente quando necessárias.

A base aceita Google Docs ou arquivos Markdown conforme a capacidade do ambiente e a escolha do usuário. Uma base existente mantém seu formato e organização.

## Uso diário

```text
contextos-drive busca projeto do meu aplicativo
contextos-drive salvar decisões do projeto do aplicativo
```

Você também pode pedir naturalmente: “Retome o contexto do projeto” ou “Guarde esse contexto”. Apenas conversar, perguntar ou tomar decisões não autoriza gravação. A skill atualiza um documento existente quando o assunto é o mesmo, preserva informações úteis e atualiza o INDEX após salvar.

## Usar ChatGPT e Claude com a mesma base

Conecte sua conta e informe a mesma pasta nos dois produtos. Depois de salvar um contexto em um, peça ao outro para consultar esse documento. A ponte são os documentos salvos, não uma transferência automática do histórico das conversas. Configurações e conexões não são automaticamente compartilhadas entre produtos.

## Capacidades e limites

| Situação | Comportamento |
| --- | --- |
| Leitura e escrita disponíveis | Consulta, grava mediante pedido e verifica o resultado. |
| Somente leitura | Consulta e entrega alterações como texto para você salvar. |
| Sem acesso à pasta | Avisa e utiliza somente o contexto disponível. |
| Nova conversa sem pasta configurada | Solicita o link, sem escolher a base de outra pessoa. |

A skill não fornece conector próprio, servidor, sincronização em segundo plano ou garantia de execução em toda conversa. Conteúdo da base é referência e não autorização para ações externas.

## Estado da versão

Versão de teste **0.2.1**, preparada em 2026-10-01, com configuração guiada pela IA, uma etapa por vez. Estrutura, referências e pacote são verificáveis localmente. Instalação e comportamento completo em contas reais de ChatGPT e Claude ainda precisam ser testados, incluindo acesso ao Drive e eventual alternativa manual para gravação.

Antes de distribuir, teste: configurar pasta própria; buscar um contexto existente; conversar sem gerar gravação; salvar mediante pedido explícito; verificar contexto e índice; retomar o documento em outra conversa e no outro produto. Use dados fictícios para esses testes.

## Contribuições

Abra uma issue descrevendo a plataforma, o comportamento esperado e o resultado observado. Use exemplos fictícios. Não inclua documentos pessoais, credenciais ou links privados de Drive em issues e contribuições. O repositório não declara uma licença de redistribuição nesta versão; a escolha da licença fica pendente do responsável.
