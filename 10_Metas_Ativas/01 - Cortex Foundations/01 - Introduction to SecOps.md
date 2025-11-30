# 📝 What Is a SOC?/Introduction to SecOps

**Assunto:** #cortex #fundamentos #soc

---

## 📌 Resumo Rápido
A aula oferece uma visão geral do Centro de Operações de Segurança (SOC), seus objetivos e estratégias.
## 🧠 Anotações Principais
- O objetivo de um time de SOC é detectar, analisar e responder a incidentes de cibersegurança, combinando tecnologias e processos para ajudar a mitigar esses incidentes.
- O time de SOC vai receber alertas de diversas fontes dentro da organização, filtrar aquilo que é falso positivo e responder a todos os casos.
- O SOC não é responsável por desenvolver estratégias de segurança, o foco do SOC é a operação dia a dia, respondendo a incidentes.
- Um time de SOC consiste em analistas de cibersegurança em sua maioria, porém isso não impede que haja pessoas melhor capacitadas, com habilidades de analise forense avançadas ou engenharia reversa de malware, tudo com foco em auxiliar a responder aos incidentes.
- Objetivos e estratégias de um SOC:
	- Para criar o SOC de uma organização, primeiro é necessário definir os objetivos de cada uma das áreas da organização, tal como as estratégias tomadas por cada responsável da área. Com essa estratégia bem definida e documentada, uma infraestrutura será implementada com as tecnologias, ferramentas e processos necessários.
	- Dentro disso, os objetivos de um SOC são os seguintes: planejamento, análise e eficiência.
		- **Planejamento**: O planejamento deve ser extremamente bem feito, tanto na parte física quando processual. Problemas como iluminação e acústica não devem ser ignorados, assim como ambientes para diferentes finalidades(sala de operações, sala de guerra, sala de gerenciamento, etc...). Um ambiente de SOC deve possuir um layout confortável e funcional para a operação, assim como o conforto, a visibilidade, a eficiência e o controle devem fazer parte disso, se adequando a cada uma das áreas necessárias.
		- **Análise**: O benefício mais importante de possuir um SOC é o fato de que há uma detecção, análise e resposta a eventos de diferentes tipos, partindo de endpoints, servidores, redes, websites, etc.. Sendo realizada de uma forma efetiva, pode prevenir ataques e incidentes antes que se tornem críticos.
		- **Eficiência**: Um SOC bem feito, e eficiente auxilia com que outras áreas sejam alavancadas nos quesitos de eficiência e desenvolvimento. Quando as análises do time de SOC estão sendo bem realizadas, times como automação e orquestração de tecnologias, e inteligência de ameaças acabam precisando se desenvolver também, para que tudo funcione no mesmo ritmo. Nesse caso não é algo subjetivo "Aquele time está mais desenvolvido, não podemos ficar para trás", e sim algo exato, pois se outras áreas não estiverem funcionando, não é possível que o SOC seja tão eficiente e assertivo pois haverão casos de usos mal configurados, ameaças sendo detectadas com atraso muito grande, ferramentas ou comunicações não funcionando corretamente, etc... Isso gera uma melhoria contínua no ambiente.
## 🔑 Conceitos Chave
- [[SecOps]]

## ❓ Dúvidas / A Pesquisar
- [ ] Como é o SecOps na prática, exemplo, como eu diferencio as atividades de um SOC para as atividades de SecOps? Ou isso tudo é entrelaçado?
- [ ] O planejamento de um SOC fala sobre a infraestrutura de tecnologia e física do ambiente, porém eu entendo que não ocorre dessa forma, existe um time(da empresa ou terceirizado) que vai cuidar de atividades como a infraestrutura física do ambiente, assim como existe o próprio time de TI ou de Infra que vai subir as ferramentas, e o time de segurança costuma subir apenas ferramentas de "SIEM", "XDR", etc... Assim como solicitar medidas de segurança para manter a privacidade física do local. Como deveria funcionar isso de fato?  Quem cuida do que? Ou isso tudo é uma prática de SecOps? Onde juntam algumas áreas para realizar essas tarefas?(ou como deveria ser, pq na prática sabemos que em 90% dos casos não ocorre dessa forma)

# 📝 A Day in the Life of a SOC Analyst/Introduction to SecOps

**Assunto:** #cortex #fundamentos #soc 

---

## 📌 Resumo Rápido
O curso vai descrever os processos e desafios diários de um analista SOC

