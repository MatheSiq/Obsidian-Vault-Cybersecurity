# 📝 Introduction to Cloud Security/Cortex Cloud-Focused Security

**Assunto:** #cortex #fundamentos #cloud #soc 

---

## 📌 Resumo Rápido
A aula vai introduzir cloud security, desde o deploy até os serviços e responsabilidades.

## 🧠 Anotações Principais
- Cloud Security é um conjunto de tecnologias e políticas que devem ser implantadas em ambientes cloud para proteger dados, aplicações e infraestrutura, assim como é feito para ambientes on-premise
- Abaixo estão alguns conceitos utilizados por cloud security:
	- Termos relacionados a implantação
		- Private Cloud
			- Um ambiente de cloud privado se refere a uma cloud presente nos próprios data centers da empresa. Portanto eles são responsáveis pela infraestrutura, cabeamento e proteção física num todo. Além disso são responsáveis por todos os deploys, versionamentos, cibersegurança, etc...
		- Hybrid Cloud
			- Uma composição de dois tipos de nuvem diferentes(Privado e pública por exemplo, mas existem outros tipos também), que são duas nuvens diferentes porém são tratadas como apenas uma no final das contas, devido a tecnologias de portabilidade e sincronização.
		- Public Cloud
			- Uma cloud pública é o que nós conhecemos como uma AWS, GCP, Azure, OCI, etc... Os provedores cuidam de toda parte física, e os contratantes são responsáveis pelas informações, dados, tecnologias, configurações, etc...
	- Termos relacionados a serviços em nuvem.
		- SaaS
			- Um modelo onde um software/aplicação 100% em nuvem é vendido como um serviço para os clientes, tal como um Google Drive.
		- IaaS
			- Modelo onde são vendidos toda a parte de infraestrutura apenas, ficando ao seu critério a forma que ela será utilizada.
		- PaaS
			- Nesse caso é vendido a infraestrutura e softwares para desenvolvimento de outros softwares.
		- Nessa imagem é possível entender melhor a responsabilidade de gerenciamento de cada item relacionado a serviços em nuvem:
		
		![[shared_responsibility_model_png.png]]
- Definições de segurança em nuvem
	- CASB
		- Ferramenta que realizar o intermédio entre o usuário e a aplicação em nuvem, aplicando políticas de segurança diversas para visibilidade, conformidade, proteção contra vazamento de dados, etc...
	- SASE
		- Uma arquitetura que vai combinar ferramentas de acesso seguro, com proteção de rede e cloud
	- FWaaS
		- Firewall as a Service, é a forma de proteger entrada e saída de conexões de rede especificamente para nuvem. São soluções de Firewall(assim como qualquer um), porém para cloud.
	- Cloud Workloader
		- Um conjunto de recursos que trabalham de forma conjunta pra realizar uma determinada tarefa, como exemplo temos VMs, Containers, Serverless, Banco de dados.
	- Container
		- Um "bloco" empacotado que vai conseguir realizar uma tarefa. Ao invés de você baixar uma ferramenta como o "Wazuh" em um servidor e instalar cada uma das partes dele(indexer, dashboar, manager), você pode configurar um container pra cada uma dessas partes, e quando for necessário escalá-lo basta você subir um container semelhante(que é o modelo microserviço)
## 🔑 Conceitos Chave
 - Container
 - SASE
 - CASB
 - SaaS
 - IaaS
 - PaaS
 - Private Cloud
 - Hybrid Cloud
 - Public Cloud
## ❓ Dúvidas / A Pesquisar

# 📝 Cloud Security Concepts, Risks, and Requirements/Cortex Cloud-Focused Security

**Assunto:** #cortex #fundamentos  #cloud #soc 

---

## 📌 Resumo Rápido
Essa aula vai descrever os conceitos, riscos e requisitos relacionados a segurança em nuvem

## 🧠 Anotações Principais
- Usuarios de plataformas cloud não são responsáveis pela segurança da infraestrutura especificamente, porém devem estar cuidando dos seus dados sensíveis para que não vazem, sejam deletados ou se percam.
- Muitos conceitos de segurança em nuvem, em sua grande maioria, são semelhantes a conceitos de segurança de TI em um geral, com alguns ajustes.
- IaaS
	- Um modelo de implantação cloud onde os terceiros(provedores cloud) são responsáveis por fornecer a infraestrutura computacional em um ambiente virtual para que qualquer um na organização possa acessá-los.
	- Benefícios
		- A movimentação para cloud está crescendo muito devido a facilidade de escalar o seu poder computacional e arquitetura em todos os sentidos. Se tem dinheiro, consegue escalar mais e mais.
		- Muitas organizações buscam por IaaS devido a facilidade de replicar arquiteturas on-premise mais familiares em ambientes cloud.
		- Ambientes cloud podem ser bem caros, porém ainda são mais baratos que manter a infraestrutura completa na sua organização, sem falar que podem ofertar possibilidades computacionais que dificilmente seriam possíveis em um ambiente cloud privado, como computação quantica e serviços de satélite.
	- Limitações:
		- Os usuários tem acesso direto a infraestrutura de hardware e rede, por conta disso se tornam usuários privilegiados, e se comprometidos o "estrago" é grande.
		- Os ambientes IaaS são vulneráveis a ataques relacionados a quebra de criptografia, permitindo que atacantes consigam acesso inicial para realizar MITM e roubo de outras credênciais. Tal como adversários podem abusar da infraestrura para rodar botnets, mineração de criptomoedas e lançar DDOS.
	- Devido aos riscos relacionados ao IaaS, sua segurança não deve ser segundo plano e as organizações que a contratam tendem a seguir por um dos dois caminhos abaixo:
		- Depender exclusivamente dos provedores
		- Aumentas consideravelmente a segurança no ambiente.
- PaaS
	- É um modelo de serviço de computação em nuvem que permite organizações alugarem hardware e software por meio da internet para tornar mais rápido o processo de construção de programas e aplicações.
	- Riscos:
		- Desenvolvedores utilizam diversas fontes como Github, guides, etc... Para construir seus códigos, consumindo APIs e outras tecnologias. Porém essas diversas fontes podem estar comprometidas, e consequentemente desenvolvedores podem utilizar códigos com injeções maliciosas, e comprometidos.
		- A visilibade é bem mais limitada, como você não consegue coletar logs do sistema operacional ou kernel, ataques que acontecem em mais baixo nível são impossíveis de serem detectados pela organização.
		- Relacionado ao ponto anterior, devido a baixa visibilidade não é possível detectar movimentações laterareis de adversários com precisão.
		- E ainda atrelado a falta de visibilidade, é extremamente dificil detectar usuários não autorizados que podem estar abusando da infraestrutura para realizar mineração de criptoativos por exemplo.
- Organizações que utilizam IaaS e PaaS em ambientes de desenvolvimento devem possuir uma arquitetura de segurança seguindo abordagens diferentes para cobrir diversos pontos. Abordagens essas como "in-line", "API-Based" e "Host-Based":
	- In-line
	- API-Based
	- Host-Based

## 🔑 Conceitos Chave
- [[Conceito A]]

## ❓ Dúvidas / A Pesquisar
- [ ] O que acontece se...?