INSERT INTO clientes (nome, email, cidade) VALUES
('Ana Silva', 'ana@email.com', 'São Paulo'),
('Carlos Souza', 'carlos@email.com', 'Rio de Janeiro'),
('Mariana Lima', 'mariana@email.com', 'Belo Horizonte');

INSERT INTO produtos (nome_produto, categoria, preco) VALUES
('Notebook', 'Eletrônicos', 3500.00),
('Mouse', 'Eletrônicos', 80.00),
('Teclado', 'Eletrônicos', 150.00);

INSERT INTO vendas (id_cliente, id_produto, data_venda, quantidade) VALUES
(1, 1, '2024-01-10', 1),
(2, 2, '2024-01-15', 2),
(1, 3, '2024-02-05', 1),
(3, 1, '2024-02-20', 1);
