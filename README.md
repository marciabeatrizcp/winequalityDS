O problema

O problema se refere aos dados de vinhos portugueses "Vinho Verde", que possuem vvariantes de vinho branco e tinto. Devido a questões de privacidade, apenas variáveis físico-químicas (input) e sensoriais (output) estão disponíveis (por exemplo, não há dados sobre tipo de uva, marca do vinho, preço de venda, etc).

Objetivo
  Criar um modelo para estimar a qualidade do vinho.

Informação sobre os atributos
  Variáveis input (baseado em testes físico-químicos):
  Tipo
  Acidez fixa
  Volatilidade da acidez
  Ácido cítrico
  Açúcar residual
  Cloretos
  Dióxido de enxofre livre
  Dióxido de enxofre total
  Densidade
  pH
  Sulfatos
  Álcool
  Variável output (baseado em dado sensorial):
  Qualidade (score entre 0 and 10)
  
Resolução
1. Faça uma análise exploratória para avaliar a consistência dos dados e identificar possíveis variáveis que impactam na qualidade do vinho.

a. Como foi a definição da sua estratégia de modelagem?
  1. Examinei todo o dataset
  2. Encontrei inconsistencias na variavel alcohol
  3. Exclui do dataset as linhas de inconsistencias
  4. Fiz a correção da variáveis com a qualidade
  5. Excolhi 4 variáveis com maior correlação
  6. Escolhi utilizar dois métodos estatísticos para classificação: KNN e Decision Tree
  7. Fiz um teste com a base toda e percebi que a acuracia para os dois métodos era muito baixa
  8. Separei a base em dois conjuntos: Vinhos tinto e branco
  9. Achei a correlação das variaveis para cada conjuntos e identifiquei que eram diferentes, 
  assim as variaveis X seriam diferentes
  10. Para os vinhos tintos considerei as variáveis: Alcohol, volatile aciditily, sulphates e citric acid. 
      As demais variáveis eu tirei do modelo
  11. Para o Método KNN a acurácia foi de: 0.80 e para Decision Tree: 0.42
  12. Para os vinhos Brancos considerei as variáveis: Alcohol, chlorides e volatile aciditily 
      As demais variáveis eu tirei do modelo
  13. Para o Método KNN a acurácia foi de: 0.77 e para Decision Tree: 0.77

b. Como foi definida a função de custo utilizada?
	As 4 variáveis de maior correlaçao com a qualidade

c. Qual foi o critério utilizado na seleção do modelo final?
	 A divisão em dois conjuntos Vinho Tinto e Branco foi muito significativa.Para os dois conjuntos as variáveis de influência 		foram diferentes. 
   
d. Qual foi o critério utilizado para validação do modelo? Por que escolheu utilizar este método? 
	Comparação do variável resposta com o y_pred do modelo.
	O problema apresentado é de classificação e o KNN foi uma boa escolha

e. Quais evidências você possui de que seu modelo é suficientemente bom?
	A matriz de confusão e a acurácia acima de 70%
