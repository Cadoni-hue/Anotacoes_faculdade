# Roadmap: entender sistemas, engenharia de software e arquitetura de software

A ideia é ir do concreto para o abstrato. Arquitetura é difícil de aprender no vácuo: só faz sentido depois que você sentiu a dor de um código mal organizado. Por isso, cada fase combina **estudo + prática**.

> Tempos estimados para ~8–10 h/semana. Os links foram escritos de memória; se algum não abrir, busque pelo nome no Google ou no YouTube.

## Visão geral

| Fase | Tema | Duração estimada |
|------|------|------------------|
| 0 | Fundamentos de computação | 3–4 semanas |
| 1 | Código bem feito | 4–6 semanas |
| 2 | Engenharia de software como processo | 3–4 semanas |
| 3 | Arquitetura de software (núcleo) | 8–12 semanas |
| 4 | System design e sistemas distribuídos | 6–8 semanas |
| 5 | Entender sistemas na prática | contínuo |

---

## Fase 0: Fundamentos de computação (3–4 semanas)

Para entender "como o sistema funciona por baixo".

**Livros e cursos (grátis)**
- [Operating Systems: Three Easy Pieces (OSTEP)](https://pages.cs.wisc.edu/~remzi/OSTEP/): no começo, leia só virtualização e concorrência.
- [Beej's Guide to Network Programming](https://beej.us/guide/bgnet/): redes na prática (TCP, sockets, HTTP).
- [The Missing Semester (MIT)](https://missing.csail.mit.edu/): terminal, Git, debug, ferramentas.
- [CS50 (Harvard)](https://cs50.harvard.edu/x/): fundamentos de computação.

**Vídeos**
- 🇺🇸 [CS50](https://www.youtube.com/@cs50): aulas sobre como a internet funciona e fundamentos.
- 🇺🇸 [Hussein Nasser](https://www.youtube.com/@hnasser): redes, HTTP, bancos de dados e proxies.
- 🇧🇷 [Fábio Akita (Akitando)](https://www.youtube.com/@Akitando): episódios sobre como computadores, redes e a web funcionam.

**Prática**
- Subir um servidor HTTP simples em Python.
- Observar o tráfego com o DevTools do navegador e o `curl`.
- Fazer tudo no WSL.

---

## Fase 1: Código bem feito (4–6 semanas)

A base da engenharia de software.

**Livros e referências**
- [Pro Git](https://git-scm.com/book) (grátis).
- [Refactoring Guru](https://refactoring.guru/): code smells, refatoração e design patterns, grátis e muito visual.
- [Architecture Patterns with Python (Cosmic Python)](https://www.cosmicpython.com/): une Python e arquitetura; serve de ponte para a Fase 3.
- *Refactoring* e *Clean Code* (pagos): existem resumos e palestras gratuitas.

**Vídeos**
- 🇺🇸 [ArjanCodes](https://www.youtube.com/@ArjanCodes): design de software em Python, SOLID, patterns.
- 🇺🇸 [Continuous Delivery (Dave Farley)](https://www.youtube.com/@ContinuousDelivery): engenharia moderna, testes, CI/CD.
- 🇧🇷 [Rodrigo Branas](https://www.youtube.com/@rodrigobranas): Clean Code, TDD e Clean Architecture em português.

**Prática**
- Pegue um projeto seu e escreva testes com `pytest`.
- Refatore aplicando SOLID.
- Observe se os patterns que você aprendeu apareceram naturalmente.

---

## Fase 2: Engenharia de software como processo (3–4 semanas)

Como times produzem software que dura.

**Livros e referências**
- [Software Engineering at Google](https://abseil.io/resources/swe-book) (grátis): testes, code review, escala e cultura.
- [Livros de SRE do Google](https://sre.google/books/) (grátis): confiabilidade e operação.
- [The Twelve-Factor App](https://12factor.net/): curto e muito útil.
- [Blog do Martin Fowler](https://martinfowler.com/): artigos sobre CI, refactoring e testes.

**Vídeos**
- 🇺🇸 [GOTO Conferences](https://www.youtube.com/@GOTOConferences): palestras de Martin Fowler, Kent Beck e outros.
- 🇧🇷 [Full Cycle](https://www.youtube.com/@fullcycle): DevOps, microsserviços, Docker e Kubernetes.

**Prática**
- Configurar CI com GitHub Actions rodando seus testes e linters.

---

## Fase 3: Arquitetura de software (8–12 semanas, o núcleo)

**Conceitos para dominar, nesta ordem**
1. Requisitos funcionais vs. **atributos de qualidade** (escalabilidade, disponibilidade, manutenibilidade etc.) e trade-offs.
2. Arquitetura em camadas, hexagonal (ports and adapters) e Clean Architecture.
3. Monólito modular vs. microsserviços (e quando **não** usar microsserviços).
4. Domain-Driven Design: linguagem ubíqua, bounded contexts, agregados.
5. Comunicação entre serviços: REST, filas, eventos, event-driven.
6. Dados: SQL vs. NoSQL, transações, consistência eventual, cache.
7. Documentar arquitetura: modelo C4 e ADRs (registros de decisão).

**Livros e referências**
- [Architecture Patterns with Python](https://www.cosmicpython.com/): leia inteiro.
- [The Architecture of Open Source Applications](https://aosabook.org/): arquiteturas reais explicadas pelos próprios autores.
- [DDD Reference (Eric Evans)](https://www.domainlanguage.com/ddd/reference/): resumo gratuito do DDD.
- [microservices.io](https://microservices.io/): catálogo de patterns de microsserviços.
- [Azure Architecture Center](https://learn.microsoft.com/azure/architecture/): catálogo de padrões, útil mesmo sem usar a nuvem.
- [AWS Well-Architected](https://aws.amazon.com/architecture/well-architected/)
- [Modelo C4](https://c4model.com/)
- [arc42](https://arc42.org/)
- [ADRs](https://adr.github.io/)

**Livros pagos, se quiser investir depois**
- *Fundamentals of Software Architecture* (Richards & Ford)
- *Designing Data-Intensive Applications* (Kleppmann)
- *Clean Architecture* (Robert C. Martin)

**Vídeos**
- 🇺🇸 [CodeOpinion](https://www.youtube.com/@CodeOpinion): DDD, event-driven, CQRS, em vídeos curtos.
- 🇺🇸 [GOTO Conferences](https://www.youtube.com/@GOTOConferences): Martin Fowler sobre arquitetura e microsserviços; Mark Richards e Neal Ford.
- 🇧🇷 [Full Cycle](https://www.youtube.com/@fullcycle): arquitetura, DDD, microsserviços.
- 🇧🇷 [Rodrigo Branas](https://www.youtube.com/@rodrigobranas): Clean Architecture.

**Prática**
- Pegue um projeto pequeno (por exemplo, seu controle financeiro) e reescreva em camadas/hexagonal.
- Desenhe um diagrama C4.
- Escreva 2–3 ADRs explicando suas decisões.

---

## Fase 4: System design e sistemas distribuídos (6–8 semanas)

Como sistemas grandes funcionam e escalam.

**Livros e referências**
- [The System Design Primer](https://github.com/donnemartin/system-design-primer): ponto de partida clássico e gratuito.
- [Distributed Systems (van Steen)](https://www.distributed-systems.net/): livro gratuito.
- [MIT 6.824](https://pdos.csail.mit.edu/6.824/): avançado, mais pesado.
- *Designing Data-Intensive Applications* (Kleppmann): a referência da área; vale comprar ou pegar em biblioteca.

**Vídeos**
- 🇺🇸 [ByteByteGo](https://www.youtube.com/@ByteByteGo): diagramas claros de sistemas reais.
- 🇺🇸 [Gaurav Sen](https://www.youtube.com/@gkcs): system design em profundidade.
- 🇧🇷 [Full Cycle](https://www.youtube.com/@fullcycle) e palestras de eventos brasileiros (QCon SP, The Developer's Conference).

**Prática**
- Projetar no papel: encurtador de URL, feed de rede social, chat.
- Explicar o raciocínio por escrito ou em voz alta.

---

## Fase 5: Entender sistemas na prática (contínuo)

- Leia o código e a documentação de projetos open source que você usa (Flask, Django, Redis, SQLite). Comece pelo README e pela estrutura de pastas, desenhe a arquitetura e compare com os exemplos do AOSA.
- Leia **post-mortems** de incidentes (busque por "postmortem" em blogs de engenharia): ensinam muito sobre como sistemas falham.
- Escreva um texto curto por mês explicando uma decisão arquitetural. Ensinar é a melhor forma de fixar.

---

## Como estudar sem se perder

1. **Um livro principal por fase**; os outros são consulta.
2. **Prática semanal**: ao terminar um tópico, aplique em código.
3. **Caderno de decisões**: qual problema, quais opções, o que escolheu e por quê. É a habilidade central de arquitetura.
4. **Revisão espaçada**: resumos curtos que você relê a cada poucas semanas.

## Por onde começar

Não abra tudo de uma vez. Comece por **Missing Semester + Refactoring Guru + Cosmic Python**, que se conectam bem com Python e Git, e deixe o resto para quando chegar na fase correspondente.

## Checklist de progresso

- [ ] Fase 0: fundamentos
- [ ] Fase 1: código bem feito
- [ ] Fase 2: engenharia como processo
- [ ] Fase 3: arquitetura
- [ ] Fase 4: system design
- [ ] Fase 5: prática contínua
