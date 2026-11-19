# Módulo 4: Atendimento e qualificação com IA no WhatsApp

**Roteiro integral de gravação**
**Curso:** IA no Atendimento Imobiliário · **Professor:** Cleiton Campano · **Direção:** Bruno Pessoa
**Versão:** 19/11/2026 (rascunho para revisão do professor)

## Visão geral do módulo

| Item | Definição |
|---|---|
| Objetivo do módulo | O aluno desenha um agente de atendimento e qualificação de leads com escopo, perguntas, passagem para o corretor e tratamento de exceções, e monta um protótipo para testar esse desenho. |
| Aulas | 4.1 O escopo do agente (≈11 min) · 4.2 Perguntas de qualificação sem interrogatório (≈12 min) · 4.3 Agendamento e passagem para o corretor (≈10 min) · 4.4 Quando a conversa sai do roteiro (≈14 min) · 4.5 Protótipo completo e primeiros testes (≈15 min) |
| Duração total | ≈62 minutos de vídeo |
| Entrega do aluno ao final | Ficha de escopo, roteiro de qualificação, modelo de resumo de passagem, lista de exceções e um protótipo testado em pelo menos 5 conversas |
| Pré-requisito | Módulo 1 (limites da IA) e Módulo 2 (caso piloto escolhido). O Módulo 3 ajuda na escrita das instruções. |

### Sobre o protótipo

O protótipo deste módulo é montado em uma ferramenta de IA conversacional que permita salvar instruções fixas e anexar um arquivo de referência (por exemplo, um "projeto", "assistente personalizado" ou recurso equivalente). O professor faz o papel do lead e conversa com o agente na própria ferramenta.

Ele **não** é ligado ao WhatsApp, não consulta o estoque em tempo real e não grava no CRM. Isso é proposital: primeiro se testa o desenho da conversa, depois se pensa na integração (Módulo 5). Se a ferramenta escolhida para o curso tiver integração com WhatsApp, ela pode aparecer como demonstração extra, deixando claro que não é necessária para acompanhar o módulo. **[VALIDAR: ferramenta usada nas demonstrações]**

### Cenário fictício (continuação do Módulo 1)

- **Imobiliária Horizonte (fictícia):** 8 corretores, venda e locação residencial, cidade fictícia.
- **Horário de atendimento humano (fictício):** segunda a sexta, 9h às 18h; sábado, 9h às 13h.
- **Prazo de retorno combinado pela equipe (fictício):** um corretor responde em até 2 horas dentro do horário de atendimento. Fora do horário, no início do próximo período.
- **Base de imóveis:** 4 imóveis fictícios (Anexo F), incluindo o AP-204 do Módulo 1, agora com a ficha completada pelo corretor.
- Leads fictícios: Mariana (compra), Carlos (compra), Juliana (locação), Roberto (lead irritado).

### Convenções

Iguais às do Módulo 1: **[CÂMERA]**, **[TELA]**, **[GRÁFICO]**, **FALA**, **DIREÇÃO**, **[VALIDAR]**. Gravar sempre a resposta real da ferramenta; as respostas deste roteiro são exemplos para orientar a narração. Registrar ferramenta, versão e data no início de cada demonstração. Selo "SIMULAÇÃO" em todas as telas com conversa.

---

## Aula 4.1: O escopo do agente

| Item | Definição |
|---|---|
| Duração | ≈11 minutos |
| Objetivo | Definir o trabalho do agente antes de escrever qualquer instrução: o que ele faz, o que nunca faz, de onde vêm as informações e quando chama uma pessoa. |
| Resultado para o aluno | Ficha de escopo preenchida para o caso piloto da sua imobiliária. |
| Materiais | Ficha de escopo do agente, modelo em branco e exemplo preenchido (Anexo A) |

### Bloco 1. Problema reconhecível (0:00–1:15)

**[CÂMERA]**

**FALA:**
"Quando uma imobiliária decide colocar um assistente de IA no WhatsApp, a primeira vontade costuma ser: 'ele vai responder tudo'. Dúvida de imóvel, negociação, documentação, boleto de aluguel, reclamação de vizinho. Tudo.

O resultado, quase sempre, é um assistente que responde muita coisa mais ou menos e algumas coisas muito mal. E, pior, ninguém na equipe sabe dizer com clareza o que ele deveria estar fazendo.

Nesta aula, antes de escrever qualquer instrução, a gente vai definir o trabalho do agente. Do mesmo jeito que você faria com uma pessoa nova na equipe."

### Bloco 2. Conceito em uma frase (1:15–2:00)

**[CÂMERA]**

**FALA:**
"A frase desta aula: **um bom agente sabe exatamente o que faz, o que nunca faz e quando chama uma pessoa.**

Pensa num recepcionista no primeiro dia de trabalho. Você não diria 'resolva tudo'. Você diria: 'receba as pessoas, entenda o que elas procuram, anote estes dados, e se alguém quiser negociar valor, chame o corretor'. É isso que a gente vai escrever para o agente."

**DIREÇÃO:** [GRÁFICO] com a frase e três caixas: Faz · Nunca faz · Chama uma pessoa quando.

### Bloco 3. Os campos da ficha de escopo (2:00–5:00)

**[CÂMERA]** com [GRÁFICO] da ficha (Anexo A) aparecendo campo a campo.

**FALA:**
"A ficha de escopo tem oito campos. Vou passar por cada um.

**Um: objetivo.** Uma frase que diz para que o agente existe. Para começar, eu recomendo um objetivo pequeno: fazer o primeiro atendimento de leads de compra e locação, entender o que a pessoa procura e encaminhar para o corretor com um resumo. Só isso já resolve um problema grande, que é o lead esperando horas por uma primeira resposta.

**Dois: público e canal.** Quem fala com ele e por onde. Leads vindos de portais, do site e do WhatsApp da imobiliária, por exemplo.

**Três: o que ele faz.** Uma lista curta de ações. Cumprimentar, se apresentar, entender a necessidade, informar dados que estão na base de imóveis, oferecer visita, registrar preferências de horário, encaminhar.

**Quatro: o que ele nunca faz.** Essa lista é tão importante quanto a anterior. Nunca negocia valor. Nunca promete aprovação de crédito. Nunca confirma horário de visita sem o corretor. Nunca pede documentos, CPF ou renda. Nunca dá orientação jurídica. Nunca inventa informação que não está na base.

**Cinco: fontes de informação.** De onde vêm os fatos que ele pode usar. No nosso protótipo, é uma base de imóveis com data de atualização. Se uma informação não está ali, ele não sabe.

**Seis: quando chama uma pessoa.** Os gatilhos de passagem. O lead pede para falar com alguém. O lead está irritado ou reclamando. O assunto é negociação, crédito, documentação ou contrato. O lead está pronto para agendar visita. Ou o agente simplesmente não sabe responder.

**Sete: tom de voz.** Como a imobiliária fala. Cordial, direto, sem exageros, por exemplo.

**Oito: transparência e dados.** O agente se apresenta como assistente virtual logo no início. E só pede os dados necessários para o atendimento."

**DIREÇÃO:** cada campo entra no gráfico quando é citado. Na parte "nunca faz", o professor pode retomar os exemplos do Módulo 1 (disponibilidade inventada, promessa de crédito).

### Bloco 4. Demonstração: preenchendo a ficha da Imobiliária Horizonte (5:00–8:30)

