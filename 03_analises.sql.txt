-- Produtos mais vendidos (valor total)
SELECT
    p.nome_produto,
    SUM(v.quantidade * p.preco) AS total_vendido
FROM vendas v
JOIN produtos p ON v.id_produto = p.id_produto
GROUP BY p.nome_produto
ORDER BY total_vendido DESC;

-- Clientes que mais gastaram
SELECT
    c.nome,
    SUM(v.quantidade * p.preco) AS total_gasto
FROM vendas v
JOIN clientes c ON v.id_cliente = c.id_cliente
JOIN produtos p ON v.id_produto = p.id_produto
GROUP BY c.nome
ORDER BY total_gasto DESC;

-- Faturamento por mês
SELECT
    DATE_TRUNC('month', v.data_venda) AS mes,
    SUM(v.quantidade * p.preco) AS faturamento
FROM vendas v
JOIN produtos p ON v.id_produto = p.id_produto
GROUP BY mes
ORDER BY mes;
