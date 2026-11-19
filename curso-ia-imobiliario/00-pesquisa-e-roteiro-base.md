# Curso de IA aplicada a negócios — pesquisa e roteiro-base

**Professor:** Cleiton Campano  
**Direção:** Bruno Pessoa  
**Versão de trabalho:** 19 de novembro de 2026

## Recomendação de produto

A proposta mais coerente com a experiência pública de Cleiton é um curso prático de **IA aplicada à experiência do cliente e aos processos de negócio**, com demonstrações de atendimento, qualificação de contatos e agentes conversacionais. Não recomendo posicioná-lo como um curso genérico de “todas as ferramentas de IA”: esse território fica rapidamente desatualizado e disputa atenção com ofertas muito amplas. O diferencial pode ser mostrar como identificar uma oportunidade, desenhar o fluxo, prototipar uma solução, avaliar a qualidade e decidir quando a automação deve passar para uma pessoa.

A página da Recrutei Academy descreve Cleiton como fundador e CEO, com experiência em tecnologia, IA, marketing, design thinking, service design, CX e EX, além de passagem por Dock, Zup Innovation e Algar. O Senac Minas o apresenta como fundador e CEO da Growmate e informa que atua no desenvolvimento e orquestração de agentes de IA no WhatsApp para captação de conversas, qualificação de contatos e atendimento. Essas experiências sustentam uma narrativa de aplicações em negócios e experiência do cliente, mas não bastam, por si só, para afirmar resultados específicos ou credenciais técnicas além do que as fontes declaram.[1] [2]

A hipótese de público para a primeira versão é formada por empreendedores, gestores, profissionais de atendimento, marketing e operações que querem aplicar IA sem precisar programar. É uma hipótese editorial e comercial a validar com entrevistas e pré-venda. A promessa deve ser concreta e verificável: **“Ao final, você vai conseguir mapear um processo, escolher uma aplicação adequada de IA, montar um protótipo assistido e avaliar riscos, qualidade e necessidade de supervisão humana.”** Evitar promessas de renda, substituição de equipes ou automação “100% autônoma”.

## O que a pesquisa sugere incluir

O AI Index 2025 de Stanford informa que 78% das organizações pesquisadas reportaram uso de IA em 2024, ante 55% em 2023, e sintetiza evidências de ganhos de produtividade, mas também registra desafios de avaliação responsável e limitações de raciocínio. É um dado internacional, não uma estimativa específica do mercado brasileiro. Para o curso, isso favorece ensinar aplicação com critério, medição e checagem, em vez de vender apenas familiaridade com ferramentas.[3]

Um modelo de competências publicado na ACM organiza a literacia em IA generativa em conhecimentos fundamentais, prompting, habilidades técnicas e considerações éticas e legais. O estudo de diretrizes disponível no arXiv destaca seleção de ferramentas, interação crítica e limites dos modelos. Em conjunto, essas referências apoiam uma jornada didática que ensine a fazer, revisar e decidir — e não apenas a escrever comandos.[4] [5]

O MEC, em suas formações de IA para docentes, combina fundamentos, aplicações, uso crítico, ética e prática contextualizada. Embora seja uma referência educacional, não voltada a negócios, a lógica de aprendizagem por aplicação e responsabilidade é transferível.[6] A ANPD publicou um radar tecnológico sobre IA generativa que deve servir de leitura de apoio para o bloco de dados e privacidade. O curso não deve oferecer aconselhamento jurídico: deve ensinar precauções operacionais, como não inserir dados pessoais ou confidenciais sem autorização e revisar as configurações e termos da ferramenta usada.[7]

Na comparação de mercado, a página da Impacta apresenta um curso de IA e automação de agentes com n8n com 28 horas, unindo fundamentos e construção de fluxos no-code. A existência desse tipo de oferta mostra que automação prática já é uma categoria visível. A oportunidade editorial para Cleiton é se diferenciar pela conexão entre processo, experiência do cliente, desenho do atendimento, critérios de qualidade e decisão de automatizar — não competir apenas por quantidade de integrações ou ferramentas.[8]

## Arquitetura sugerida

**Formato inicial:** 6 módulos, 18 aulas de 8 a 15 minutos, cerca de 3,5 a 4,5 horas de conteúdo principal. Acrescentar arquivos de apoio e exercícios curtos. Gravar demonstrações de tela em blocos independentes para facilitar atualização de ferramentas. Manter ferramentas apresentadas como exemplos substituíveis, com data de gravação visível.

