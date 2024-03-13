# Projeto_Banco_de_Dados_1

**Tema:** Sistema de Gerenciamento de Escola

Para a idealização do projeto, foi realizado um conjunto de histórias para determinar os requisitos mínimos e os requisitos adicionais. Essas histórias tiveram como inspiração as diversas atividades que estão presentes em escolas reais para a formação do modelo entidade-relacionamento fictício a seguir.

##	Requisitos Mínimos
   
  *	Um conjunto de alunos de uma mesma série formam uma turma.
  *	Aluno tem que ter nome, sobrenome, CPF, data de nascimento, série, e-mail do responsável financeiro, conjunto de matérias com base na série.
  *	Professor tem que ter nome, sobrenome, CPF, data de nascimento, formação, valor recebido por hora aula, disciplinas lecionadas.
  *	Funcionário tem que ter nome, sobrenome, CPF, data de nascimento, salário, função.
  *	Os alunos ao entrarem no colégio ou ao começarem um novo ano tem que fazer a matrícula.
  *	Matrícula tem que ter o nome do responsável (financeiro e pedagógico), valor a pagar, prazo para pagar.
  *	A sala tem que estar disponível para determinada turma.
  
##	Requisitos Adicionais Idealizados

  * Coordenador pedagógico, trabalha em conjunto com o setor de psicologia e professores, responsável por compor o plano de ensino (as disciplinas, horários) e manter uma relação com os alunos e seus familiares.
Dono/Diretor (um ou mais), controlar as finanças, ver projetos ou mudanças para melhoria da escola (mais próximo do setor financeiro), esses projetos eles podem ser sugestões de alunos, funcionários, professores e coordenadores.

  * Mensalidade, precisa enviar um boleto do pagamento para o e-mail do responsável financeiro do aluno.

  * Salários de todos os funcionários, professores, coordenadores, tem são pagos até o quinto dia útil de cada mês.

  * Uma turma precisa ter uma quantidade mínima e máxima de alunos (balanceada), precisa de uma sala com um tamanho adequado.

  * Diferentes tipos de aluno, integral, bolsista, desconto.

  * Professores podem criar projetos de extensão (esportes, robótica, olímpiadas de disciplinas), com prazo de inscrição, nome do projeto, se vai ser online ou presencial.

  * Projetos de extensão de uma disciplina podem ser recomendados para alunos que apresentam notas boas naquela disciplina.

  * Aulas de reforço, pode recomendar aulas de reforço para aqueles alunos com nota abaixo da média, mas qualquer aluno pode frequentar uma aula de reforço, precisa de um horário, sala, disciplina, um estagiário para as aulas. Lista de presença, quem é mais esforçado.

  * Notas dos alunos em cada disciplina, pode usar essas notas no futuro para determinar uma nota média da turma com base em determinada disciplina (se a nota for baixa, podem ver qual é a causa, para tentarem melhorar o aprendizado). Cada professor pode determinar a forma de avaliação, a quantidade de avaliações, se vai ser média ou média ponderada (determinar pesos).  

##	Requisitos Adicionais Aplicados
   
##	Implementação

   Para realizar a implementação, as histórias foram utilizadas para determinar as entidades, os atributos dessas entidades e os relacionamentos. A seguir temos duas listas, uma sobre as entidades e seus respectivos atributos e outra sobre os relacionamentos identificados e explicados de uma forma mais formal.

   * Entidades
     
     *	Aluno
       
     *	Professor
       
     *	Disciplina
       
     *	Matrícula
       
     *	Funcionário
       
     *	Coordenador pedagógico
       
     *	Diretor
       
     *	Projetos de extensão
       
     *	Turma

   * Relacionamentos

   