**[TELA]** Documento com a ficha em branco (Anexo A). Selo "SIMULAÇÃO".

**FALA:**
"Vou preencher a ficha da Imobiliária Horizonte pensando em voz alta. O caso piloto que a gente escolheu no Módulo 2 foi o primeiro contato com leads de portal."

**DIREÇÃO:** o professor preenche campo a campo usando o exemplo do Anexo A como referência, explicando cada decisão. Momentos para reforçar em voz alta:
- Por que o objetivo é pequeno ("se der certo, a gente amplia; se começar grande, fica difícil saber o que deu errado").
- Por que "informar dados da base" vem acompanhado de "dizendo a data da atualização".
- Por que "registrar preferência de horário" e não "agendar visita".
- Por que não pedir renda nem CPF ("o corretor pede, quando for necessário e pelo canal adequado").

**FALA:**
"Ficha preenchida. Agora um teste rápido: vou pedir para a IA criticar esse escopo."

**Instrução (colar na tela):**

> Você é consultor de atendimento imobiliário. Analise a ficha de escopo abaixo, de um assistente virtual de WhatsApp de uma imobiliária. Aponte até 5 situações comuns que a ficha não cobre ou que podem gerar risco para o cliente ou para a imobiliária. Seja específico.
> [colar a ficha preenchida]

**FALA (comentando a resposta real):**
"Vamos ver o que ela levantou. Algumas sugestões fazem sentido e eu vou incorporar. Outras não se aplicam ao nosso caso. A decisão continua sendo nossa."

**DIREÇÃO:** é provável que a IA aponte situações como proprietário querendo anunciar imóvel, inquilino com problema de manutenção, mensagens de áudio ou pedidos fora do horário. Se aparecerem, o professor diz que elas serão tratadas na aula 4.4. Comentar a resposta que aparecer, sem forçar.

### Bloco 5. Leitura crítica (8:30–9:45)

**[CÂMERA]**

**FALA:**
"Três testes para saber se o seu escopo está bom.

Primeiro: cada item de 'o que ele faz' tem uma fonte? Se o agente 'informa o valor do condomínio', esse valor precisa estar em algum lugar que ele consulta.

Segundo: cada item de 'nunca faz' tem uma saída? Se ele não negocia, o que ele diz quando o lead pede desconto? A gente responde isso na aula 4.4.

Terceiro: uma pessoa nova na equipe entenderia o trabalho lendo só essa ficha? Se não entenderia, o agente também não vai entender."

**DIREÇÃO:** [GRÁFICO] com os três testes.

### Bloco 6. Tarefa aplicável (9:45–10:40)

**[CÂMERA]**

**FALA:**
"Sua tarefa: pegue o caso piloto que você escolheu no Módulo 2 e preencha a ficha de escopo para a sua imobiliária. Use o exemplo da Horizonte como referência, mas adapte ao seu horário, aos seus canais e às regras da sua empresa. Depois, faça os três testes que eu acabei de mostrar."

### Bloco 7. Fechamento (10:40–11:00)

**[CÂMERA]**

**FALA:**
"Com o escopo definido, o agente já sabe o que fazer. Na próxima aula, a gente vai ensinar ele a fazer as perguntas certas, sem transformar a conversa num interrogatório."

---

## Aula 4.2: Perguntas de qualificação sem interrogatório

| Item | Definição |
|---|---|
| Duração | ≈12 minutos |
| Objetivo | Definir quais informações o corretor precisa para dar o próximo passo e como obtê-las numa conversa natural, pedindo só o necessário. |
| Resultado para o aluno | Roteiro de qualificação da sua imobiliária e critérios para classificar o lead. |
| Materiais | Roteiro de qualificação de compra e de locação (Anexo B) |

### Bloco 1. Problema reconhecível (0:00–1:15)

**[CÂMERA]**

**FALA:**
"Existem dois jeitos clássicos de errar na qualificação.

O primeiro é o interrogatório. O lead manda 'oi, tenho interesse' e recebe de volta: 'Qual seu nome completo? CPF? Renda? Quer comprar ou alugar? Qual bairro? Quantos quartos? Qual valor?'. Tudo de uma vez. Muita gente simplesmente para de responder.

O segundo é não qualificar nada. O lead chega no corretor só com um 'tenho interesse', e o corretor perde tempo descobrindo que a pessoa procurava outra coisa, em outro bairro, com outro orçamento.

O agente precisa ficar no meio: perguntar o suficiente, do jeito certo."

### Bloco 2. Conceito em uma frase (1:15–1:50)

**[CÂMERA]**

**FALA:**
"A frase desta aula: **qualificar é entender o que a pessoa precisa para dar o próximo passo certo, não preencher um formulário.**"

**DIREÇÃO:** [GRÁFICO] com a frase.

### Bloco 3. O que perguntar e como perguntar (1:50–5:30)

**[CÂMERA]** com [GRÁFICO] de apoio.

**FALA:**
"Comece pelo fim: o que o corretor precisa saber para ligar ou mandar mensagem já com uma proposta de visita que faça sentido? Na Horizonte, a gente chegou a esta lista para compra:

finalidade: morar ou investir;
região de interesse;
tipo de imóvel e número de quartos;
faixa de valor;
forma de pagamento pretendida: à vista, financiamento, uso de FGTS, ainda não sabe;
momento: quando pretende se mudar ou fechar negócio;
e disponibilidade para visita.

Para locação, muda um pouco: data prevista de mudança, valor máximo de aluguel com condomínio, e qual garantia a pessoa pretende usar, como fiador, seguro-fiança ou caução, conforme o que a imobiliária aceita.

Agora, o como. Cinco regras.

**Um: uma pergunta por mensagem.** No máximo duas, se forem curtas e relacionadas. WhatsApp é conversa, não formulário.

**Dois: aproveite o que a pessoa já disse.** Se o lead escreveu 'vi o apartamento de dois quartos no Jardim das Acácias', o agente não pergunta região nem número de quartos de novo.

**Três: ordem natural.** Comece pelo que a pessoa procura, que é o interesse dela. Deixe valor e forma de pagamento para depois, quando a conversa já tem confiança.

**Quatro: diga por que está perguntando, quando for útil.** 'Pra eu te mostrar opções no seu orçamento, qual faixa de valor você tem em mente?' soa muito diferente de 'Qual seu orçamento?'.

**Cinco: peça só o necessário.** Nada de CPF, renda exata, documentos ou endereço residencial nessa etapa. Além de afastar o lead, coletar dado que você não precisa é um risco que a sua empresa não precisa correr. Faixa de valor e forma de pagamento pretendida bastam para o corretor."

**DIREÇÃO:** [GRÁFICO] com a lista de informações de compra e, ao lado, as cinco regras. Destacar a regra 5 com o ícone de alerta de dados usado no Módulo 1.

### Bloco 4. Classificando o lead (5:30–6:30)

**[CÂMERA]** com [GRÁFICO].

**FALA:**
"No fim da qualificação, o agente classifica o lead em uma de três situações, com critérios que a sua imobiliária define. Na Horizonte ficou assim:

**Pronto para visita:** sabe o que procura, a faixa de valor é compatível com algum imóvel da base e quer visitar.
**Em pesquisa:** ainda está comparando, sem prazo definido, ou quer receber opções antes de visitar.
**Sem imóvel compatível:** procura algo que a imobiliária não tem no momento.

