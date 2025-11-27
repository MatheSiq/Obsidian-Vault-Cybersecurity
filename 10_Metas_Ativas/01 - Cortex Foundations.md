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
- [ ] 