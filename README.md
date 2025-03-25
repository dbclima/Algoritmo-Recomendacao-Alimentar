# Algebra Linear Algorítmica - Trabalho Final
## Alunos
- [Diogo Lima](http://www.github.com/dbclima)
- [Antônio Pedro Corrêa](https://github.com/AntonioPedro04)


## Descrição
Neste projeto desenvolveremos um software que recebe alimentos e o objetivo  alimentar de um individuo e retorna a dieta ideal do mesmo.

### Dados de entrada:
- Peso [kg]
- Idade [ano]
- Gênero [M/F]
- Lista de preferencia alimentar

### Objetivos alimentares
A quantidade ideal de cada nutriente ingerido por dia:
- **Calorias**:
    - Homens: 2400 [kcal]/dia
    - Mulheres: 2000 [kcal]/dia
    - fonte: https://oglobo.globo.com/saude/noticia/2023/01/quantas-calorias-devo-consumir-por-dia.ghtml

- **Proteína**: 
    - Sem exercício: 1.0 [g/kg]/dia
    - Com exercício: 2.0 [g/kg]/dia
    - Consideraremos 1.5 [g/kg]/dia
    - fonte: https://www.metropoles.com/saude/como-calcular-quantidade-proteina-por-dia

- **Lipídeos (Gordura)**
    - 30% da Caloria diária (ou menos)
    - 1g tem cerca de 9 kcal
    - fonte caloria diária: https://www.who.int/news/item/17-07-2023-who-updates-guidelines-on-fats-and-carbohydrates
    - fonte conversão g -> kcal: https://brasilescola.uol.com.br/curiosidades/contando-calorias.htm#:~:text=Um%20grama%20de%20carboidrato%20oferece,fornece%20cerca%20de%209%20kcal.

- **Colesterol**
    - 10% da caloria diária (ou menos)
    - 22g tem cerca de 200 kcal (9 kcal/g)
    - fonte: https://www.healthline.com/health/high-cholesterol/rda

- **Carboidrato**
    - 4 a 6 [g/kg]/dia
    - Consideraremos 5 [g/kg]/dia
    - fonte: https://www.terra.com.br/vida-e-estilo/quantas-gramas-diarias-de-carboidrato-sao-necessarias-para-hipertrofia-entenda,f5f7ce9ed991948b24cbd30bc1e8f9c6njbq608z.html#:~:text=%22Um%20consumo%20m%C3%A9dio%20de%20carboidratos,g%20de%20carboidratos%20por%20dia.

- **Fibra Alimentar**
    - 2-5 anos: 15 g/dia
    - 6-9 anos: 21 g/dia
    - 10+ anos: 25 g/dia
    - fonte: https://www.who.int/news/item/17-07-2023-who-updates-guidelines-on-fats-and-carbohydrates

- **Cálcio**
    - < 1 ano: 260 mg/dia
    - 1-3 anos: 700 mg/dia
    - 4-8 anos: 1000 mg/dia
    - 9-18 anos: 1300 mg/dia
    - 18-70 anos: 1000 mg/dia
    - 70+ anos: 1200 mg/dia
    - fonte: https://www.unimed.coop.br/viver-bem/alimentacao/qual-a-quantidade-de-calcio-que-o-corpo-precisa-e-como-obte-la

- **Magnésio**
    - < 1 ano: 30 mg/dia
    - 1-3 anos: 75 mg/dia
    - 4-8 anos: 80 mg/dia
    - 9-13 anos: 240 mg/dia
    - 14-18 anos: 
        - homem: 410 mg/dia
        - mulher: 360 mg/dia
    - 19-30 anos: 
        - homem: 400 mg/dia
        - mulher: 310 mg/dia
    - 31+ anos: 
        - homem: 420 mg/dia
        - mulher: 320 mg/dia
    - fonte: https://www.healthline.com/nutrition/magnesium-dosage#supplements

## Dados Utilizados

### Base de alimentos
Os dados refletem as quantidades de nutriente para mais de 300 alimentos.

Fonte de dados: https://www.kaggle.com/datasets/ispangler/composio-nutricional-de-alimentos-taco?select=taco-db-nutrientes.csv

## Projeção Ortogonal
Recebe o vetor Alvo (que contém os dados  referentes à alimentação balanceada) e o vetor que contém os dados dos alimentos escolhidos pelo usuário. Dessa forma, iremos encontrar a projeção do vetor ideal de consumo no subespaço gerado pelos vetores dos alimentos. Essa projeção é a combinação linear do subespaço desses vetores mais próxima possível do vetor ideal de consumo.