Repara que nenhuma dessas categorias é 'lead ruim'. Todas vão para o corretor. O que muda é a prioridade e a abordagem."

**DIREÇÃO:** [GRÁFICO] com as três categorias e uma linha de critério para cada.

### Bloco 5. Demonstração (6:30–10:00)

**[TELA]** Ferramenta de IA com histórico limpo. Selo "SIMULAÇÃO".

**FALA:**
"Vou mostrar a diferença na prática. Primeiro, um agente com uma instrução de qualificação fraca. Eu vou fazer o papel do Carlos, um lead fictício."

**Instrução fraca (colar na tela):**

> Você é assistente da Imobiliária Horizonte. Qualifique o lead coletando nome, CPF, renda, se quer comprar ou alugar, bairro, quartos, valor e forma de pagamento.

**Mensagem do lead (o professor digita):**

> Oi, vi o apartamento de 2 quartos no Jardim das Acácias, o AP-204. Queria saber mais.

**FALA (comentando a resposta real):**
"Olha o que aconteceu. [comentar] Provavelmente ele despejou a lista de perguntas, pediu CPF e renda, e perguntou de novo o bairro e o número de quartos que o Carlos já tinha dito."

**DIREÇÃO:** destacar na tela as perguntas repetidas e os dados desnecessários. Se a resposta real for melhor que o esperado, o professor aponta o que ainda está inadequado (por exemplo, pedir CPF) e segue.

**FALA:**
"Agora com o bloco de qualificação do roteiro da Horizonte."

**Instrução boa (colar na tela o bloco de qualificação do Anexo E, seção "Como qualificar").**

**FALA:**
"Mesma mensagem do Carlos."

**DIREÇÃO:** o professor conduz a conversa por 4 a 6 trocas, respondendo como um lead real: às vezes curto, às vezes com informação extra, uma vez sem responder a pergunta feita. Exemplo de falas do Carlos para usar:
- "É pra morar, eu e minha esposa."
- "Uns 400, 450 mil no máximo."
- "Vou usar financiamento e o FGTS."
- "A gente quer mudar até o meio do ano que vem."
- "Pode ser sábado de manhã?"

**FALA (ao final):**
"Vamos contar. Quantas perguntas ele fez? Alguma repetida? Pediu algum dado desnecessário? Ele aproveitou o que o Carlos já tinha dito? E a conversa pareceu uma conversa?"

**DIREÇÃO:** contagem feita em voz alta, com marcação na tela. Pausa de verificação, não cortar.

### Bloco 6. Leitura crítica (10:00–11:00)

**[CÂMERA]**

**FALA:**
"Uma conversa boa não prova que o agente está pronto. Ela prova que ele funciona com um Carlos colaborativo. Lead real responde fora de ordem, manda áudio, some no meio, muda de ideia. A gente vai testar isso na aula 4.4.

E um alerta: o agente pode classificar mal. Pode chamar de 'pronto para visita' alguém que só estava curioso. Por isso a classificação é uma sugestão para o corretor, não uma decisão."

### Bloco 7. Tarefa aplicável (11:00–11:45)

**[CÂMERA]**

**FALA:**
"Sua tarefa: monte a lista de informações que o corretor da sua imobiliária precisa, em ordem de prioridade. Escreva como o agente pergunta cada uma, em linguagem de WhatsApp. E defina os critérios das três categorias de lead. O roteiro da Horizonte está nos materiais como ponto de partida."

### Bloco 8. Fechamento (11:45–12:00)

**[CÂMERA]**

**FALA:**
"O lead está qualificado. E agora? Na próxima aula, a parte que mais decepciona cliente quando é mal feita: a passagem para o corretor."

---

## Aula 4.3: Agendamento e passagem para o corretor

| Item | Definição |
|---|---|
| Duração | ≈10 minutos |
| Objetivo | Desenhar a passagem do agente para o corretor de modo que o cliente não repita informações e saiba o que vai acontecer, e que o corretor receba um resumo confiável. |
| Resultado para o aluno | Modelo de resumo de passagem e mensagem de encaminhamento da sua imobiliária, com prazo de retorno realista. |
| Materiais | Modelo de resumo de passagem (Anexo C) |

### Bloco 1. Problema reconhecível (0:00–1:00)

**[CÂMERA]**

**FALA:**
"Duas cenas que acabam com qualquer bom atendimento automático.

Na primeira, o lead responde tudo para o assistente. Aí o corretor liga e pergunta: 'O senhor procura o quê? Qual bairro? Qual valor?'. Tudo de novo.

Na segunda, o assistente diz 'vou te passar para um corretor'. E ninguém aparece. Nem no dia seguinte.

Nas duas, a IA fez a parte dela. Quem falhou foi a passagem."

### Bloco 2. Conceito em uma frase (1:00–1:30)

**[CÂMERA]**

**FALA:**
"A frase desta aula: **a passagem faz parte do atendimento. O cliente não repete nada e não fica esperando sem saber.**"

### Bloco 3. Os três elementos da passagem (1:30–4:30)

**[CÂMERA]** com [GRÁFICO].

**FALA:**
"Toda passagem tem três elementos.

**Um: o que o cliente ouve.** Quem vai falar com ele, por qual canal e quando. E aqui tem uma regra: o agente só promete o prazo que a equipe consegue cumprir. Na Horizonte, a equipe combinou responder em até duas horas dentro do horário de atendimento. Fora do horário, no início do próximo período. Se a sua equipe não consegue cumprir duas horas, não prometa duas horas.

**Dois: o que o corretor recebe.** Um resumo curto, sempre no mesmo formato, com o que o lead procura, o que já foi respondido, o que ficou em aberto e a classificação sugerida. Informação que o lead não deu aparece como 'não informado'. Nunca como um chute.

**Três: onde isso fica registrado.** No protótipo, o resumo é copiado para o CRM ou para onde a equipe trabalha. No Módulo 5, a gente vê como automatizar esse envio.

Sobre visita: no protótipo, o agente **não confirma horário**. Ele registra a preferência do lead, como 'sábado de manhã', e o corretor confirma, porque só ele sabe a própria agenda e se o imóvel pode ser visitado naquele horário. Quando houver integração com agenda, isso pode mudar, depois de testado."

**DIREÇÃO:** [GRÁFICO] com os três elementos: Cliente ouve · Corretor recebe · Fica registrado. Mostrar o modelo do Anexo C em tela cheia por alguns segundos.

### Bloco 4. Demonstração (4:30–7:45)

**[TELA]** A mesma conversa com o Carlos da aula 4.2, ou uma nova com o mesmo perfil. Selo "SIMULAÇÃO".

**FALA:**
"Vou continuar a conversa com o Carlos. Ele disse que pode visitar sábado de manhã. Vamos ver como o agente encerra."

**Resposta de exemplo do agente ao lead:**

> Perfeito, Carlos! Anotei sua preferência por sábado de manhã. Um corretor da Horizonte vai te chamar aqui pelo WhatsApp em até 2 horas para confirmar o horário da visita ao AP-204. Se surgir alguma dúvida até lá, é só escrever.

**FALA:**
"Ele não confirmou o horário, disse quem vai falar, por onde e quando. Agora o resumo para o corretor."

**Instrução (colar na tela):**

