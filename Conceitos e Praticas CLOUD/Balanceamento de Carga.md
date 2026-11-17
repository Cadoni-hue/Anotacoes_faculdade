Load Balancing
	componente que balanceia a carga(podendo aumentar VMs)
	Algoritmos de Distribuicao
			O load Balancing vai utilizar algoritmos para decidir para onde vai cada requisicao
				Round Robin: Distribui por igual as requisicoes entre os targets
					ideal para quando as requisicoes tem custos parecidos
				Least Outstanding Requests:
					envia as requisicoes para o target com menos requicisoes pendentes
					ideal para quando o tempo de cada requisicao varia muito
				Flow Hash:
					utiliza um HASH como parametro para garantir estar na mesma porta
				Random:
					sorteia um target
	Componentes:
			Listener: define a porta 
			Target Group: conjunto de destinos que recebe o trafego
			Health Check: Revisao periodica para ver o estado de cada target
			Rules: condicoes de roteamento
			Security group: controla quais portas podem entrar pelo LB
	Health Checks
			Parametros para cada target
			Protocol: HTTP, HTTPS, TCP, gRPC 
			 Path (HTTP): Endpoint específico para verificação (ex: /health, /status) 
			  Interval: Frequência das verificações (ex: 30 segundos)  Timeout: Tempo máximo de espera por resposta (ex: 5 segundos) 
			  Healthy threshold: Verificações consecutivas bem-sucedidas para considerar healthy (ex: 3) 
			  Unhealthy threshold: Verificações consecutivas falhas para considerar unhealthy (ex: 2) 
			  Success codes: Códigos HTTP aceitos como resposta saudável (ex: 200-299)
Modelos OSI:
	ALB(aplication Load Balancer) Camada 7(https)
		Ideal para aplicaçoes WEB
		compreende os recursos e requicisoes https
	NLB(Network Load Balancer)Camada4 (TCP/UDP/TLS)
		Latencia Baixa
		ideal para integracoes de alta perfomance tipo Jogos
	GWLB(Gateway Load Balancer) Camada 3 (IP)
		ideal para centralizacao de inspecoes de seguranca
CDN (Contend Delivery Network)
	uma rede de servidores posicionadas em centenas de locais geograficos ao redor do mundo denominados pontos de presença ou (PoPs), onde armazenan copias de conteudo para caso o usuario mais proximo pedir.
	Resolve o problema de latencia, ja que o usuario vai receber os arquivos vias um PoPs mais proximo
	OBS: Tipo um Cache
			Tipos de Caches
			Cache HIT:
				usuario solicita requicisao
				o DNS pega o PoPs mais perto e utiliza ele
			Cache MISS
				usuario solicita algo que nao esta no PoPs
				ele pega no servidor a requicisao, e depois guada no PoPs, para outro usuario