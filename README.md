<p>Neste esudo de caso, eu vou trabalhar com o departamento de recursos humanos de uma empresa.</p>
<p align="justify">O objetivo vai ser prever quais funcionários têm mais tendência de deixar a empresa. Este estudo é importante porque mostra o principal problema das empresas que é realizar a contrtação e manter as telentosas na empresa. O processo de contratação  pode levar muito tempo e é gasto muito dinheiro. Se a empresa possui funcionários talentosos, é preciso manter esses funcionários oferecendo mais beneficios ou outros tipos de bonus. Além de gastos com a contratação ha também gastos com o treinamento.
</p>
<p>Algumas afirmações de pesquisas feitas nas empresas:</p>
<ul>
  <li>Contratar e reter funcionários são tarefas extremamente complexas que exigemm capital, tempo e habilidades.</li>
  <li>Pequenos empresários gastam em torno de 40% das horas de trabalho em tarefas que não geram receitas, como a contratação.</li>
  <li>Empresas gastam de 15% a 20% do salário dos funcionários para recrutar um outro candidato.</li>
  <li>Uma empresa, em média, perde entre 1% a 2,5% de sua receita total no tempo em que leva para treinar um novo funcionário.</li>
  <li>A contratação de um novo funcionário custa, em média, $7,5645.00 em uma empresa com aproximadamente 500 funcionários.</li>
  <li>Demora, em média, 52 dias para um funcionário ocupar sua nova posição.</li>
</ul>
<p align="justify">De posse dessas informações, o Departamento de Recursos Humanos da IBM-EUA coletou dados de seus funcionários e gostaria de  fazer uma previsão de quais funcionários estão mais propensos a sair de seu emprego.
</p>

<p>Alguns exemplos de dados coletados dos funcionários pelo RH:</p>
<ul>
  <li>Envolvimento com o trabalho.</li>
  <li>Escolaridade.</li>
  <li>Satisfação com o trabalho.</li>
  <li>Métricas de desempenho.</li>
  <li>Relacionamento.</li>
  <li>Equilibrio entre as atividades pessoais e profissionais.</li>
</ul>
<p>Para esta simulação, o Cientista de Dados irá receber uma Base de Dados do Departamento de RH para fazer análises e a previsão de quem vai deixar a empresa.</p> 
<p>Algoritmos de classificação utilizado neste estudo:</p>
<ul>
  <li>Regressão Logistica.</li>
  <li>Randon Forest</li>
  <li>Gradient-Boosted</li>
</ul>
<p>Vencedor: <b>Regressão Logistica</b></p>
<ul>
  <li>Accuracy = 0.903153</li>
  <ul>
    <li>Test Error = 0.0968468</li>
  </ul>
</ul>
<p>Variáveis Categoricas:</p>
<ul>
  <li>Educação:</li>
    <ul>
      <li>1 Abaixo da faculdade</li>
      <li>2 Faculdade</li>
      <li>3 Bacharelado</li>
      <li>4 Mestre</li>
      <li>5 Doutor</li>
    </ul>
  <li>Satisfação Ambiental:</li>
    <ul>    
      <li>1 Baixa</li>
      <li>2 Média</li>
      <li>3 Alta</li>
      <li>4 Muito Alta</li>
    </ul>
  <li>Envolvimento No Trabalho:</li>
    <ul>    
      <li>1 Baixo</li>
      <li>2 Médio</li>
      <li>3 Alto</li>
      <li>4 Muito Alto</li>
    </ul> 
  <li>Satisfação No Trabalho:</li>
    <ul>    
      <li>1 Baixa</li>
      <li>2 Média</li>
      <li>3 Alta</li>
      <li>4 Muito Alta</li>
    </ul>
  <li>Classificação de Desempenho:</li>
    <ul>    
      <li>1 Baixo</li>
      <li>2 Médio</li>
      <li>3 Alto</li>
      <li>4 Muito Alto</li>
    </ul>
  <li>RelacionamentoSatisfação:</li>
    <ul>    
      <li>1 Baixa</li>
      <li>2 Média</li>
      <li>3 Alta</li>
      <li>4 Muito Alta</li>
    </ul>
  <li>RelacionamentoSatisfação:</li>
    <ul>    
      <li>1 Ruim
      </li>2 Regular
      <li>3 Bom</li>
      <li>4 Muito Bom</li>
    </ul>
