
Sincrona e Assincrona:
	Sincrona
		Resposta imediata (o servico pede uma requisicao, e  espera a resposta para continuar o servico)
		tecnologias comuns: 
			REST usa HTTPS troca de dados em JSON 
			gRPC usa https/2 contratos em protobuf
		Quando Usar
			sincrona em transacoes criticas que precisam de resposta imediata
			assincrona notificacoes, atualizacoes, que podem aparecer depois
	Assincrona
			O servico envia uma mensagem e continua as tarefas
			Tecnologias comuns:
				RabbitMQ, Apache Kafka, Amazon SQS
Gerecenciamento de Dados:
	cada microsservico deve escolher a melhor tecnologia  e  base de dados para a sua funcao 
	Database per Service
		um banco de dados para cada microservico permite melhor evolucao de cada banco, porem dificulta a integracao de dados
	Event Sourcing
		 registra os eventos/caminho que os dados tomaram 
	CQRS
		Separa leitura da Escrita
	Sagas
		Padrao para transacoes
Boas Praticas
	Versionamento de APIs
	Governanca de Eventos(Logs)
	Obseevabilidade
	Resiliencia
	