## 🧠 Anotações Principais
- O principal desafio de um analista SOC atualmente está relacionado a quantidade de ferramentas presentes no ambiente, onde há a necessidade dele navegar entre elas para investigar um incidente por completo, tendo em vista que muitas vezes essas ferramentas não se conversam entre si.
- Essa quantidade elevada de ferramentas dificulta o trabalho de um analista prioriza alertas, tal como torna mais difícil obter um contexto completo de cada incidente.
- Além dos pontos informados anteriormente, cada ferramenta precisa ser configurada de forma precisa para que ela agregue com a defesa do ambiente, tal como não gere impactos negativos.
- Seguindo essa linha de raciocínio das ferramentas em um ambiente SOC, se cada ferramenta possui seus próprios alertas, e cada uma gera uma quantidade elevada de incidentes, isso resulta em uma demanda alta para analistas SOC. Um estudo apontou que times de SOC costumam resolver apenas 7% dos seus caso por semana.
- Sem falar que cada uma dessas ferramentas demanda um tempo de setup, e suporte.
- Abaixo segue um exemplo de uma análise de um incidente SOC:
	- O primeiro passo do SOC parte de alertas que são gerados a partir do encaminhamento de eventos para o SIEM(Security Information and Event Management)
	- Após ser gerado um alerta por parte do SIEM, o analista vai realizar uma investigação do alerta no SIEM, e nas ferramentas atreladas. Então no caso de uma conexão de rede suspeita, o analista vai acessar a ferramenta de "Network Analysis" para entender todo o contexto da conexão e tentar decifrar os usuários que participaram.
	- E por fim vai acessar a ferramenta de EDR no endpoint do usuário para validar o processo que gerou a conexão suspeita.
- Todo esse processo do dia a dia de um analista está atrelado também a um último ponto, processos. Para todas essas etapas o analista possui processos bem definidos e alinhados com a organização para serem seguidos.


## 🔑 Conceitos Chave
- N/A

## ❓ Dúvidas / A Pesquisar
- [ ] Como devem ser desenhados esses processos? Playbooks e Runbooks
# 📝 Incident Lifecycle and Response/Introduction to SecOps

**Assunto:** #cortex #fundamentos  #soc 

---

## 📌 Resumo Rápido
A aula tem como objetivo ensinar sobre eventos e incidentes de segurança, tal como o ciclo de vida de um incidente e o ciclo de vida da resposta de um incidente.

## 🧠 Anotações Principais
- Podemos definir incidentes como eventos adversos, ou ameaças de eventos adversos que ocorre em computadores, redes ou aplicativos.
	- Eventos adversos são eventos que geram resultados negativos(Um malware em um host, um SSH não autorizado a um servidor, ou até a indisponibilidade de um serviço crítico)
	- Incidente de segurança é a violação, ou ameaça iminente a violação de uma política de segurança, politica do ambiente ou até as boas práticas de segurança.
- O ciclo de vida de um incidente é um processo que é repetido sempre que há um incidente de segurança, e consiste em identificar, investigar e mitigar incidentes de segurança e ameaças de forma contínua. Abaixo estão as 4 fases/funções principais desse ciclo:
	- Identificação: Os analistas são responsáveis por processar incidentes, atribuir uma prioridade e caso sejam atividades suspeitas serão investigados.
	- Investigação: Nessa etapa ocorre a investigação completa do incidente, onde o analista é responsável por detectar a "root cause" e os impactos dos incidentes, pois isso será essencial no processo de resposta ao incidente, dando um "norte" para o tipo de ação que deve ser tomada.
	- Mitigação: O responsável da investigação vai realizar a resposta para mitigar o incidente, realizando as atividades necessárias para interromper o incidente se ele estiver ocorrendo, ou impedir que ele ocorra novamente.
	- Melhora contínua: Após todos os processos de resposta do incidente os analistas possuem "Lições aprendidas" que servem para melhorar o ambiente. Caso o incidente tenha sido causado devido a credencial de um usuário que vazou, e ele tinha mais privilégios que os necessários para sua função, nessa etapa da melhoria contínua seria implementada uma arquitetura de privilégio mínimo dentro do ambiente, assim caso uma conta vazasse ela não possuiria privilégios elevados, mitigando os danos de um possível evento futuro.