</ul>
<p>Dicionário de Dados:</p>
<table>
  <tr>
    <table>
      <tr><td>Age</td><td>Idade</td></tr>
      <tr><td>Attrition</td><td>Atrito</td></tr>
      <tr><td>BusinessTravel</td><td>Viagem de negócios</td></tr>
      <tr><td>DailyRate</td><td>Diária</td></tr>
      <tr><td>Department</td><td>Departamento</td></tr>
      <tr><td>DistanceFromHome</td><td>Distância de casa</td></tr>
      <tr><td>Education</td><td>Educação</td></tr>
      <tr><td>EducationField</td><td>Campo da educação</td></tr>
      <tr><td>EmployeeCount</td><td>Contagem de funcionários</td></tr>
      <tr><td>EmployeeNumber</td><td>Número de empregados</td></tr>
      <tr><td>EnvironmentSatisfaction</td><td>Satisfação Ambiental</td></tr>
      <tr><td>Gender</td><td>Gênero</td></tr>
      <tr><td>HourlyRate</td><td>Taxa Diária</td></tr>
      <tr><td>JobInvolvement</td><td>Envolvimento no Trabalho</td></tr>
      <tr><td>JobLevel</td><td>Nível de emprego</td></tr>
      <tr><td>JobRole</td><td>Cargo de Trabalho</td></tr>
      <tr><td>JobSatisfaction</td><td>Satisfação no Trabalho</td></tr>
      <tr><td>MaritalStatus</td><td>Estado Civil</td></tr>
      <tr><td>MonthlyIncome</td><td>Renda Mensal</td></tr>
      <tr><td>MonthlyRate</td><td>Taxa Mensal</td></tr>
      <tr><td>NumCompaniesWorked</td><td>Número de companias que trabalhou</td></tr>
      <tr><td>Over18</td><td>Mais de 18 anos</td></tr>
      <tr><td>OverTime</td><td>Ao longo do tempo</td></tr>
      <tr><td>PercentSalaryHike</td><td>Percentual do Salário</td></tr>
      <tr><td>RelationshipSatisfaction</td><td>Satisfação Relacionamento</td></tr>
      <tr><td>StandardHours</td><td>Horas padrão</td></tr>
      <tr><td>StockOptionLevel</td><td>Nível de opção de estoque</td></tr>
      <tr><td>TotalWorkingYears</td><td>Total de anos de trabalho</td></tr>
      <tr><td>TrainingTimesLastYear</td><td>Tempos de treinamento Último ano</td></tr>
      <tr><td>WorkLifeBalance</td><td>WorkLifeBalance</td></tr>
      <tr><td>YarsAtCompany</td><td>Anos Na Empresa</td></tr>
      <tr><td>YearsInCurrentRole</td><td>Anos na função atual</td></tr>
      <tr><td>YearsSinceLastPromotion</td><td>Anos Desde Última Promoção</td></tr>
      <tr><td>YearsWithCurrManager</td><td>Anos na mesma gerência</td></tr>
    </table>
  </tr>
</table>
<p>Bases de dados</p>
<ul>
  <li>Base de dados: https://www.kaggle.com/pavansubhasht/ibm-hr-analytics-attrition-dataset></li>
  <li>Base de dados: https://www.kaggle.com/pavansubhasht/ibm-hr-analytics-attrition-dataset</li>
  <li>Stock: https://www.moneyunder30.com</li>
</ul>