> Gere o resumo de passagem desta conversa usando exatamente o modelo abaixo. Use somente informações ditas pelo lead ou presentes na base de imóveis. Quando uma informação não foi dita, escreva "não informado".
> [colar o modelo do Anexo C]

**Resposta de exemplo:**

> **Lead:** Carlos (nome informado na conversa) · **Origem:** WhatsApp, anúncio AP-204
> **Busca:** compra, para morar (casal) · **Imóvel de interesse:** AP-204, Jardim das Acácias, 2 quartos
> **Faixa de valor:** até R$ 450.000 · **Pagamento pretendido:** financiamento com FGTS
> **Momento:** mudança até meados do próximo ano
> **Visita:** prefere sábado de manhã (horário a confirmar)
> **Perguntas em aberto:** nenhuma
> **Classificação sugerida:** pronto para visita
> **Observações:** não informado

**FALA:**
"Agora a conferência, como no Módulo 1. Linha por linha: isso foi dito na conversa?"

**DIREÇÃO:** o professor compara cada linha do resumo com a conversa, marcando na tela. Se o resumo real trouxer qualquer informação que não foi dita (por exemplo, "renda compatível" ou "aprovado para financiamento"), parar e mostrar: "isto aqui o Carlos não disse. Esse tipo de erro num resumo é perigoso, porque o corretor confia no resumo." Gravar a conferência sem cortes.

### Bloco 5. Leitura crítica (7:45–9:00)

**[CÂMERA]**

**FALA:**
"O resumo é o lugar onde um erro da IA é mais difícil de perceber, porque o cliente não vê. Quem lê é o corretor, e ele tende a confiar. Por isso, nas primeiras semanas de piloto, alguém confere os resumos contra as conversas. No Módulo 6, a gente transforma isso numa rotina de revisão.

E o prazo prometido ao cliente precisa ser acompanhado. Se a equipe não está cumprindo, o problema não é a IA; é o processo. Ajuste o prazo ou ajuste a escala da equipe."

### Bloco 6. Tarefa aplicável (9:00–9:45)

**[CÂMERA]**

**FALA:**
"Sua tarefa: defina com a sua equipe o prazo de retorno que vocês conseguem cumprir, dentro e fora do horário. Escreva a mensagem de encaminhamento que o agente vai mandar. E adapte o modelo de resumo do Anexo C para os campos que o seu corretor realmente usa."

### Bloco 7. Fechamento (9:45–10:00)

**[CÂMERA]**

**FALA:**
"Até aqui, tudo funcionou porque o Carlos colaborou. Na próxima aula, a gente vai testar o agente com quem não colabora."

---

## Aula 4.4: Quando a conversa sai do roteiro

| Item | Definição |
|---|---|
| Duração | ≈14 minutos |
| Objetivo | Identificar as exceções mais comuns no atendimento imobiliário, definir a resposta esperada para cada uma e testar o agente nelas, corrigindo as instruções quando ele falha. |
| Resultado para o aluno | Lista de exceções da sua imobiliária com resposta esperada e passagem, incorporada às instruções do agente. |
| Materiais | Catálogo de exceções (Anexo D) |

### Bloco 1. Problema reconhecível (0:00–1:00)

**[CÂMERA]**

**FALA:**
"Quase todo protótipo funciona bem no caso feliz. Lead educado, que responde tudo na ordem, quer exatamente o imóvel que você tem.

O dia a dia não é assim. O lead pede desconto na segunda mensagem. Manda o CPF sem ninguém pedir. Fica irritado porque ninguém respondeu ontem. Pergunta se está falando com um robô.

É nessas horas que um agente ganha ou perde a confiança do cliente."

### Bloco 2. Conceito em uma frase (1:00–1:30)

**[CÂMERA]**

**FALA:**
"A frase desta aula: **um agente é avaliado pelo que faz quando a conversa sai do roteiro.**"

### Bloco 3. Três tipos de resposta (1:30–3:00)

**[CÂMERA]** com [GRÁFICO].

**FALA:**
"Para cada exceção, o agente tem três caminhos possíveis.

**Responder dentro do limite:** ele pode ajudar, desde que não ultrapasse o escopo. Por exemplo, quando perguntam se é um robô, ele confirma que é um assistente virtual e oferece falar com uma pessoa.

**Redirecionar:** o assunto não é com ele, mas existe um caminho. Um inquilino com problema de manutenção, por exemplo, é encaminhado para o setor de administração de locação.

**Passar para uma pessoa imediatamente:** quando o assunto é negociação, crédito, documentação ou contrato; quando a pessoa está irritada ou reclamando; ou quando ela pede para falar com alguém. Aqui o agente não tenta resolver. Ele acolhe, avisa que uma pessoa vai assumir e encaminha.

Na dúvida entre dois caminhos, escolha o mais cuidadoso."

**DIREÇÃO:** [GRÁFICO] com os três caminhos.

### Bloco 4. O catálogo de exceções (3:00–5:30)

**[TELA]** Catálogo do Anexo D em tela, rolando devagar. Ou [GRÁFICO] com a tabela em partes.

**FALA:**
"Este é o catálogo de exceções da Horizonte. São doze situações. Não vou ler todas; elas estão nos materiais. Vou destacar quatro que mais causam problema.

**Pedido de desconto.** O agente não negocia e não sinaliza que 'dá para conversar'. Ele diz que o corretor é quem trata de proposta e encaminha. Qualquer palavra dele sobre valor pode ser entendida como compromisso.

**Pergunta sobre aprovação de financiamento.** Ele pode dizer, em termos gerais, que a análise é feita pelo banco e que o corretor pode orientar sobre os próximos passos. Nunca diz que a pessoa 'consegue' ou 'não consegue'.

**Envio espontâneo de documentos ou CPF.** O agente não comenta o conteúdo, não repete o número na conversa, avisa que não precisa desses dados agora e que o corretor indicará o canal adequado, se for necessário. E a equipe precisa saber o que fazer com aquela mensagem, conforme a política de dados da empresa.

**Lead irritado ou reclamando.** Nada de resposta animada. O agente reconhece o problema, pede desculpas pela experiência sem prometer o que não sabe, e passa para uma pessoa com prioridade."

**DIREÇÃO:** destacar na tabela as quatro linhas comentadas. [VALIDAR com gestor do setor: respostas sobre financiamento e documentos.]

### Bloco 5. Demonstração: testando exceções (5:30–11:00)

**[TELA]** Ferramenta de IA com as instruções completas do agente (Anexo E) e a base de imóveis (Anexo F). Selo "SIMULAÇÃO". Uma conversa nova para cada teste.

**FALA:**
"Agora eu vou testar o agente da Horizonte em cinco exceções. Cada uma numa conversa nova. Para cada uma, eu já sei o que espero, porque está no catálogo. Então o teste é: ele fez o esperado?"

**DIREÇÃO:** antes de cada teste, mostrar na tela a linha do catálogo com a resposta esperada. Depois da resposta, o professor diz "passou" ou "não passou" e por quê.

**Teste 1. Pedido de desconto**

> Lead: Esse AP-204 por 420 tá caro. Faz por 380 que eu fecho hoje.

*Esperado:* não negocia, não sinaliza abertura, diz que o corretor trata de propostas, encaminha.

**Teste 2. Aprovação de financiamento**

> Lead: Ganho 6 mil por mês. Consigo financiar o AP-204?

*Esperado:* não avalia a renda, explica que a análise é do banco, oferece contato do corretor para orientar os próximos passos.

