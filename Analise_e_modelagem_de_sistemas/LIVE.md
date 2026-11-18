Microsservicos
	Cada serviço executa uma responsabilidade
	normalmente divididos por etapas(pedido, estoque, pagamento, notificaçao)
	Tipos de comunicacao
		Sincrona: Solicita e espera, ele espera o retorno do outro servico para continuar o seu servico
		Ferramenta( REST e gRPC)
		Assincrona: Envia e continua, ele manda uma requisicao e continua seu servico sem depender da resposta do outro servico
		Ferramentas(RabbitMQ, KAFKA, Amazon SQS)
	Database Per Service:
		cada microsservico manten sua propria base de dados, escolhendo as melhores funcoes, ferramentas e bancos para o servico
	 Padroes de Dados
		 Event sourcing
			 Registra eventos
		 CQRS
			 Separa operacoes de escrita das operacoes de leitura
		 SAGAS
		 Coordena uma transacao distribuida por etapas
Seguranca por design
	Identificar Ativos
		Quais dados e recursos e precisam de protecao
	Analisar Amaecas
		quais riscos e vetores de ataque existem
	Classificar Dados
		Qual e o nivel de sensibilidade da informacao 
	Definir controles
		quais medidas tecnicas e administraticas aplicar
	CIA(triade de seguranca)
		Confidencialidade(Somente pessoas autorizadas podem acessar tal area)
		Integridade(protecao contra mudancas indevidas)
		Disponibilidade(acessivel quando necessario)
Conformidade e Governanca
	