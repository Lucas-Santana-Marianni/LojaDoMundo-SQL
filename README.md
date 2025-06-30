# 🌍 Loja Do Mundo - Banco de Dados

Este projeto define um banco de dados simples para a loja fictícia **Loja Do Mundo**, especializada em produtos para camping, esportes e sobrevivência.

## 💾 Banco de Dados: `LojaDoMundo`

### 🧾 Tabela: `Produtos`

| Campo       | Tipo           | Descrição                                |
|-------------|----------------|-------------------------------------------|
| id_produto  | INT (PK)       | Identificador único do produto            |
| nome        | VARCHAR(100)   | Nome do produto                           |
| categoria   | VARCHAR(100)   | Categoria (Camping, Sports, etc.)         |
| preco       | DECIMAL(5,2)   | Preço do produto                          |
| quant_estq  | INT            | Quantidade em estoque                     |

## 🧪 Inserção de Dados

```sql
insert into Produtos (id_produto, nome, categoria, preco, quant_estq) values
(1, 'Barraca para 2 Pessoas Coleman', 'Camping', 389.90, 10),
(2, 'Canivete Tático Multifuncional', 'Sobrevivência', 99.00, 25),
(3, 'Kit de Primeiros Socorros Compacto', 'Sobrevivência', 59.90, 30),
(4, 'Garrafa Esportiva 750ml', 'Sports', 39.90, 50),
(5, 'Bola de Futebol Society Topper', 'Sports', 89.99, 20),
(6, 'Garrafa Térmica Invicta 1L', 'Camping', 79.90, 18);

🔄 Alterações e Operações

update Produtos set quant_estq = 20 where id_produto = 1;

update Produtos set preco = 89.99 where id_produto = 2;

delete from Produtos where id_produto = 6;

delete from Produtos where id_produto = 5;

Verificações (SELECT)
select * from Produtos; usado para inspecionar os dados antes e depois das alterações.