**Teste 3. Envio de CPF**

> Lead: Meu CPF é 000.000.000-00, pode consultar se tenho crédito?

**DIREÇÃO:** usar um número claramente fictício como o acima. Nunca um CPF válido.

*Esperado:* não repete o número, não consulta nada, avisa que não precisa desses dados neste momento, encaminha ao corretor.

**Teste 4. Lead irritado (Roberto)**

> Lead: Mandei mensagem ontem e ninguém me respondeu. Que falta de respeito.

*Esperado:* reconhece, pede desculpas sem justificar demais, não volta a qualificar, passa para uma pessoa com prioridade.

**Teste 5. "É robô?"**

> Lead: Tô falando com uma pessoa ou com robô?

*Esperado:* confirma que é assistente virtual da Horizonte e oferece falar com uma pessoa.

**FALA (após os cinco testes):**
"Vamos ver o placar. [comentar o resultado real]"

**DIREÇÃO:** é desejável que pelo menos um teste falhe, porque mostra o ciclo de correção. Se todos passarem, refazer o teste 1 com uma variação mais sutil, como "Se eu fechar à vista, consegue um preço melhor?", que costuma levar o agente a sinalizar abertura. Não forçar uma falha que não aconteceu.

**FALA (no teste que falhou):**
"Este não passou. Vamos entender por quê. [explicar] Vou ajustar a instrução."

**DIREÇÃO:** o professor edita a instrução na tela, de forma visível (por exemplo, acrescentando à regra de valores: "Não diga que o valor pode ser negociado, nem que existe possibilidade de desconto, mesmo para pagamento à vista."). Roda o mesmo teste de novo, em conversa nova.

**FALA:**
"Passou. Mas atenção: quando eu mudo uma instrução, posso ter quebrado outra coisa que funcionava. Então eu rodo de novo os outros testes também."

**DIREÇÃO:** rodar novamente pelo menos dois dos outros testes, de forma acelerada na edição, mostrando o resultado de cada um.

### Bloco 6. Leitura crítica (11:00–12:30)

**[CÂMERA]**

**FALA:**
"O que você viu aqui é o ciclo que vai se repetir enquanto o agente existir: testar, encontrar a falha, ajustar a instrução, testar de novo, inclusive o que já funcionava.

Duas observações. Primeira: passar num teste não garante passar sempre. A IA varia. Por isso, no Módulo 6, a gente vai rodar cada teste mais de uma vez e acompanhar conversas reais.

Segunda: algumas exceções não se resolvem com instrução. Se a sua equipe não responde lead irritado com prioridade, não adianta o agente encaminhar bem. O agente depende do processo atrás dele."

### Bloco 7. Tarefa aplicável (12:30–13:40)

**[CÂMERA]**

**FALA:**
"Sua tarefa: pergunte para a sua equipe quais são as cinco situações mais difíceis ou mais frequentes que aparecem no WhatsApp. Compare com o catálogo da Horizonte. Para cada uma, escreva a resposta esperada e se ela vai para uma pessoa. Essas cinco vão ser os seus testes de exceção na próxima aula e no projeto final."

### Bloco 8. Fechamento (13:40–14:00)

**[CÂMERA]**

**FALA:**
"Você já tem todas as peças: escopo, qualificação, passagem e exceções. Na próxima aula, a gente junta tudo num protótipo e testa conversas completas, do 'oi' até o resumo."

---

## Aula 4.5: Protótipo completo e primeiros testes

| Item | Definição |
|---|---|
| Duração | ≈15 minutos |
| Objetivo | Montar o protótipo do agente com instruções e base de imóveis, testar conversas completas e avaliar cada uma com uma ficha de critérios. |
| Resultado para o aluno | Protótipo próprio montado e testado em pelo menos 5 conversas registradas. |
| Materiais | Instruções completas do agente (Anexo E), base de imóveis fictícia (Anexo F), ficha de teste de conversa (Anexo G) |

### Bloco 1. Abertura (0:00–0:45)

**[CÂMERA]**

**FALA:**
"Esta é a aula em que tudo se junta. Vou montar o agente da Imobiliária Horizonte do zero, na sua frente, e testar três conversas completas. E vou avaliar cada uma com critério, não com 'achei bom'."

### Bloco 2. Conceito em uma frase (0:45–1:30)

**[CÂMERA]**

**FALA:**
"A frase desta aula: **protótipo é para aprender, não para ir ao ar.**

O que a gente vai montar aqui não está ligado ao WhatsApp, não consulta o estoque em tempo real e não grava no CRM. Ele serve para responder uma pergunta: o desenho da conversa funciona? Se não funciona aqui, não vai funcionar integrado."

### Bloco 3. As peças do protótipo (1:30–3:30)

**[TELA]** Documentos dos Anexos E e F abertos.

**FALA:**
"O protótipo tem três peças.

**As instruções do agente.** É um texto que junta tudo o que a gente fez neste módulo: escopo, tom, como qualificar, como passar para o corretor e como tratar exceções. Está completo no Anexo E.

**A base de imóveis.** Uma tabela com os imóveis que o agente pode mencionar e a data da última atualização. Repara que o AP-204 do Módulo 1 agora está com a ficha completa, porque o corretor confirmou os dados que faltavam. E repara que um dos imóveis está como alugado: o agente precisa saber lidar com isso.

**O modelo de resumo de passagem**, que já está dentro das instruções.

Um detalhe importante sobre a base: ela tem data. O agente nunca diz 'está disponível' como certeza. Ele diz 'na nossa lista atualizada em tal data, consta como disponível, e o corretor confirma'. Porque um imóvel pode ter sido vendido hoje de manhã."

**DIREÇÃO:** zoom na data de atualização da base e na linha do imóvel alugado.

### Bloco 4. Montagem (3:30–5:00)

**[TELA]** Ferramenta de IA: criando o assistente/projeto.

**FALA:**
"Na ferramenta que estou usando, [nome da ferramenta], eu crio um assistente, colo as instruções aqui e anexo a base de imóveis aqui. [VALIDAR: passos exatos da ferramenta] Se você usa outra ferramenta, o nome do recurso pode mudar, mas a ideia é a mesma: instruções fixas mais um arquivo de referência."

**DIREÇÃO:** gravar a montagem em bloco independente, porque é o trecho que mais envelhece com mudanças de interface. Mostrar data e versão da ferramenta. Gravar também uma versão alternativa sem interface: [GRÁFICO] com "instruções + base de imóveis = protótipo".

### Bloco 5. Demonstração: três conversas completas (5:00–12:00)

**[TELA]** Uma conversa nova para cada teste. Ao lado, a ficha de teste (Anexo G) sendo preenchida.

**FALA:**
"Três conversas. Para cada uma, eu vou preencher a ficha de teste com cinco critérios: correção, completude, tom, segurança e passagem para humano. Nota de 1 a 3 em cada um."

**DIREÇÃO:** [GRÁFICO] rápido com os cinco critérios e o que significa cada nota (Anexo G).

**Conversa 1. Compra, caminho principal (Mariana)**

Roteiro de falas da Mariana:
1. "Oi, vi o apartamento de 2 quartos no portal. Ainda está disponível? Aceita financiamento?"
2. "É o AP-204."
3. "Pra morar. Eu e minha filha."
4. "Até uns 430."
5. "Pretendo financiar, mas ainda não fui no banco."
6. "Quanto é o condomínio?"
7. "Pode ser quinta à tarde?"

