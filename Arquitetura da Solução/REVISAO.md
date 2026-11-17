Camadas:
	UI/Apresentação:
		aquillo que o usuario vê exemplo botoes
	Negocio/ bussines layer:
		onde é calculado as regras, aquilo q vc nao pode e pode
	Dados/ banco de Dados:
		onde ficam guardados as informações do sistema
Cliente-Servidor:
	como os sistemas se comportam junto com o cliente
		Tiers 2,3 e N
		Tier 2: a Camada de Apresentação e Negocios estao juntas
		pode acabar gerando gargalo quando a maquina nao for muito forte, se precisar mudar de regra precisa mudar de todas
	Tier: 3 
		O recomendado nos dias atuais, um servidor para cada camada 
	Tier N:
	4 Tiers ou mais
	Tipos de usuarios:
		Thin clients:
		clientes que demandam menos do sistema, fazem menos requisições para o banco de dados
		Thick clients:
		Clientes que demandam mais do sistema, fazem varias requiçoes seguidas, podendo gerar gargalo
Tipos de organizações de sistemas
	Monolito:
	o sistema é montado em um unico codigo
	bom no inicio por ser mais facil, ruim para manunteção
	Por Função:
	Cada codigo tem sua função
	bom pq nao é dependente de outros codigos(exemplo: se o codigo de login cair, nao intefere no codigo de compra) ruim: se o banco de dados cair o sistema inteiro cai
	Microsserviços:
	Cada Codigo tem sua nuvem, deixando cada area independente e podendo escalar a mesma cada vez mais
	Ruim: Alta complexidade
Comunicações assincrona e sincrona
	Assincrona: enquanto a requisição é pedida o sistema continua trabalhando(bom pq o usuario nao fica sem "ver nada", ruim pq o usuario pode ver alguma informação desatualizada)
	Sincrona: o sistema processa primeiro para te enviar
Onde guardar os arquivos
	Arquivos Simples:
	pastas fisicas com documentos soltos
	SGBDs: arquivos com etiquetadas e acesso rapido onde o sistema monitora a segurança
	ACID:
		A: Atomicidade Tudo ou Nada
		C: Consistencia: o banco deve respeitar todas as regras de integridade do sistema 
		 I: isolamento feitas de forma sequencial, que parecem simultanea
		 D: Durabilidade: Uma vez confirmado ele ja é guardado quase que instantaneamente 
	SQL: Baseiase em guardar dados em tabelas, onde elas se relacionam
	NoSQL