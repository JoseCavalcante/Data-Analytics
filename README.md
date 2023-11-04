<p>O Departamento de Recursos Humanos da IBM-EUA coletou dados de seus funcionários e gostaria de  fazer uma previsão de quais funcionários estão mais propensos a sair de seu emprego.
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
<p>Antes de apresentarmos um Modelo de Machine Learning para que se realize essas previsões, resolvemos fazer algumas percepções sobre os dados apresentados pelo Departamento de Recursos Humanos.</p>
<p>As percepções retiradas se baseiam em cima de 4 categorias principais: <b>Educação</b>, <b>Estado Civil</b>, <b>Departamento</b> e <b>Distância de Casa</b>.</p>
<p>Cada categoria analisada ficará extratificada pelo <b>Gênero</b>, masculino/feminino. Mostrando o total de quem saiu e quem ficou na empresa.</p>
<p>Clique <a href="https://app.powerbi.com/view?r=eyJrIjoiMGY1Zjk1NmMtZWJmZi00NDJhLTg0NWEtYzI4ODcyZDgzMTczIiwidCI6ImZhMDg5NTAxLTRmMzctNDY1ZC1iZGUzLWFmODdlMmJiMWJiYiJ9">aqui</a> para visitar o DashBoard</p>
<p>Variáveis Categóricas da Base Histórica:</p>
<ul>
  <li><b>Educação:</b></li>
    <ul>
      <li>1 Abaixo da faculdade</li>
      <li>2 Faculdade</li>
      <li>3 Bacharelado</li>
      <li>4 Mestre</li>
      <li>5 Doutor</li>
    </ul>
  <li><b>Satisfação Ambiental:</b></li>
    <ul>    
      <li>1 Baixa</li>
      <li>2 Média</li>
      <li>3 Alta</li>
      <li>4 Muito Alta</li>
    </ul>
  <li><b>Envolvimento No Trabalho:</b></li>
    <ul>    
      <li>1 Baixo</li>
      <li>2 Médio</li>
      <li>3 Alto</li>
      <li>4 Muito Alto</li>
    </ul> 
  <li><b>Satisfação No Trabalho:</b></li>
    <ul>    
      <li>1 Baixa</li>
      <li>2 Média</li>
      <li>3 Alta</li>
      <li>4 Muito Alta</li>
    </ul>
  <li><b>Classificação de Desempenho:</b></li>
    <ul>    
      <li>1 Baixo</li>
      <li>2 Médio</li>
      <li>3 Alto</li>
      <li>4 Muito Alto</li>
    </ul>
  <li><b>RelacionamentoSatisfação:</b></li>
    <ul>    
      <li>1 Baixa</li>
      <li>2 Média</li>
      <li>3 Alta</li>
      <li>4 Muito Alta</li>
    </ul>
  <li><b>RelacionamentoSatisfação:</b></li>
    <ul>    
      <li>1 Ruim</li>
      <li>2 Regular</li>
      <li>3 Bom</li>
      <li>4 Muito Bom</li>
    </ul>
</ul>
<p>Dicionário de Variáveis</p>
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
