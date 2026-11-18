Servidores:
	Nuvem(OpEx):
		vc aluga um servidor para vc usar(se dor de cabeça para a manutenção )
		prós: vc paga oque vc usa( nao tem preço fixo ), nao precisa se preocupar com manutenção
		contras: se a internet cai nao tem como usar o servidor 
	Servidor Local(CapEx):
		vc monta seu servidor na sua casa (tendo que cabear toda a casa para conectar no servidor )
Modelos de serviços:
	IaaS( infraestrutura como serviço ):
			o fornecedor gerencia os servidores, armazenamentos e rede
			vc tem que gerenciar: SO, Dados e sua aplicação
			ex: AWS EC2, Microsoft Azure
	PaaS(Plataforma como serviço):
			fornecedor: redes, servers, SO, banco de dados, base
			vc: codigos e dados
			ex: Heroku, Google
	SaaS(Software como serviços):
			fornecedor faz "tudo"
			vc so consome
			ex: netflix, spotify, Gmail
Docker e container
	container é como se fosse uma caixa onde tudo que o software precisa para ser rodado em outra maquina
	vantagens: garante portabilidade
Kubernets:
	como se fosse o gerente dos containers
Cloud Native
	Trabalha usando "todas as maquinas", em seu potencial maximo
	Operando em modo Active-Active
		todas as replicas estão trabalhando
		simultaneamente