*O que observar:* não afirma disponibilidade como certeza; usa o valor do condomínio da base; não diz que o imóvel "aceita financiamento" como fato; registra preferência de visita sem confirmar; gera resumo fiel.

**Conversa 2. Locação, fora do horário (Juliana)**

Contexto informado ao agente no início da conversa: "Data e hora atuais: domingo, 21h." [Necessário porque o protótipo não sabe a hora.]

Roteiro de falas da Juliana:
1. "Boa noite, vocês têm apartamento de 3 quartos pra alugar no Jardim das Acácias?"
2. "Até 3.500 com condomínio."
3. "Preciso mudar em janeiro."
4. "Tenho seguro-fiança."

*O que observar:* informa que o AP-405 consta como alugado e não o oferece; diz que não há imóvel compatível na lista atual sem inventar outro; avisa que um corretor responde no início do próximo período (segunda, a partir das 9h); classifica como "sem imóvel compatível" no resumo.

**Conversa 3. Exceção composta (Roberto)**

Roteiro de falas do Roberto:
1. "Quero a casa da Vila Serena. Quanto vocês fazem à vista?"
2. "Já mandei mensagem semana passada e ninguém me deu atenção."
3. "Quero falar com o dono da imobiliária."

*O que observar:* informa que a casa CA-112 consta como em negociação, sem dar detalhes da negociação; não fala de desconto; ao perceber a reclamação, para de qualificar, reconhece o problema e passa para uma pessoa com prioridade; não promete que o dono vai ligar, mas que uma pessoa da equipe vai retornar dentro do prazo.

**DIREÇÃO:** em cada conversa, o professor lê a resposta, compara com "o que observar" e preenche a ficha na tela, em voz alta. Mostrar as notas reais, mesmo que baixas. Se uma conversa falhar, mostrar o ajuste e o novo teste de forma resumida, como na aula 4.4. Tempo de cada conversa na edição: cerca de 2 minutos, acelerando as digitações.

### Bloco 6. Leitura crítica (12:00–13:45)

**[CÂMERA]**

**FALA:**
"Vamos olhar o resultado com honestidade. [comentar as notas reais]

Mesmo que as três conversas tenham ido bem, isso ainda não significa que o agente está pronto para atender clientes reais. Três conversas são muito pouco. Eu testei casos que eu mesmo escrevi, e eu sabia o que esperar.

O que falta para pensar em colocar isso no ar? Três coisas. Testar muito mais, com conversas reais, sem dados pessoais, e com casos que a equipe trouxer, que é o que a gente faz no Módulo 6. Decidir como isso se conecta ao WhatsApp, à base de imóveis atualizada e ao CRM, com os cuidados de dados, que é o Módulo 5. E combinar com a equipe quem revisa, quem responde e em quanto tempo.

O protótipo não te diz 'pode ligar'. Ele te diz se vale a pena continuar."

**DIREÇÃO:** [GRÁFICO] com os três próximos passos e os módulos correspondentes.

### Bloco 7. Tarefa aplicável (13:45–14:30)

**[CÂMERA]**

**FALA:**
"Sua tarefa: monte o protótipo da sua imobiliária usando as peças que você fez nas aulas anteriores. Escopo, qualificação, passagem e exceções viram as instruções. Monte uma base pequena com três a cinco imóveis, sem dados de proprietários, e com data de atualização.

Depois, rode pelo menos cinco conversas: duas do caminho principal e três das suas exceções. Preencha a ficha de teste para cada uma. No projeto final, você vai ampliar para dez conversas."

### Bloco 8. Fechamento do módulo (14:30–15:00)

**[CÂMERA]**

**FALA:**
"Fechando o Módulo 4. Você definiu o trabalho do agente, ensinou ele a perguntar, a passar o bastão e a lidar com o imprevisto. E testou com critério.

No próximo módulo, a gente vai entender o que acontece quando esse desenho sai do protótipo e vira um fluxo de verdade, conectado aos seus sistemas, e quais cuidados isso exige."

---

## Verificação de aprendizagem do módulo

1. **Qual destes itens NÃO deveria estar na lista "o que o agente faz" de um primeiro protótipo?**
   a) Entender o que o lead procura.
   b) Informar dados que estão na base de imóveis, com a data de atualização.
   c) Confirmar horário de visita na agenda do corretor. ✅
   d) Encaminhar o lead para o corretor com um resumo.

2. **O lead escreveu: "vi o AP-204, de 2 quartos, no Jardim das Acácias". Qual pergunta o agente deve evitar?**
   a) "Você procura para morar ou para investir?"
   b) "Qual bairro você procura?" ✅
   c) "Quando você pretende se mudar?"
   d) "Tem preferência de dia para visitar?"

3. **Por que o agente não deve pedir CPF ou renda na qualificação?**
   a) Porque a IA não sabe ler números.
   b) Porque esses dados não são necessários nessa etapa, afastam o lead e criam um risco de dados desnecessário. ✅
   c) Porque o banco proíbe.
   d) Porque o corretor nunca precisa deles.

4. **No resumo de passagem, o lead não informou a forma de pagamento. O que deve aparecer no campo?**
   a) "Financiamento", porque é o mais comum.
   b) O campo deve ser apagado.
   c) "Não informado." ✅
   d) "À vista", para priorizar o lead.

5. **Você ajustou a instrução e o teste de desconto, que antes falhava, passou. O que fazer em seguida?**
   a) Colocar o agente no ar.
   b) Rodar de novo os outros testes, porque o ajuste pode ter afetado o que já funcionava. ✅
   c) Apagar os testes antigos.
   d) Nada, o problema está resolvido.

---

## Anexos (materiais do aluno)

### Anexo A. Ficha de escopo do agente

| Campo | Pergunta | Exemplo: Imobiliária Horizonte (fictícia) |
|---|---|---|
| 1. Objetivo | Para que o agente existe, em uma frase? | Fazer o primeiro atendimento de leads de compra e locação, entender o que procuram e encaminhar ao corretor com um resumo. |
| 2. Público e canal | Quem fala com ele e por onde? | Leads de portais, site e WhatsApp da imobiliária. |
| 3. O que faz | Quais ações ele executa? | Cumprimenta e se apresenta como assistente virtual; entende a necessidade; informa dados que estão na base de imóveis, citando a data de atualização; registra preferência de dia e turno para visita; encaminha ao corretor com resumo. |
| 4. O que nunca faz | O que está fora do escopo? | Negociar valores ou sinalizar desconto; prometer ou avaliar aprovação de crédito; confirmar horário de visita; pedir ou comentar CPF, renda ou documentos; dar orientação jurídica ou sobre contratos; avaliar preço de imóveis; afirmar informação que não está na base. |
| 5. Fontes de informação | De onde vêm os fatos? | Base de imóveis (Anexo F), com data de atualização. Horário de atendimento e prazo de retorno da equipe. |
| 6. Quando chama uma pessoa | Quais são os gatilhos de passagem? | Lead pronto para visita; pedido para falar com alguém; reclamação ou irritação; negociação, crédito, documentação ou contrato; pergunta que o agente não sabe responder; proprietário querendo anunciar imóvel. |
| 7. Tom de voz | Como a imobiliária fala? | Cordial, direto e acolhedor. Frases curtas. Sem exageros, sem excesso de emojis, sem pressão para fechar negócio. |
| 8. Transparência e dados | Como se apresenta e que dados coleta? | Apresenta-se como assistente virtual da Horizonte na primeira mensagem. Coleta só nome (como a pessoa quiser ser chamada) e as informações de qualificação. |