| Módulo | Resultado de aprendizagem | Conteúdo e demonstração |
|---|---|---|
| 1. IA sem mistério | Distinguir IA tradicional, generativa e automação; reconhecer o que um modelo faz e onde pode falhar. | Conceitos em linguagem simples; demonstração da mesma tarefa com resposta útil e resposta inventada; mapa “bom para / verificar / não delegar”. |
| 2. Encontrar o caso de uso | Selecionar tarefas adequadas a IA com base em valor, frequência, risco e necessidade de julgamento humano. | Mapa de jornada; matriz de priorização; exemplo de dúvidas repetidas no atendimento; exercício de escolha de um processo. |
| 3. Trabalhar com copilotos | Criar instruções úteis e iterar com contexto, formato de saída, critérios e exemplos. | Estrutura de prompt; transformar briefing ruim em instrução testável; revisar e checar respostas; biblioteca de modelos adaptáveis. |
| 4. IA na experiência do cliente | Esboçar uma conversa de atendimento e qualificação, definindo escopo, tom, limites e passagem para humanos. | Jornada de conversa; perguntas de descoberta; tratamento de exceções; demonstração de agente ou protótipo, sem prometer integração universal. |
| 5. Automação com segurança | Entender os componentes de um fluxo e reconhecer riscos de dados, erros e ações externas. | Gatilho, contexto, modelo, validação, ação e registro; simular um fluxo; casos de falha; LGPD e dados confidenciais em nível operacional. |
| 6. Medir, melhorar e colocar em uso | Avaliar qualidade e decidir se o processo deve ser mantido, ajustado ou interrompido. | Rubrica de qualidade; taxa de resolução, tempo, satisfação e escalonamento; plano piloto; checklist de supervisão e melhoria contínua. |

**Projeto final:** o aluno escolhe um processo simples, desenha o estado atual, propõe uma melhoria com IA, cria um protótipo (mesmo que manual ou em ferramenta no-code), testa pelo menos cinco casos — incluindo exceções — e apresenta uma decisão: automatizar, manter apoio humano ou não usar IA. O resultado é mais demonstrável do que uma coleção de prompts.

## Roteiro-base para a primeira aula

**Aula 1.1 — O que a IA pode fazer pelo seu trabalho (10–12 min)**  
**Objetivo:** alinhar expectativas e apresentar a promessa do curso.  
**Tela:** professor em plano médio; depois demonstração de uma solicitação de cliente e da resposta gerada; fechar com mapa visual “tarefa → IA → revisão → ação”.

**Abertura — 0:00–0:45**  
“Se você já abriu uma ferramenta de inteligência artificial, fez uma pergunta e recebeu uma resposta convincente, talvez tenha pensado: ‘isso vai resolver tudo’. Ou talvez tenha testado uma vez, recebido algo genérico e concluído que não serve para o seu trabalho. Neste curso, vamos sair desses dois extremos. Você vai aprender a encontrar tarefas em que a IA ajuda de verdade, orientar o sistema, conferir o resultado e reconhecer quando uma pessoa precisa assumir.”

**Contexto — 0:45–2:30**  
“Eu sou Cleiton Campano. Minha atuação combina tecnologia, inteligência artificial e experiência do cliente. Ao longo do curso, vamos olhar para situações concretas de negócio: entender uma demanda, responder com contexto, organizar informação e apoiar processos de atendimento. A ideia não é decorar nomes de ferramentas. É aprender um método que continue útil mesmo quando as ferramentas mudarem.”

**Demonstração — 2:30–6:30**  
Na tela, apresentar uma mensagem fictícia de cliente: “Comprei há uma semana, ainda não recebi e não sei onde está meu pedido.” Primeiro, pedir à IA “responda ao cliente” e mostrar uma resposta genérica. Em seguida, adicionar contexto fictício, tom, objetivo e limites: não inventar status do pedido; pedir identificador de forma segura; explicar o próximo passo; encaminhar para uma pessoa se não houver acesso ao sistema. Comparar as respostas e narrar: “A instrução melhorou a forma da resposta. Mas não criou acesso ao pedido nem comprovou os fatos. A IA pode ajudar a redigir; a informação operacional precisa vir de uma fonte confiável.”

