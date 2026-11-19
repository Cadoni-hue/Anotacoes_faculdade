 Monitoramento VS Observabilidade
	monitoramento
		Reativo
	observabilidade
		invesatigativo
		ele procura o porque do Erro
Pilares
	Metrica
		Valores numericos que ajudam a medir ao longo do tempo
	Logs
		Registros de eventos discretos
	Traces
		Caminho de uma requisiçao (fica dentro do log)
Ferramentas
	Ditributed Tracing (X-ray)
		Cada segmento = um span
		Conjunto de Spans = um trace 
		Trace ID unico conecta tudo
		Service map ilustra dependencias
Sinais 
	para todos precisa de uma metrica e uma compativo para comparar sel ha uma anomalia
	Latencia 
		o Tempo de resposta 
		tendo um minimo aceitavel ou um padrao
	Trafego
		Demanda do sistema
		quantas requisicoes eu preciso responder por segundo 
		o sistema precisa suportar um minimo
	Erros
		Taxa de Falhas
		o quanto ele falha, tendo um minimo de taxa de erro 
	Saturacao
		Quao cheio esta
		quantidade de uso de uma CPU por exemplo(se da tempo de subir mais uma maquina )
SLIs, SLOs e Error Budgets
	SLI = Indicador medio
		velocidade de internet
	SLO = Meta desejada
		tempo no ar
	SLA Contrato com cliente
		Garantia de estabilidade
Boas Praticas
	Instrumentar desde o inicio
		Quais ferramentas eu irei usar e instrumentar 
	Logs
	Correlacionar
		Comos os tres pilares se relacionam
	Centralizar
		nunca isolar um log
	Definir  SLOs Realistas
		Baseado em como os usuarios utilizaram
	Reduzir Ruido
		Cada alerta deve ser acionavel ( a cada alarme tem que ter uma acao)
	Retencao adequada
		Custo vs auditoria