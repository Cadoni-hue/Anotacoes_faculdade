CapEx vs OpEx
	CapEx (data center fisico da empresa):
		gasto inicial alto
		compra de hardwate
		Risco Ociosidade de hardware
	OpEx (nuvem de terceiros):
		Continuo por uso
		Paga sobre os dados que usa
		Risco Gastos descontrolados
Ideia de FinOps
	transparencia de valores de custo, otimizar recursos, governança continua
Modelos de precificao da nuvem
	On-Demand
		0% de Desconto
		0 compromisso
		ideal para cargas imprevisiveis(black friday)
	Reserved
		ate 72% de Desconto
		1 a 3 anos de compromisso
		vc compra o hardware para vc por 1 tempo determinado
		ideal para cargas estaveis
	Saving Plans
		ate 70% de desconto
		Gasto por hora
		ideal para cargas estaveis e flexiveis
	Spot
		"leilao"
		ate 90% de Desconto
		maquinas que nao estao sendo usadas 
		pode cair a qualquer hora
		ideal para Batch, CI/CD
Rightsizing
	Ideia de otimizar o custo por instacias
		EX: instacias com <15% de uso = candidata a reducao
	Monitorar metricas de utilizar ao logo do prazo
		monitorar por 2, 3 dias para ver se a algum custo desnecessario
	Compute Optimizer
Maquinas "Zumbis"
	maquinas que ficam ligadas ociosas sem ninguem perceber
	Volumes de Discos nao anexados, HD 
	dependendo da empresa posso desligar a noite ou final de semana
Tagging e alocacao de custo
	tags para cada recurso
		usa tags para cada equipe para saber quanto cada time esta usando
	um relatorio que cada equipe esta usando
Armanezamento e Rede
	tradding OFF
		quanto mais caro, mais rapido vc acessa ele
	a Ideia de quanto tempo voce vai guardar algum dado
	Classes
		Hot(dado com acesso frequente) = Caro
		Coll (acesso Ocacional) = 
		Archive (Raramente acessado) = barato 
	LifeCycle
		movem dados automaticamente
		pode determinar por tempo, para "congelar"
	Egress
		Reduzir com CDN e VPC Endpoints
Ferramentas de Gestao de Custo
	Cost Explorer
	AWS Budgets
	Cost & Usage Reports
	Multi-clouds
		Cloud-Health
		Apptio Cloudability
		Spot.io