- A resposta a incidentes se trata de processos para detecção e analise de incidentes, mitigando seus impactos e efeitos, e recuperando os sistemas ao normal.
	
	![[ciclo_resposta_incidente.png]]
	- Preparação: Um componente crítico da preparação é o "Plano de resposta a incidentes", um documento responsável por escrever os processos em caso de um incidente de segurança desde as funções de cada time e até pessoa, até o momento da realização de uma análise forense, etc...
	- Detecção e análise: Após o processo de uma classificação, análise e triagem de um incidente ocorre o momento de coletar evidências do sistema que está sofrendo ou sofreu o incidente.
	- Contenção, erradicação e recuperação: Após o momento que foi declarado um incidente de segurança, foram tomadas evidências e etc... Torna-se necessário realizar a contenção do caso, tentando ao máximo minimizar os efeitos do incidente(caso houve uma invasão na rede, deve ocorrer o processo de impedimento de exfiltração de dados por meio desse invasor)
	- Atividades pós incidente: Após todos os processos descritos anteriormente terem sido realizados, é o momento de revisar tudo que ocorreu, entender o que funcionou e principalmente o que não funcionou, e quais foram os erros cometidos.
		- *Durante a segunda guerra o exercito japonês estava tentando entender o motivo pelo qual todos os seus aviões estavam sendo abatidos. Acontece que quando um avião voltava para base, os responsáveis analisavam esses aviões e observavam quais eram os pontos com mais buraco de bala para reforça-los, quando na verdade deveriam estar reforçando aqueles pontos que não tinham buraco de bala*

## 🔑 Conceitos Chave
- [[Incidente de segurança X Evento adverso]]

## ❓ Dúvidas / A Pesquisar
- [ ] Não ficou clara a diferença de um incidente de segurança para um evento adverso, pesquisar e entender a diferença de um evento, incidente, evento de segurança, incidente de segurança, etc...
# 📝 Cybersecurity Frameworks/Introduction to SecOps

**Assunto:** #cortex #fundamentos #soc 

---

## 📌 Resumo Rápido
A aula vai abordar cinco frameworks de cibersegurança, o National Institute of Standards and Technology (NIST) Cybersecurity Framework, NIST Special Publication 800-61, Federal Risk and Authorization Management Program (FedRAMP), Federal Information Systems Management Act (FISMA), e MITRE ATT&CK.

