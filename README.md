# PostgreSQL

## Consultas com SELECT

Selecionando todos os registros da tabela products
Para listar todos os dados da tabela products, utilizei o comando abaixo:

```
SELECT * FROM products;
```


 <details>
  <summary>🎥 Clique aqui para assistir ao vídeo demonstrativo</summary>
   
 https://github.com/user-attachments/assets/ab1800b3-a778-4ff0-beb6-b5c16a03da29
    
</details>


Busquei na tabela products o nome e o preço dos produtos que têm menos de 5 unidades em estoque
```
SELECT product_name, unit_price
FROM products
WHERE units_in_stock < 5;
```
<details>
  <summary>🎥 Clique aqui para assistir ao vídeo demonstrativo</summary>
   


https://github.com/user-attachments/assets/1167e1f5-b82c-42d4-bd8d-dd0090e3f662

</details>


## INNER JOIN
 Retorna apenas as linhas onde há uma correspondência em ambas as tabelas. Abaixo um exemplo com as tabelas suppliers e territories:
 
### Objetivo:
Obter o nome da empresa do fornecedor (company_name) e a descrição do território (territory_description), para todos os fornecedores que têm territórios associados.

```
SELECT suppliers.company_name, territories.territory_description
FROM suppliers
INNER JOIN territories ON suppliers.supplier_id = territories.region_id;
```

<details>
  <summary>🎥 Clique aqui para assistir ao vídeo demonstrativo</summary>
   

https://github.com/user-attachments/assets/f9ec8619-c553-4609-83ea-99eaf9585d16

</details>

## Exemplo de OUTER JOIN
O OUTER JOIN (também conhecido como LEFT OUTER JOIN ou RIGHT OUTER JOIN) retorna todas as linhas de uma tabela e as linhas correspondentes da outra tabela. Se não houver correspondência, o PostgreSQL irá preencher os campos da tabela que não tem correspondência com valores NULL.

### Objetivo:
Obter todos os fornecedores e seus territórios associados, mesmo que não existam territórios associados para alguns fornecedores.

```
SELECT suppliers.company_name, territories.territory_description
FROM suppliers
LEFT OUTER JOIN territories ON suppliers.supplier_id = territories.region_id;
```

<details>
  <summary>🎥 Clique aqui para assistir ao vídeo demonstrativo</summary>
   
https://github.com/user-attachments/assets/e340297f-50cb-440c-8974-762574926974

</details>













