# mongodb-commerce

Projeto Commerce em MongoDB!

O Projeto teve como finalidade manipular o banco de dados desenvolvendo uma serie de Querys com diferentes tipos de complexidade.

O banco é composto por dados fictícios do cardápio do McDonalds como ingredientes, valores nutricionais e dados de vendas.

# Instruções da aplicação

### Rodando aplicação com docker

```
git clone git@github.com:Maarceloo/commerce-mongodb.git &&
cd commerce-mongodb &&
npm install &&
docker-compose up -d &&
code .
```

## Observação

<details>
<summary>Utilizando a extensao do mongoDB para VsCode, conecte ao banco na porta 27019</summary>
<br>
![conectando-extensao](https://github.com/Maarceloo/commerce-mongodb/blob/main/img/conectando_extensao.png)

</details>

<details>
<summary>Rode os arquivos "desafios*.mongodb".</summary>
<br>
![rodando-querys](https://github.com/Maarceloo/commerce-mongodb/blob/main/img/rodando_Querys.png)
</details>

<details>
<summary>Estrutura do banco</summary>
<br>

```
[
  {
    "nome": "Big Mac",
    "ingredientes": [
      "hamburguer",
      "alface",
      "queijo",
      "molho especial",
      "cebola",
      "picles",
      "pão com gergelim"
    ],
    "tags": [
      "bovino",
      "pão"
    ],
    "valoresNutricionais": [
      {
        "tipo": "calorias",
        "quantidade": 502,
        "unidadeMedida": "kcal",
        "percentual": 25
      },
      {
        "tipo": "carboidratos",
        "quantidade": 45,
        "unidadeMedida": "gramas",
        "percentual": 15
      },
      {
        "tipo": "sódio",
        "quantidade": 1047,
        "unidadeMedida": "miligramas",
        "percentual": 44
      },
      {
        "tipo": "proteínas",
        "quantidade": 27,
        "unidadeMedida": "gramas",
        "percentual": 36
      },
      {
        "tipo": "lipídios",
        "quantidade": 25,
        "unidadeMedida": "gramas",
        "percentual": 45
      }
    ],
    "descricao": "Não existe nada igual\nDois hambúrgures, alface, queijo, molho especial, cebola e picles num pão com gergelim",
    "curtidas": 145,
    "vendidos": 137
  },
  {
    "nome": "Quarteirão com Queijo",
    "ingredientes": [
      "hamburguer",
      "queijo",
      "cebola",
      "picles",
      "pão com gergelim",
      "ketchup",
      "mostarda"
    ],
    "valoresNutricionais": [
      {
        "tipo": "calorias",
        "quantidade": 528,
        "unidadeMedida": "kcal",
        "percentual": 26
      },
      {
        "tipo": "carboidratos",
        "quantidade": 33,
        "unidadeMedida": "gramas",
        "percentual": 11
      },
      {
        "tipo": "sódio",
        "quantidade": 1072,
        "unidadeMedida": "miligramas",
        "percentual": 35
      },
      {
        "tipo": "proteínas",
        "quantidade": 30,
        "unidadeMedida": "gramas",
        "percentual": 40
      },
      {
        "tipo": "lipídios",
        "quantidade": 31,
        "unidadeMedida": "gramas",
        "percentual": 56
      }
    ],
    "descricao": "Inigualável. Perfeito.\nUm hambúrguer feito com pura carne bovina, envolvida por duas fatias de queijo temperado com ketchup, mostarda, cebola e picles.",
    "curtidas": 13,
    "vendidos": 39
  },
  {
    "nome": "Cheddar McMelt",
    "ingredientes": [
      "hamburguer",
      "queijo cheddar",
      "molho shoyu",
      "cebola grelhada",
      "pão escuro com gergelim"
    ],
    "valoresNutricionais": [
      {
        "tipo": "calorias",
        "quantidade": 468,
        "unidadeMedida": "kcal",
        "percentual": 23
      },
      {
        "tipo": "carboidratos",
        "quantidade": 30,
        "unidadeMedida": "gramas",
        "percentual": 10
      },
      {
        "tipo": "sódio",
        "quantidade": 819,
        "unidadeMedida": "miligramas",
        "percentual": 34
      },
      {
        "tipo": "proteínas",
        "quantidade": 28,
        "unidadeMedida": "gramas",
        "percentual": 37
      },
      {
        "tipo": "lipídios",
        "quantidade": 27,
        "unidadeMedida": "gramas",
        "percentual": 48
      }
    ],
    "descricao": "Sem palavras para descrever.\nFeito com carne bovina, delicioso queijo tipo cheddar derretido, cebola grelhada ao molho shoyu e para completar um pão escuro com gergelim.",
    "curtidas": 36,
    "vendidos": 97
  },
  {
    "nome": "McChicken",
    "ingredientes": [
      "frango empanado",
      "molho suave",
      "alface",
      "pão com gergelim"
    ],
    "valoresNutricionais": [
      {
        "tipo": "calorias",
        "quantidade": 404,
        "unidadeMedida": "kcal",
        "percentual": 20
      },
      {
        "tipo": "carboidratos",
        "quantidade": 36,
        "unidadeMedida": "gramas",
        "percentual": 12
      },
      {
        "tipo": "sódio",
        "quantidade": 718,
        "unidadeMedida": "miligramas",
        "percentual": 24
      },
      {
        "tipo": "proteínas",
        "quantidade": 17,
        "unidadeMedida": "gramas",
        "percentual": 22
      },
      {
        "tipo": "lipídios",
        "quantidade": 22,
        "unidadeMedida": "gramas",
        "percentual": 39
      }
    ],
    "tags": [
      "ave"
    ],
    "descricao": "O sabor que você adora.\nFrango empanado e dourado com molho suave e cremoso, acompanhado de alface crocante num pão com gergelim.",
    "curtidas": 108,
    "vendidos": 85
  },
  {
    "nome": "Extra Chicken",
    "ingredientes": [
      "frango empanado",
      "maionese",
      "alface",
      "pão com gergelim",
      "tomate"
    ],
    "valoresNutricionais": [
      {
        "tipo": "calorias",
        "quantidade": 345,
        "unidadeMedida": "kcal",
        "percentual": 17
      },
      {
        "tipo": "carboidratos",
        "quantidade": 35,
        "unidadeMedida": "gramas",
        "percentual": 12
      },
      {
        "tipo": "sódio",
        "quantidade": 662,
        "unidadeMedida": "miligramas",
        "percentual": 20
      },
      {
        "tipo": "proteínas",
        "quantidade": 13,
        "unidadeMedida": "gramas",
        "percentual": 18
      },
      {
        "tipo": "lipídios",
        "quantidade": 17,
        "unidadeMedida": "gramas",
        "percentual": 29
      }
    ],
    "tags": [
      "ave"
    ],
    "descricao": "Quem ama frango pede.\nPão com gergelim, frango empanado e crocante, alface crespa, tomate fresquinho e a famosa maionese do McDonald's",
    "curtidas": 64,
    "vendidos": 71
  }
]

```

</details>


# Requisitos 

| Requisitos | Descrição |
|---|---|
| `1` | Retorne a quantidade de documentos inseridos na coleção produtos |
| `2` | Ordene a coleção produtos pela quantidade de lanches vendidos em ordem crescente, mostrando apenas o nome e a quantidade de lanches vendidos |
| `3` | Retorne o lanche mais vendido, mostrando apenas o nome e a quantidade do lanche mais vendido |
| `4` | Retorne os lanches que tiveram vendas maiores que 50 e menores que 100, mostrando apenas o nome e a quantidade de lanches vendidos em ordem crescente |
| `5` | Retorne o nome, as curtidas e vendidos dos lanches que tiveram quantidade de curtidas igual a 36 ou tenham a quantidade de vendas igual a 85 |
| `6` | Retorne o nome e as curtidas dos lanches que tiveram curtidas maiores que 10 e menores que 100 |
| `7` | 7 - Retorne o nome e vendidos dos lanches que tenham sido vendidos com uma quantidade diferente de 50 e em que o campo tags não exista |
| `8` | 8 - Delete os lanches com menos de 50 curtidas e retorne o nome dos lanches que restaram no banco |
| `9` | 9 - Retorne o nome de todos os lanches que possuam calorias abaixo de 500 |
| `10` | Retorne o nome de todos os lanches que tenham o percentual de proteínas maior ou igual a 30 e menor ou igual a 40 |
| `11` | Retorne o nome do produto, a quantidade de curtidas e quantos itens foram vendidos dos produtos que não sejam iguais a Big Mac e McChicken |
| `12` | Adicione ketchup aos ingredientes para todos os sanduíches menos o McChicken, garantindo que não haja duplicidade nos ingredientes |
| `13` | Inclua o campo criadoPor em todos os documentos, colocando Ronald McDonald no valor desse campo |
| `14` | Crie uma query que retorne todos os lanches que possuem picles em seus ingredientes e mostre apenas os 3 primeiros itens contidos no array valoresNutricionais |
| `15` | Adicione o campo avaliacao em todos os documentos da coleção e efetue alterações nesse campo |
| `16` | Adicione o campo ultimaModificacao com a data corrente somente no sanduíche Big Mac |
| `17` | Retorne a quantidade total de produtos em uma nova coleção chamada resumoProdutos |
| `18` | Inclua bacon no final da lista de ingredientes dos sanduíches Big Mac e Quarteirão com Queijo |
| `19` | Remova o item cebola de todos os sanduíches |
| `20` | Remova o primeiro ingrediente do sanduíche Quarteirão com Queijo |
| `21` | Remova o último ingrediente do sanduíche Cheddar McMelt |
| `22` | Adicione a quantidade de vendas dos sanduíches por dia da semana |
| `23` | Insira os valores combo e tasty no array tags de todos os sanduíches e aproveite para deixar os valores em ordem alfabética ascendente (A a Z) |
| `24` | Ordene em todos os documentos os valores do array valoresNutricionais pelo campo percentual de forma decrescente |
| `25` | Adicione o valor muito sódio ao final do array tags nos produtos em que o percentual de sódio seja maior ou igual a 40 |
| `26` | Adicione o valor contém sódio ao final do array tags nos produtos em que o percentual de sódio seja maior do que 20 e menor do que 40 |
| `27` | Conte quantos produtos contém Mc no nome, sem considerar letras maiúsculas ou minúsculas |
| `28` | Conte quantos produtos têm 4 ingredientes |
| `29` | Renomeie o campo descricao para descricaoSite em todos os documentos |
| `30` | Remova o campo curtidas do item Big Mac |
| `31` | Retorne o nome dos sanduíches em que o número de curtidas é maior que o número de sanduíches vendidos |
| `32` | Retorne o nome e a quantidade de vendas (vendidos) dos sanduíches em que o número de vendas é múltiplo de 5 |

## Autor 
- [Marcelo De Lima](https://github.com/Maarceloo)