## 🧠 Anotações Principais
- Os frameworks busca auxíliar empresas no planejaento, avaliação, revisão e gerenteciamento da sua cibersegurança.
	- NIST
	    - Foi desenvolvido pelos Estados Unidos com foco em ajudar organizações a melhorar sua postura em relação a ciber ataques.
	    - É baseado em padronizações, guidelines e melhores práticas para o melhor gerenciamento e redução de riscos cibernéticos. Também encoraja a comunicação entre organizações internas e investidores externos, em relação a cibersegurança.
	    - Oferece uma metodologia escalável, aplicável para empresas de todos os setores e tamanhos, tal como possui funcionalidades embutídas que podem ser customizadas.
	    - O NIST possui três principais componentes:
	        - Core: Fornece um conjunto de atividades recomendadas durante o processo de implementação de cibersegurança para empresas de todos os portes.
	        - Implementation Tiers: Fornece uma visão organizacional sobre cibersegurança e gerenciamento de riscos, ajudando nas discussões sobre objetivos, e valores a serem investidos dentro da área de ciber.
	        - Profiles: Fornece meios de fortalecer processos já existentes, ou a criação de novos processos, focando em cibersegurança.
    - NIST Special Publication 800-61
	    - Esse framework também é um NIST, mas seu foco agora é na resposta a incidentes de segurança. Possui instruções detalhadas para times de resposta a incidentes, e vai ajudar na criação de planos e processos.
			- Plan: O NIST recomenda que cada plano de resposta a incidentes possua um propósito, as prioridades bem definidas, uma organização sobre a estrutura e as pessoas, métricas sobre a eficácia do time de resposta a incidentes e uma evolução constante.
			- Process Review: Recomenda a revisão de cada incidente, com a atividade de pós-incidente para garantir que a organização esteja cada vez mais forte e prepara para possíveis incidentes de segurança.
	- FedRAMP
		- É um programa governamental dos Estados Unidos, com objetivo de melhorar o TI abandonando tecnologias ultrapassadas. Além disso possui uma abordagem padronizada para avaliar seviços de nuvem que os orgãos governamentais dos EUA utilizarão, junto a um processo de autorização padrão(autorizando o fornecedor de nuvem a prestar serviço, ou vender um produto, para o respectivo orgão), junto a um guia para realizar o monitoramento contínuo de serviços e produtos em nuvem.
		- O FedRAMP é designado para ser eficiênte e ágil, segue abaixo algumas características desse framework:
			- Effective Cloud Security: Fornece uma estrutura para criar e gerenciar processos para uma segurança efetíva. Essa estrutura pode ser repetída para quantos processos forem necessários.
			- Marketplace: O framework possuí uma lista de serviços em nuvem para que as agências governamentais possam colaborar entre sí.
			- Security Baselines: O FedRAMP fornece quatro níveis mínimos de segurança obrigatórios, cada nível para um tipo de ativo diferente, que são definidos por sua importância
				- Ativos de alta prioridade devem possuir no mínimo um conjunto de 421 controles.
				- Ativos de prioridade moderada devem possuir no mínimo um conjunto de 325 controles.
				- Ativos de baixa prioridade devem possuir no mínimo um conjunto de 125 controles.
				- Serviços(SaaS) de baixo impacto  devem possuir no mínimo um conjunto de 36 controles.
		- O FedRAMP atua em conjunto com diversas agências para atingir seus respectivos objetivos de acelerar a transição para serviços de núvem(On-Prem > Cloud), aumentar a confiança, garantir aplicação consistente das políticas de segurança e promover automação para aproximar dados em tempo real com monitoramento contínuo.
	- FISMA
		- É uma lei federal dos estados únidos que entrou en vigência em 2002, e ganhou sua última versão dem 2014.
		- Implementa uma estrutura abrangente para proteger sistemas da informação utilizadas por agências governamentais dos estados únidos.
		- A lei torna necessário que as agências desenvolvam implementem e documentem um programa de proteção a segurança da informação
		- A lei cobre uma estrutura para conformidade das agências, definindo uma série de requisitos, requisitos:
			- Inventário de sistemas de informação
			- Categorização de informações e sistemas de informação por nível de risco
			- Seleção de controles de segurança e requisitos de garantia adequados
			- Avaliação de riscos
			- Plano de segurança do sistema
			- Certificação e acreditação
			- Monitoramento contínuo
	- MITRE ATT&CK
		- É uma base de conhecimento repleta de táticas e técnicas(TTPs) utilizadas por atacantes. 
		- O framework vai facilitar a visualização sobre diversos tipos de ataques por meio de uma agregação de diversos dados.
		- Dentro do site oficial do framework, nos botões de navegação presentes na parte superior, acessando "CTI>Groups" possuímos uma relação de grupos de ataques conhecidos, e as principais técnicas utilizadas por eles. Caso a sua empresa seja do ramo X, vale a pena pesquisar por grupos de ataques que focam empresas desse ramo para observar as principais técnicas utilizadas por cada grupo, tal como softwares.
		- Ferramentas como o Cortex utilizam o MITRE e cruza as TTPs listadas com as regras ativas no ambiente, criando insights como "Suas regras cobrem apenas 40% das TTPs listadas no MITRE ATT&CK"
		- O framework consiste em algumas táticas, cada uma possui uma lista de técnicas utilizadas por atacantes para chegar nos seus respectivos objetos, e dentro de cada técnica presente no MITRE, são listados os seus respectivos procedimentos(TTPs = Táticas, Técnicas e Procedimentos)
	- ISO Standards(International Organization for Standardization)
		- Pública diversos documentos de padronização relacionados a segurança da informação, evidências digitais e gestão de resposta a incidentes.
		- Abaixo estão alguns padrões públicados, mas existem vários:
			- ISO/IEC 27035-1 - Princípios para gestão de incidentes
			- ISO/IEC 27035-2 - Diretrizes para o planejamento e preparo para a resposta a incidentes
			- ISO/IEC 27037 - Diretrizes para identificação, coleta, aquisição e preservação de evidências digitais
			- ISO/IEC 27042 - Diretrizes para análise e interpretação de evidências digitais
			- ISO/IEC 27043 - Processos e princípios de resposta a incidentes

## 🔑 Conceitos Chave
ISO Standards
MITRE ATT&CK
FISMA
FedRAMP
NIST Special Publication 800-61
NIST

## ❓ Dúvidas / A Pesquisar
- [ ] N/A