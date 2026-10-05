# OrderHub

![Java](https://img.shields.io/badge/Java-21-orange?logo=openjdk)
![Maven](https://img.shields.io/badge/Build-Maven-blue?logo=apachemaven)
![Status](https://img.shields.io/badge/status-em%20desenvolvimento-yellow)

API de **pedidos e estoque** para uma loja: catálogo de produtos, pedidos, pagamentos e baixa de estoque.

O OrderHub é um projeto de portfólio construído do zero para demonstrar, num domínio realista, as práticas que uso no desenvolvimento backend com Java: modelagem orientada a objetos, testes automatizados, transações, concorrência, segurança e arquitetura em camadas.

---

## Por que este domínio?

Pedidos e estoque parecem simples, mas escondem problemas reais de backend:

- **Regras de negócio que mudam** — descontos, frete e formas de pagamento precisam ser plugáveis.
- **Consistência** — um pedido, seus itens e a baixa de estoque precisam acontecer juntos ou não acontecer.
- **Concorrência** — dois clientes tentando comprar a última unidade ao mesmo tempo.
- **Integração** — eventos de pedido disparando notificações de forma assíncrona e confiável.

## Funcionalidades

| Funcionalidade | Status |
| --- | --- |
| Modelo de domínio (produto, pedido, item, cliente) | 🔜 Planejado |
| Formas de pagamento plugáveis (Pix, cartão, boleto) | 🔜 Planejado |
| Políticas de desconto (cupom, fidelidade, frete grátis) | 🔜 Planejado |
| Persistência em PostgreSQL com migrations | 🔜 Planejado |
| API REST com validação, paginação e erros padronizados | 🔜 Planejado |
| Autenticação JWT com papéis ADMIN e CLIENTE | 🔜 Planejado |
| Controle de estoque seguro sob concorrência | 🔜 Planejado |
| Eventos de pedido via mensageria | 🔜 Planejado |
| Ambiente completo com Docker Compose | 🔜 Planejado |
| Pipeline de CI com testes e cobertura | 🔜 Planejado |

Legenda: ✅ Concluído · 🚧 Em andamento · 🔜 Planejado

## Stack

- **Linguagem:** Java 21
- **Build:** Maven
- **Testes:** JUnit 5, AssertJ
- **Próximas etapas:** Spring Boot, Spring Data JPA, Spring Security, PostgreSQL, Flyway, Testcontainers, RabbitMQ, Docker, GitHub Actions, Angular

## Arquitetura

> Em construção. O núcleo de domínio é escrito em Java puro, sem dependência de framework; o Spring Boot entra depois, como camada de entrada e infraestrutura.

## Como rodar

**Pré-requisitos:** JDK 21 e Maven 3.9+

```bash
git clone https://github.com/SEU-USUARIO/orderhub.git
cd orderhub
mvn clean verify
```

## Roadmap

- [ ] Domínio em Java puro: entidades, objetos de valor, interfaces de pagamento
- [ ] Collections, Streams e exceções de domínio
- [ ] Regras de desconto com Strategy e Java moderno (records, sealed, pattern matching)
- [ ] Cobertura de testes do domínio com TDD
- [ ] Banco PostgreSQL com migrations e queries de relatório
- [ ] API REST com Spring Boot e JPA
- [ ] Segurança com JWT e testes de integração
- [ ] Estoque seguro sob concorrência
- [ ] Arquitetura hexagonal e eventos com RabbitMQ
- [ ] Docker Compose e CI com GitHub Actions
- [ ] Interface web em Angular

## Decisões técnicas

Registro das principais escolhas do projeto e o motivo de cada uma.

| Decisão | Motivo |
| --- | --- |
| Java 21 | Versão LTS atual, com records, sealed classes, pattern matching e virtual threads |
| Domínio sem framework | Mantém as regras de negócio testáveis e independentes de infraestrutura |

## Autor

**João** — Desenvolvedor Java full-stack

[LinkedIn](https://www.linkedin.com/in/SEU-PERFIL) · [GitHub](https://github.com/SEU-USUARIO)
