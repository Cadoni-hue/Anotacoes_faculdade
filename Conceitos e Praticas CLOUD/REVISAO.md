VPC(Virtual Private Cloud), VNet(Virtual Network)
	ambiente isolado dentro da infraestrutura do provedor
SubRedes (publica e Privada)
	publica quando gateway contem uma rota para 0.0.0.0/0
	podendo enviar trafego quanto a receber informacoes
	privadas nao tem acesso direto a internet, so utilizando NAT gateway e NAT instaces
gateways e NATgateways
	gatewaway: é a ponte para acesso a internet de forma bidirecional
	nao tem filtragem de trafego
	NATgateways: é uma das formas de conectar com a internet na sub rede privada
Pilares fundamentais:
	Execelencia operacional
	Seguranca
	Confiabilidade
	Eficiencia e Desempenho
	Otimizacao de custo
	Sustentabilidade
Modelos de compra de nuvem
	Sob demanda
	instacias reservadas 
		compromisso de uso continuo por prazo em troca de descontos
	instacias SPOT
		utilizacao ociosa podendo ter interrupcoes a qualquer momento  
Modelos de Nuvem
	Nuvem Privada
		consiste em uso exclusivo para uma unica organizacao
		Controle Total
		Isolamento
		Costumizacao
		Custo Elevado
	Nuvem Publica
		é provisionada de uso publico
		Economia de Escala
		Elasticidade 
		Modelo Opex(pagamento pelo consumo)
		Responsabilidade Compatilhada
		Multilocatorio
	Nuvem Comunitaria
		uso exclusivo para uma comunidade especifica de consumidores pertencentes a organizacoes que compartilham preocupacoes em comuns
		compatilhamento Setorial
			Os custos sao dividos pelas empresas que o usam
		Conformidade padronizada
		Governança colaborativa
			 o infra e gerido pelos membros, ou por uma delegado ou provedor de confiança
	Nuvem Hibrida 
		duas ou mais nuvens distintas
		caracteristicas
			conectividade dedicada:
				conexões dedicadas (AWS Direct Connect, Azure ExpressRoute, Google Cloud Interconnect) ou SD-WAN, utilizando para baixa latencia e alta seguirança
			consistencia operacional
		Cloud bursting
			a mistura da computacao local, com a nuvem publica em momentos de pico 
		Tired Deployment
			Cargas de trabalhos sao distribuidas por camadas (on-premises)
		Disaster  recovery
			caso de falha de site primario. Mantido em  nuvem publica pelo baixo custo
		Modernizaçao gradual
	MultiCloud
		consiste em uma conexao simultanea de dois ou mais provedores de nuvens publicas
		motivacoes para adocao
			reduz a dependencia de um unico provedor
			pode selecionar ferramentas melhores de cada provedor
			 otimizacao de custo
		dificuldades
			complexidade operacional
			custo de transferencia
			consistencia de segurança
			portabilidade de aplicacoes