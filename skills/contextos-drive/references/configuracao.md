# Configuração da base pessoal

## Guia simples conduzido pela IA

Quando o usuário pedir para começar, instalar ou configurar, conduza o passo a passo no chat. Dê uma etapa curta por vez, em linguagem comum, com a ação concreta e o resultado esperado. Aguarde o resultado quando a etapa depender de uma ação da pessoa. Pule o que já estiver resolvido e execute você mesmo as operações disponíveis e autorizadas. Não despeje o manual inteiro nem peça confirmação repetida de ações já autorizadas.

1. Identifique qual produto a pessoa está usando se isso ainda não estiver claro. Para instruções de menus, consulte documentação oficial atual quando possível; não invente botões nem presuma que a interface de outra plataforma é igual.
2. Verifique se há acesso ao Drive. Se faltar conexão, explique como conectar a própria conta no produto utilizado, com instrução curta, e espere a pessoa concluir. Nunca peça credenciais no chat.
3. Pergunte se ela já tem uma pasta para a base. Se tiver, solicite o link. Se não tiver e não houver ferramenta autorizada de criação, oriente: “No seu Google Drive, crie uma pasta chamada Contexts. Abra a pasta, copie o endereço e cole aqui.” Criar a pasta manualmente não é autorização para gravar documentos nela.
4. Leia a pasta indicada e determine se há base existente. Se estiver vazia e ainda não houver autorização, explique o resultado concreto e peça uma única autorização: “Posso criar nesta pasta os dois documentos iniciais, INSTRUCOES e INDEX?” Um pedido anterior para criar a base dispensa repetir essa pergunta.
5. Crie ou oriente a criação dos documentos conforme as capacidades verificadas. Na alternativa manual, apresente um documento por vez com o texto pronto e uma instrução simples de onde colocá-lo. Verifique leitura quando disponível; quando não puder verificar, diga isso.
6. Entregue a orientação personalizada já preenchida para futuras conversas e explique onde colocá-la no produto utilizado. Não afirme persistência automática.
7. Termine mostrando dois exemplos curtos: um pedido de busca e um de gravação explícita. Ofereça orientação caso a pessoa encontre dificuldade, sem criar contexto de demonstração por iniciativa própria.

Se a skill ainda não estiver instalada, ajude a pessoa com a instalação disponível na conta antes de configurar o Drive. Quando skills não estiverem disponíveis, explique a alternativa de instruções em projeto ou configurações sem alegar instalação nativa.

## Base existente

Peça o link da pasta do próprio usuário se ele ainda não o forneceu. Verifique acesso com o conector autenticado, leia as instruções e o índice e preserve a organização. Não substitua documentos existentes por modelos. Se houver índices ambíguos, resolva pelo conteúdo e atualização ou faça uma pergunta curta.

## Base nova

O pedido “configure uma nova base no meu Drive” autoriza criar a estrutura mínima dentro do destino indicado. Apenas instalar ou ativar a skill não autoriza criação.

Se não houver destino, pergunte onde criar. Com destino e autorização, crie uma pasta Contexts se necessário, INSTRUCOES e INDEX usando os modelos. O índice começa vazio; não crie exemplos como contextos reais nem importe dados pessoais da conversa sem pedido. Prefira Google Docs quando ambos os ambientes conseguirem lê-los; preserve Markdown quando for a escolha do usuário.

Verifique documentos e links. Quando não houver ferramentas de escrita, forneça os dois textos e explique como criar os documentos manualmente. Não anuncie configuração concluída até verificar leitura.

## Continuidade entre assistentes

Entregue uma orientação personalizada com o link verificado da pasta para o usuário colocar nas configurações de cada assistente:

“Minha base de contextos fica em [LINK DA MINHA PASTA]. Quando houver acesso ao meu Google Drive, consulte INSTRUCOES e INDEX no início de cada conversa e leia os contextos relevantes para meu pedido. Ao mudar de assunto, consulte outros contextos conforme necessário. Só salve ou atualize contextos quando eu pedir explicitamente. Se não houver acesso, avise brevemente. Use a skill contextos-drive quando disponível.”

Substitua o campo pelo link real antes de entregar o texto. Não altere configurações pessoais automaticamente. Sem um local persistente para a configuração, peça ao usuário que guarde essa orientação nas configurações do produto; não afirme lembrar a pasta em futuras conversas.

Cada assistente exige sua própria conexão autorizada com a conta do usuário. Conectar o Drive em um produto não o conecta no outro. Verifique leitura e escrita separadamente. O método funciona com consulta em ambos e gravação manual quando escrita não estiver disponível.

## Verificação prática

Teste leitura do índice e recuperação de um contexto pertinente. Para testar gravação, use um contexto descartável somente mediante pedido explícito e verifique o resultado. Em uma nova conversa no outro assistente, peça que consulte esse contexto. Não exclua o teste sem autorização. Registre limitações na resposta, não na base, salvo pedido de gravação.