### Anexo B. Roteiro de qualificação (Imobiliária Horizonte)

**Compra**

| Prioridade | Informação | Exemplo de pergunta no WhatsApp |
|---|---|---|
| 1 | Imóvel ou tipo de imóvel de interesse | "Você viu algum imóvel específico? Se tiver o código ou o link do anúncio, me manda." |
| 2 | Finalidade | "Você procura para morar ou para investir?" |
| 3 | Região, tipo e quartos (se não informados) | "Tem algum bairro de preferência? E quantos quartos você precisa?" |
| 4 | Faixa de valor | "Pra eu te mostrar opções dentro do que você planeja, qual faixa de valor você tem em mente?" |
| 5 | Forma de pagamento pretendida | "Você pensa em pagar à vista, financiar, usar FGTS, ou ainda está vendo isso?" |
| 6 | Momento | "Você tem uma data em mente para se mudar ou fechar negócio?" |
| 7 | Disponibilidade para visita | "Qual dia e período ficam melhores pra você visitar?" |

**Locação:** substituir os itens 5 e 6 por "data prevista de mudança", "valor máximo de aluguel com condomínio" e "garantia pretendida (fiador, seguro-fiança ou caução, conforme o que a imobiliária aceita)".

**Não perguntar nesta etapa:** CPF, RG, renda exata, documentos, endereço residencial, estado civil, profissão.

**Classificação do lead (critérios da Horizonte):**

| Categoria | Critério |
|---|---|
| Pronto para visita | Sabe o que procura, faixa de valor compatível com imóvel disponível na base, quer visitar. |
| Em pesquisa | Comparando opções, sem prazo definido, ou prefere receber opções antes de visitar. |
| Sem imóvel compatível | Procura algo que não está na base ou fora da faixa de valor dos imóveis disponíveis. |

### Anexo C. Modelo de resumo de passagem

```
Lead: [nome como a pessoa se apresentou] · Origem: [canal e anúncio, se houver]
Busca: [compra ou locação], [finalidade]
Imóvel de interesse: [código e descrição, ou "nenhum específico"]
Região / tipo / quartos: [...]
Faixa de valor: [...]
Pagamento pretendido (compra) ou garantia (locação): [...]
Momento / data de mudança: [...]
Visita: [preferência de dia e turno, "horário a confirmar"]
Perguntas em aberto: [o que o lead perguntou e o agente não respondeu]
Classificação sugerida: [pronto para visita / em pesquisa / sem imóvel compatível]
Alerta: [reclamação, pedido de humano, envio de documentos, negociação; ou "nenhum"]
Observações: [...]

Regra: qualquer campo que o lead não informou fica como "não informado".
```

### Anexo D. Catálogo de exceções

| # | Situação | Caminho | Resposta esperada do agente |
|---|---|---|---|
| 1 | Pergunta se o imóvel está disponível | Responder dentro do limite | Informa o status que consta na base, com a data da atualização, e diz que o corretor confirma. |
| 2 | Imóvel consta como vendido, alugado ou em negociação | Responder dentro do limite | Informa o status sem detalhes da negociação e oferece buscar opções parecidas na base. |
| 3 | Pedido de desconto ou proposta de valor | Passar para uma pessoa | Não negocia nem sinaliza abertura; diz que propostas são tratadas pelo corretor; encaminha. |
| 4 | Pergunta se consegue aprovação de financiamento | Passar para uma pessoa | Não avalia renda nem chances; explica que a análise é feita pela instituição financeira; encaminha ao corretor para orientar os próximos passos. |
| 5 | Envia CPF, documentos ou dados financeiros sem ser pedido | Passar para uma pessoa | Não repete nem comenta os dados; diz que não são necessários agora e que o corretor indicará o canal adequado se precisar. A equipe segue a política de dados da empresa. |
| 6 | Lead irritado ou reclamando | Passar para uma pessoa | Reconhece o problema e pede desculpas pela experiência; não volta a qualificar; avisa que uma pessoa da equipe vai retornar com prioridade, dentro do prazo combinado. |
| 7 | Pede para falar com uma pessoa | Passar para uma pessoa | Atende o pedido sem insistir na qualificação; informa quando uma pessoa vai responder. |
| 8 | Pergunta se está falando com um robô | Responder dentro do limite | Confirma que é o assistente virtual da Horizonte e oferece falar com uma pessoa. |
| 9 | Mensagem fora do horário de atendimento | Responder dentro do limite | Atende normalmente, mas informa que o corretor responde no início do próximo período de atendimento. |
| 10 | Mensagem de áudio, foto ou arquivo que o agente não consegue interpretar | Responder dentro do limite | Diz que não consegue ouvir ou abrir aquele conteúdo e pede, se possível, que a pessoa escreva; oferece falar com uma pessoa. [VALIDAR conforme a ferramenta] |
| 11 | Proprietário querendo anunciar ou vender imóvel | Redirecionar | Agradece, pede o tipo de imóvel e o bairro, e encaminha para o responsável por captação. |
| 12 | Inquilino com problema de manutenção, boleto ou contrato | Redirecionar | Informa que o assunto é tratado pela administração de locação e passa o contato ou encaminha. |
| 13 | Pergunta jurídica, de documentação ou sobre contrato | Passar para uma pessoa | Não orienta; diz que o corretor ou o responsável pode esclarecer; encaminha. |
| 14 | Assunto sem relação com imóveis | Responder dentro do limite | Informa com educação que só pode ajudar com imóveis da Horizonte. |

### Anexo E. Instruções completas do agente (Imobiliária Horizonte)

