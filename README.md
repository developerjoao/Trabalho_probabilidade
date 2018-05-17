# Trabalho_probabilidade
Repositório para guardar o trabalho de probabilidade com Ivanovitch para a segunda unidade

Endereço para o Vídeo: https://www.youtube.com/watch?v=S7JRnwgpzR0

Análise da Taxa de Aprovação das Disciplinas do IMD - UFRN

Bibliotecas: pandas, matplotlib.pyplot, seaborn e numpy

Inicialmente buscamos dados referentes às turmas, notas, disciplinas e discentes do semestre 2017.2 no banco de dados que nos é disponibilizado pela UFRN.
Armazenamos todas estas informações em variáveis com os mesmos nomes. (turmas, notas, disciplinas e discentes)

Em seguida, fazemos as adaptações necessárias nos dataframes para que ele possa ser utilizado no merge.

Depois, é feito o merge entre os dataframes turmas e disciplinas, utilizamos como base a coluna id_componente(Passo Necessário pois as
turmas estavam com IDs, dessa forma, não sabiamos de quais disciplinas se tratavam as turmas)

Nosso novo dataframe possui dados referentes à todas as turmas, então filtramos, ficando somente com turmas consolidadas do IMD.

Novamente é feito um merge, dessa vez entre os dataframes turmas_imd e docentes, com a coluna id_servidor como base.

Uma vez mais, filtramos somente as turmas do IMD.

Fazemos uma definicao de aprovado, sendo estes tanto os alunos aprovados, quanto os aprovados por nota, e por fim colocamos uma flag nos 
alunos aprovados no semestre 2017.2

Por fim, adicionamos os alunos que estão armazenados como Lato Sensu, Indeferidos, Cancelados ou Excluidos.

Após tratar os dados para o cálculo do percentual de aprovados, fizemos uma tentativa de criar todos os percentuais de uma única vez.
Como não conseguimos desta forma, acabamos fazendo cada disciplina por vez.

Após adquirir a taxa de aprovação de cada disciplina, adicionamos todas as disciplinas, juntamente de sua taxa, à um novo merge, e por fim
imprimimos a informação através de um gráfico de barras, em ordem decrescente de aprovação, com o nome das disciplinas logo abaixo.
