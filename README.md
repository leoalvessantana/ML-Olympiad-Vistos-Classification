# ML Olympiad for Students - TopVistos EUA
Essa é uma competição de Machine Learning, cujo objetivo é prever a aprovação de vistos de trabalho dos EUA.


<div align="center">
<img src="img/topvistos.jpg" width="800px" />
</div>


## 1. Contexto de negócio

As comunidades empresariais nos Estados Unidos enfrentam uma alta demanda por recursos humanos, mas um dos desafios constantes é identificar e atrair o talento certo, que é talvez o elemento mais importante para se manter competitivo. Empresas nos Estados Unidos procuram indivíduos trabalhadores, talentosos e qualificados tanto localmente quanto no exterior.

A Lei de Imigração e Nacionalidade (INA) dos EUA permite que trabalhadores estrangeiros venham trabalhar nos Estados Unidos temporária ou permanentemente. A lei também protege os trabalhadores americanos contra impactos adversos em seus salários ou condições de trabalho, garantindo que os empregadores americanos cumpram os requisitos legais ao contratar trabalhadores estrangeiros para suprir a escassez de mão de obra. Os programas de imigração são administrados pelo Escritório de Certificação de Trabalho Estrangeiro (OFLC).

O OFLC processa pedidos de certificação de emprego para empregadores que buscam trazer trabalhadores estrangeiros para os Estados Unidos e concede certificações nos casos em que os empregadores podem demonstrar que não há trabalhadores americanos suficientes disponíveis para realizar o trabalho com salários que atendam ou excedam o salário pago para a ocupação na área de emprego pretendida.


## 2. Objetivo

No ano fiscal de 2016, o OFLC processou 775.979 pedidos de empregadores para 1.699.957 posições de certificações de trabalho temporárias e permanentes. Isso representou um aumento de nove por cento no número total de pedidos processados em relação ao ano anterior. O processo de revisar cada caso está se tornando uma tarefa tediosa à medida que o número de candidatos aumenta a cada ano.

O aumento do número de candidatos a cada ano demanda uma solução baseada em Aprendizado de Máquina que possa ajudar na pré-seleção dos candidatos com maiores chances de aprovação de VISTO. O OFLC contratou sua empresa, TopVistos, para soluções baseadas em dados. Como Cientista de Dados, você deve analisar os dados fornecidos e, com a ajuda de um modelo de classificação:

* Facilitar o processo de aprovação de vistos.

* Recomendar um perfil adequado para os candidatos para os quais o visto deve ser certificado ou negado, com base nos fatores que influenciam significativamente o status do caso.



## 2. Premissas de Negócio
Para esse problema a métrica de avaliação a ser utilizada deve ser o F1-Score, comumente usado em problemas de classificação, mede a taxa de acertos utilizando as estatísticas de Precisã e Recall.


### 2.1. Descrição dos Dados
O conjunto de dados que representam o contexto está disponível na plataforma do Kaggle. Esse é o link: https://www.kaggle.com/competitions/ml-olympiad-for-students-topvistos-eua/overview. O dataset possui os seguintes atributos:

| Atributo                          | Descrição                                                                                                                                             |
| :-------------------------------- | :---------------------------------------------------------------------------------------------------------------------------------------------------- |
| id_do_caso                        | ID de cada solicitação de visto                                                                                                                       |
| continente                        | Informação do continente do empregado                                                                                                                 |
| educação_do_empregado             | Informação sobre a educação do empregado                                                                                                              |
| tem_experiência_de_trabalho       | O empregado possui alguma experiência de trabalho? S = Sim; N = Não                                                                                   |
| requer_treinamento_de_trabalho    | O empregado requer algum treinamento de trabalho? S = Sim; N = Não                                                                                    |
| num_de_empregados                 | Número de funcionários na empresa do empregador                                                                                                       |
| ano_de_estabelecimento            | Ano em que a empresa do empregador foi estabelecida                                                                                                   |
| região_de_emprego                 | Informação da região de emprego pretendida pelo trabalhador estrangeiro nos EUA.                                                                      |
| salário_prevalecente              | Salário médio pago a trabalhadores em ocupações semelhantes na área de emprego pretendida.                                                            |
| unidade_de_salário                | Unidade do salário prevalecente. Os valores incluem Por Hora, Por Semana, Por Mês e Por Ano.                                                          |
| posição_em_tempo_integral         | A posição de trabalho é em tempo integral? S = Posição em Tempo Integral; N = Posição em Meio Período                                                 |
| status_do_caso                    | Indicador se o visto foi certificado ou negado                                                                                                        |



## 3. Planejamento da solução

Vamos seguir os seguintes passos:


1. **Coleta de Dados:** Esta etapa tem como objetivo realizar a coleta dos dados, no nosso caso acessando a plataforma do Kaggle para download dos arquivos que serão usados.
2. **Limpeza dos Dados:** Esta etapa tem como objetivo remover toda e qualquer sujeira nos dados. Um dado sujo pode ser entendido como um dado que irá atrapalhar a performance final do algoritmo de Machine Learning. Tomando o cuidado entender bem o fenômeno que está sendo estudado para que não sejam removidos dados importantes para a modelagem do problema.
3. **Exploração dos Dados:** Esta etapa tem como objetivo entender os dados e como eles se relacionam entre si. Normalmente, são criadas hipóteses acionáveis de negócio que são posteriormente validadas utilizando técnicas de análise de dados. Além da criação de novas *features* que serão utilizadas na etapa de Modelagem de Dados.
4. **Modelagem dos Dados:** Esta etapa tem como objetivo preparar os dados para que eles sejam utilizados pelos algoritmos de Machine Learning. É nesta etapa que são feitos as transformações e *encodign* dos dados, a fim de facilitar o aprendizado do algoritmo utilizado.
5. **Aplicação de Algoritmos de Machine Learning:** Esta etapa tem como objetivo selecionar e aplicar algoritmos de Machine Learning nos dados preparados nas etapas anteriores. É nesta etapa que são selecionados os algoritmos e feito a comparação de performance entre eles, para selecionar o algoritmos que melhor performou como algoritmo final.
6. **Envio da Solução:** Esta etapa tem como objetivo publicar o algoritmo selecionado, deixando publico e utilizável a solução criada.


## Obervação
Projeto em desenvolvimento. Atualmente estamos na etapa 1.