**Princípio central — 6:30–8:30**  
“Pense na IA como uma etapa de um processo, não como o processo inteiro. Antes de automatizar, precisamos saber qual problema estamos resolvendo, quais dados podem ser usados, como vamos verificar o resultado e o que acontece quando a resposta não é suficiente. Se a tarefa envolve dados pessoais, informação confidencial, dinheiro, saúde, direitos ou uma decisão importante, o nível de cuidado sobe. Não coloque informações sensíveis em uma ferramenta sem autorização e sem entender como os dados serão tratados.”

**Exercício — 8:30–10:30**  
“Escolha uma tarefa que você repete toda semana. Anote: qual é a entrada, o que você precisa produzir, como sabe que ficou bom e o que pode dar errado. Na próxima aula, vamos usar esse mapa para decidir se a IA é uma boa ajuda, uma ajuda parcial ou uma escolha inadequada.”

**Fechamento — 10:30–11:00**  
“Seu primeiro objetivo não é automatizar tudo. É escolher uma tarefa pequena, testar com critério e aprender com o resultado. Vamos começar pelo processo, não pela ferramenta.”

## Orientações de direção e gravação

Para cada aula, usar a mesma espinha dorsal: problema reconhecível, conceito em uma frase, demonstração completa, leitura crítica do resultado e tarefa aplicável. Intercalar câmera com tela; gravar narração em frases curtas; manter a interface ampliada e esconder notificações, nomes, dados reais e informações de clientes. Usar cenários fictícios em todas as demonstrações. Registrar a versão e data das ferramentas mostradas e capturar planos alternativos sem interface quando uma atualização puder tornar a aula obsoleta.

Na direção, pedir a Cleiton que explique decisões em voz alta: por que escolheu aquele caso, que dado está faltando, o que pode dar errado e qual seria a passagem para um humano. Isso transmite raciocínio profissional e diferencia o curso de uma simples gravação de cliques. Não editar pausas de verificação que ajudem o aluno a compreender o método. Inserir capítulos, legendas, materiais baixáveis e um aviso claro de que ferramentas, interfaces e funcionalidades podem mudar.

**Materiais complementares:** mapa de processo de uma página; matriz de priorização; modelos de prompts editáveis; checklist de teste com exemplos de exceções; ficha para avaliar resposta (correção, completude, tom, segurança e necessidade de escalonamento); plano piloto de duas semanas. Os modelos devem ser apresentados como pontos de partida e sempre ajustados ao contexto e às regras da organização.

## Decisões a fechar antes do roteiro integral

1. Público prioritário: empreendedores/PMEs, equipes de atendimento e CX, ou profissionais de conhecimento em geral.
2. Profundidade técnica: usuário de copilotos, construtor no-code de automações, ou trilha híbrida com fundamentos e demonstrações.
3. Ferramentas que Cleiton poderá demonstrar e se haverá custos, contas ou integrações necessários para o aluno acompanhar.
4. Resultado verificável do curso e limites da promessa comercial.
5. Casos reais autorizados para uso; na ausência de autorização, desenvolver casos fictícios compostos e identificá-los como simulações.
6. Oferta e entrega: curso gravado autônomo, comunidade, plantões ou atualização periódica de aulas.

## Referências

[1]: https://academy.recrutei.com.br/site/speakers/cleiton-campano "Perfil de Cleiton Campano na Recrutei Academy"
[2]: https://mg.senac.br/web/comunicacao/w/sistema-fecom%C3%A9rcio-promove-palestra-gratuita-sobre-intelig%C3%AAncia-artificial-no-atendimento-ao-cliente-em-araguari "Senac Minas: IA no atendimento ao cliente"
[3]: https://hai.stanford.edu/ai-index/2025-ai-index-report "Stanford AI Index Report 2025"
[4]: https://dl.acm.org/doi/10.1145/3685680 "Generative AI Literacy: Twelve Defining Competencies"
[5]: https://arxiv.org/html/2504.19038v1 "Generative AI Literacy: A Comprehensive Framework for Leveraging Generative AI"
[6]: https://www.gov.br/mec/pt-br/escolas-conectadas/competencias-e-formacao/bloco-tematico-3-inteligencia-artificial-na-educacao "MEC: Inteligência Artificial na Educação"
[7]: https://www.gov.br/anpd/pt-br/centrais-de-conteudo/documentos-tecnicos-orientativos/radar_tecnologico_ia_generativa_anpd.pdf "ANPD: Radar Tecnológico sobre Inteligência Artificial Generativa"
[8]: https://www.impacta.com.br/cursos/ia-e-automacao-de-agentes-com-n8n/ "Impacta: Curso de IA e Automação de Agentes com n8n"