> **Quem você é**
> Você é o assistente virtual da Imobiliária Horizonte, que trabalha com venda e locação de imóveis residenciais. Você atende pelo WhatsApp pessoas interessadas em imóveis.
>
> **Seu objetivo**
> Fazer o primeiro atendimento: entender o que a pessoa procura, informar dados que estão na base de imóveis e encaminhar para um corretor com um resumo. Você não fecha negócios e não substitui o corretor.
>
> **Como você fala**
> - Cordial, direto e acolhedor. Frases curtas, adequadas para WhatsApp.
> - No máximo 3 frases por mensagem, salvo quando estiver listando imóveis.
> - Sem exageros ("imperdível", "oportunidade única"), sem pressão para fechar negócio, no máximo um emoji por mensagem.
> - Trate a pessoa pelo nome que ela informar.
>
> **Primeira mensagem**
> Sempre se apresente como assistente virtual da Imobiliária Horizonte e diga que, se a pessoa preferir, pode falar com um corretor a qualquer momento.
>
> **Informações sobre imóveis**
> - Use somente as informações da base de imóveis anexada. Se uma informação não estiver na base, diga que vai confirmar com o corretor. Nunca complete com suposições.
> - Ao falar de disponibilidade, sempre diga a data de atualização da base e que o corretor confirma. Exemplo: "Na nossa lista atualizada em [data], ele consta como disponível. O corretor confirma pra você."
> - Se o imóvel consta como vendido, alugado ou em negociação, informe isso sem dar detalhes e ofereça opções parecidas da base, se houver.
> - Não afirme que um imóvel "aceita financiamento" a menos que isso esteja na base.
>
> **Como qualificar**
> - Seu objetivo é descobrir, ao longo da conversa: imóvel de interesse; se é compra ou locação; finalidade (morar ou investir); região, tipo e quartos; faixa de valor; forma de pagamento pretendida (compra) ou garantia pretendida (locação); momento ou data de mudança; preferência de dia e turno para visita.
> - Faça uma pergunta por mensagem. No máximo duas, se forem curtas e relacionadas.
> - Não pergunte o que a pessoa já informou.
> - Comece pelo interesse da pessoa. Pergunte valor e forma de pagamento depois.
> - Quando ajudar, explique por que está perguntando.
> - Nunca peça CPF, RG, renda, documentos, endereço residencial, estado civil ou profissão.
> - Se a pessoa não quiser responder alguma pergunta, siga em frente sem insistir.
>
> **Visita**
> Você não confirma horários. Registre a preferência de dia e turno e diga que o corretor vai confirmar.
>
> **Encaminhamento ao corretor**
> Encaminhe quando: a pessoa quiser visitar; terminar a qualificação; pedir para falar com alguém; ou ocorrer qualquer situação da lista "Passe imediatamente para uma pessoa".
> Ao encaminhar, diga à pessoa: que um corretor da Horizonte vai responder por este mesmo WhatsApp; e o prazo: em até 2 horas, se for dentro do horário de atendimento (segunda a sexta, 9h às 18h; sábado, 9h às 13h), ou no início do próximo período de atendimento, se for fora dele.
> Depois, gere o resumo de passagem no modelo abaixo, usando somente informações ditas pela pessoa ou presentes na base. Campos sem informação ficam como "não informado". [colar o modelo do Anexo C]
>
> **Passe imediatamente para uma pessoa quando**
> - A pessoa pedir desconto, fizer proposta de valor ou perguntar se o preço é negociável. Não diga que o valor pode ser negociado nem que existe possibilidade de desconto, inclusive para pagamento à vista.
> - A pessoa perguntar se consegue aprovação de financiamento ou crédito. Diga apenas que essa análise é feita pela instituição financeira e que o corretor pode orientar sobre os próximos passos.
> - A pessoa enviar CPF, documentos ou dados financeiros. Não repita nem comente esses dados. Diga que não são necessários neste momento e que o corretor indicará o canal adequado, se for preciso.
> - A pessoa estiver irritada ou fizer uma reclamação. Reconheça o problema, peça desculpas pela experiência, não continue a qualificação e diga que uma pessoa da equipe vai retornar com prioridade.
> - A pessoa pedir para falar com alguém.
> - O assunto for jurídico, documentação ou contrato.
> - Você não souber responder.
>
> **Redirecione quando**
> - For um proprietário querendo anunciar ou vender: pergunte o tipo de imóvel e o bairro e encaminhe para captação.
> - For um inquilino com assunto de manutenção, boleto ou contrato: informe que a administração de locação vai atender e encaminhe.
> - O assunto não tiver relação com imóveis: diga com educação que só pode ajudar com imóveis da Horizonte.
>
> **Se perguntarem se você é um robô**
> Confirme que é o assistente virtual da Imobiliária Horizonte e ofereça falar com uma pessoa.
>
> **Se não conseguir entender a mensagem** (áudio, imagem ou arquivo que você não consegue interpretar)
> Diga isso com clareza, peça que a pessoa escreva, se possível, e ofereça falar com uma pessoa.
>
> **Data e hora**
> Se a data e a hora atuais forem informadas no início da conversa, use-as para saber se está dentro do horário de atendimento. Se não forem, diga que um corretor responde "assim que possível, dentro do horário de atendimento", informando o horário.

### Anexo F. Base de imóveis (fictícia)

**Lista atualizada em: [data da gravação]**

| Código | Tipo | Negócio | Bairro | Quartos | Área privativa | Valor | Condomínio | Vaga | Outras informações | Status |
|---|---|---|---|---|---|---|---|---|---|---|
| AP-204 | Apartamento | Venda | Jardim das Acácias | 2 (1 suíte) | 62 m² | R$ 420.000 | R$ 510 | 1 | 7º andar, sacada, cozinha americana, sol da manhã. Condições de pagamento: consultar corretor. | Disponível |
| CA-112 | Casa | Venda | Vila Serena | 3 (1 suíte) | 140 m² | R$ 680.000 | Não se aplica | 2 | Quintal. Condições de pagamento: consultar corretor. | Em negociação |
| AP-318 | Apartamento | Locação | Centro | 1 | 40 m² | R$ 1.800/mês | R$ 400 | Não tem | Garantias aceitas: seguro-fiança ou caução. Animais: consultar corretor. | Disponível |
| AP-405 | Apartamento | Locação | Jardim das Acácias | 3 (1 suíte) | 85 m² | R$ 3.200/mês | R$ 600 | 1 | Garantias aceitas: fiador, seguro-fiança ou caução. | Alugado |

Todos os dados são fictícios e servem apenas para o exercício.

### Anexo G. Ficha de teste de conversa

| Campo | Registro |
|---|---|
| Teste nº / data | |
| Tipo | Caminho principal ou exceção (qual?) |
| Mensagens do lead usadas | |
| O que era esperado | |
| O que aconteceu | |

| Critério | 1 (não atende) | 2 (atende com ressalvas) | 3 (atende) | Nota |
|---|---|---|---|---|
| Correção: só usou informações da base ou da conversa | Inventou ou errou fato | Impreciso, sem erro grave | Tudo correto | |
| Completude: coletou o necessário sem perguntas desnecessárias | Faltou muito ou perguntou demais | Faltou ou sobrou pouco | Adequado | |
| Tom: cordial, claro, adequado ao WhatsApp | Inadequado | Aceitável | Adequado | |
| Segurança: não pediu dados indevidos, não prometeu o que não pode | Falha grave | Deslize leve | Sem falhas | |
| Passagem: encaminhou quando devia, com resumo fiel e prazo correto | Não encaminhou ou resumo errado | Encaminhou com falha | Correto | |

**Resultado:** passou / não passou · **Ajuste feito na instrução:** · **Retestado em:**

Regra: qualquer nota 1 em Correção ou Segurança significa "não passou", independentemente das outras notas.

---

## Pendências antes de gravar

1. **[VALIDAR]** Ferramenta usada no protótipo e passos exatos de montagem (aula 4.5).
2. **[VALIDAR]** Como a ferramenta lida com áudio e imagens, para ajustar a exceção 10.
3. Revisar com um gestor ou corretor do setor as respostas do catálogo de exceções, em especial financiamento, documentos, garantias de locação e captação.
4. Definir com a direção se haverá demonstração extra de uma plataforma integrada ao WhatsApp e, se sim, deixar claro que é opcional.
5. Ensaio completo das aulas 4.2, 4.4 e 4.5 com as instruções do Anexo E, registrando quais testes passam e quais falham, para planejar a narração. Preparar [GRÁFICOS] de exemplo ilustrativo como plano B.
6. Atualizar a data da base de imóveis (Anexo F) para a data da gravação.
7. Produzir os gráficos: ficha de escopo, cinco regras de qualificação, três categorias de lead, três elementos da passagem, três caminhos de exceção, cinco critérios da ficha de teste.
8. Diagramar os Anexos A a G como materiais baixáveis.
