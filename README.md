# Sistema de Gerenciamento de Descontos com Java 21

Este projeto é um sistema de gerenciamento de descontos desenvolvido em Java 21, utilizando conceitos modernos da linguagem, como `Records`, `Sealed Classes`, e `Pattern Matching for Switch`. O sistema calcula descontos para diferentes tipos de clientes com base em regras de negócio complexas e validações.

---

## Requisitos do Sistema

### Tipos de Clientes

- **Regular**: Sem desconto.
- **VIP**: 10% de desconto para compras acima de R$ 100,00.
- **Premium**: 20% de desconto para compras acima de R$ 200,00.
- **Gold**: 30% de desconto para compras acima de R$ 500,00, com um limite máximo de R$ 150,00 de desconto.
- **Corporate**: Desconto personalizado com base em contratos (implementado como uma classe selada).

---

### Descontos Progressivos

- Para clientes **Premium** e **Gold**, o desconto aumenta em 5% a cada R$ 100,00 acima do valor inicial (R$ 200,00 para Premium e R$ 500,00 para Gold).

---

### Limites de Desconto

- O desconto máximo para clientes **Gold** é R$ 150,00.
- Para outros clientes, não há limite de desconto.

---

### Bônus de Fidelidade

- Clientes com mais de 2 anos de cadastro ganham um bônus de 5% no desconto.
- Clientes **Corporate** têm um bônus fixo de 10%.

---

### Descontos Personalizados para Clientes Corporate

- Clientes **Corporate** podem ter descontos personalizados com base em contratos específicos.

---

### Validações

- Descontos não se aplicam a compras abaixo de R$ 50,00.
- Descontos não podem ser negativos.

---

## Funcionalidades Implementadas

1. **Cálculo de Descontos**:
   - Descontos são calculados com base no tipo de cliente, valor da compra e tempo de cadastro.
   - Descontos progressivos e limites máximos são aplicados conforme as regras de negócio.

2. **CRUD de Clientes**:
   - Adicionar, remover, atualizar e consultar clientes.
   - Cada cliente possui um ID, nome, tipo e data de cadastro.

3. **Validações de Entrada**:
   - Garantia de que descontos não sejam aplicados a valores abaixo de R$ 50,00.
   - Verificação de que descontos não sejam negativos.

---

## Tecnologias Utilizadas

- **Java 21**:
  - `Records` para imutabilidade.
  - `Sealed Classes` para restringir tipos de clientes.
  - `Pattern Matching for Switch` para simplificar a lógica de descontos.
- **JUnit 5**:
  - Testes unitários com `@ParameterizedTest`, `@RepeatedTest`, `@Tag`, e `assertAll`.
  - Uso de `@BeforeEach`, `@AfterEach`, e `@DisplayName` para organização dos testes.

---

