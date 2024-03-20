# Projeto_Banco_de_Dados_1

**Tema:** Sistema de Gerenciamento de Escola

**Nome:** Heloísa Fernanda Ferreira Jorge

Para a idealização do projeto, foi realizado um conjunto de histórias para determinar os requisitos mínimos e os requisitos adicionais. Essas histórias tiveram como inspiração as diversas atividades que estão presentes em escolas reais para a formação do modelo entidade-relacionamento fictício a seguir.

##	Requisitos Mínimos
   
  *	Um conjunto de alunos de uma mesma série formam uma turma.
  *	Aluno tem que ter nome, sobrenome, número da matrícula, idade, série, conjunto de disciplinas com base na série e gênero.
  *	Professor tem que ter nome, sobrenome, CPF, idade, gênero, formação, valor recebido por hora aula, disciplinas lecionadas.
  *	Funcionário tem que ter nome, sobrenome, CPF, idade, gênero, salário, função.
  *	Matrícula tem que ter as informações do responsável (financeiro e pedagógico), valor a pagar, prazo para pagar.
  *	Uma sala tem que estar disponível para determinada turma.
  
##	Requisitos Adicionais Idealizados

  * O coordenador pedagógico, trabalha em conjunto com o setor de psicologia e professores, responsável por compor o plano de ensino (as disciplinas, horários). O coordenador pedagógico foi adicionado ao modelo, porém não se encaixava um setor de psicologia ao modelo conceitual. E a relação da criação do plano de ensino não se mostrou algo essencial na criação do modelo e para disciplina, por isso não foi adicionado. A motivação para a adição desses dados ao modelo era o de representar a atuação do coordenador pedagógico na escola.
    
  * Dono/Diretor (um ou mais), controlar as finanças, ver projetos ou mudanças para melhoria da escola (mais próximo do setor financeiro), esses projetos eles podem ser sugestões de alunos, funcionários, professores e coordenadores. A principal motivação foi a criação do sistema de sugestões, porém este não se mostrou necessário ao banco de dados e sem esse sistema não havia uma necessidade clara de colocar o dono no modelo.

  * Mensalidade, precisa enviar um boleto do pagamento para o e-mail do responsável financeiro do aluno. Esse tipo de funcionalidade não é adicionado em um modelo entidade-relacionamento, porém é uma forma de usar os dados do banco de dados. A motivação para a criação dessa funcionalidade era a de ajudar os responsáveis dos alunos. 

  * Salários de todos os funcionários, professores, coordenadores, tem são pagos até o quinto dia útil de cada mês. A motivação seria a adição de um lembrete ao dono sobre isso, porém isso não se encaixaria em um banco de dados.

  * Projetos de extensão de uma disciplina podem ser recomendados para alunos que apresentam notas boas naquela disciplina. Os projetos de extensão foram adicionados ao modelo conceitual, mas como o objetivo do sistema de recomendação é ser uma possível aplicação dos dados, este não precisaria estar no modelo.

  * Recomendar aulas de reforço para aqueles alunos com nota abaixo da média. A motivação foi estimular os alunos que estão com nota baixa a irem ao reforço. Esse tipo de funcionalidade não é colocado em um modelo entidade-relacionamento, mas demonstra um possível uso dos dados de um banco de dados.

  * Usar as notas dos alunos no futuro para determinar uma nota média da turma com base em determinada disciplina (se a nota for baixa, podem ver qual é a causa, para tentarem melhorar o aprendizado). Cada professor pode determinar a forma de avaliação, a quantidade de avaliações, se vai ser média ou média ponderada (determinar pesos). A motivação para adição dessas funcionalidades seria proporcionar uma forma de cálculo das notas e de estatísticas sobre essas notas, porém esse tipo de dados não se encaixava em um modelo entidade-relacionamento.

##	Requisitos Adicionais Aplicados

   * Adicionar as notas dos alunos em cada disciplina ao banco de dados, com objetivo de conseguir localizar e organizar as notas de cada um dos alunos.

   * Uma turma precisa ter uma quantidade mínima e máxima de alunos e de uma sala que não esteja ocupada. A motivação para adicionar turma ao banco de dados é poder verificar quais alunos estão presentes em determinada turma.

   * Apresentar a opção de diversos planos de pagamento, como: plano anual, semestral e mensalidade. Além disso essas opções de pagamento ficam disponíveis para os responsáveis no momento de criação da matrícula. A principal razão para adição de planos de pagamento é organizar as finanças da escola.

   * Professores podem criar projetos de extensão (esportes, robótica, olímpiadas de disciplinas), com prazo de inscrição, nome do projeto, se vai ser online ou presencial. O objetivo da adição dos projetos de extensão ao banco de dados é o seu uso futuro na funcionalidade de recomendação de projetos de extensão com base na nota.

   * Alunos podem frequentar aulas de reforço. Essas aulas precisam de um horário, uma sala, uma disciplina, um estagiário e uma lista de presença para os alunos que frequentarem as aulas de reforço. A motivação para a adição de aulas de reforço foram as possíveis aplicações desses dados em um banco de dados, como exemplo, recomendar aulas de reforço para alunos que apresentam dificuldades em uma disciplina.

   * Lista de presença dos alunos de uma turma para uma disciplina. O objetivo da lista é conseguir mapear os alunos que compareceram as aulas da sua turma ou de reforço e assim conseguir mapear a quantidade faltas.

   * Atividades extracurriculares para os alunos, essas atividades têm determinado conjunto de horários e custo. Atividades curriculares foram adicionadas ao projeto, pois são muito comuns no ambiente escolar.

   * Uma sala de aula pode apresentar mais de um tipo, pois pode ser um laboratório por exemplo. As salas elas apresentam um tamanho e um nome, este a diferencia das demais salas. A motivação para a adição de salas foi o de proporcionar um controle sobre as salas ocupadas e não ocupadas, a partir de um banco de dados.

   * Um coordenador pedagógico é responsável por manter uma relação com o responsável pedagógico de seus alunos. A principal motivação para a adição do coordenador pedagógico, foi a presença de um no colégio em que eu estudava.
   
##	Implementação

   Para realizar a implementação, as histórias foram utilizadas para determinar as entidades, os atributos dessas entidades e os relacionamentos. A seguir temos duas listas, uma sobre as entidades e seus respectivos atributos e outra sobre os relacionamentos identificados.

   * Entidades
     
     *	Aluno (num_matricula, série, p_nome, sobrenome, gênero, idade)
       
     *	Professor (valor_hora, formação, CPF, p_nome, sobrenome, gênero, idade)
       
     *	Disciplina (nome_disc, ementa, série)
       
     *	Matrícula (prazo, ano, valor_pag)
       
     *	Funcionário (CPF, função, salário, p_nome, sobrenome, gênero, idade)
       
     *	Coordenador pedagógico (conj_séries, CPF, p_nome, sobrenome, gênero, idade)
    
     *	Projetos de extensão (ID, online_ou_pres, horários, nome_projeto, prazo_inscr)
       
     *	Planos de Pagamento (prazo, forma_pag, valor_mensal, valor_semes, valor_anual)
       
     *	Turma (quant_alunos, nome_turma, turno)
    
     *	Sala (tipo, tamanho, nome_sala)
    
     *	Aula de Reforço (ID, horários)
    
     *	Atividade Extracurricular (ID, nome_ativ, horários, custo)
    
     *	Estagiário (valor_hora, formação, nome_uni, CPF, p_nome, sobrenome, gênero, idade)
    
     *	Lista de Presença (nome_turma, nome_disc, reforço, data_da_lista, alunos_presentes)
    
     *	Pessoa (p_nome, sobrenome, gênero, idade)

   * Relacionamentos

        Os relacionamentos a seguir foram organizados segundo a maneira como deveriam ser lidos no diagrama e mostrando as duas (ou mais, no caso de relacionamentos ternários) formas de leitura da relação existente entre as entidades.

     *   Um professor leciona uma ou mais atividades extracurriculares. Uma atividade extracurricular é lecionada por um professor.
    
     *   Um professor pode criar muitos projetos de extensão. Um projeto de extensão é criado por um professor.
    
     *   Um professor leciona uma ou mais disciplinas para uma ou mais turmas. Uma disciplina é lecionada para uma ou mais turmas, por um ou mais professores. Uma turma apresenta uma ou mais disciplinas que são lecionadas por um ou mais professores.
    
     *   Um aluno pode participar de muitas atividades extracurriculares. Uma atividade extracurricular precisa de um ou mais alunos.
    
     *   Um aluno pode participar de muitos projetos de extensão. Um projeto de extensão precisa da participação de um ou mais alunos.
    
     *   Um aluno pode participar de muitas aulas de reforço. Uma aula de reforço precisa de participação de um ou mais alunos.
    
     *   Um aluno está ligado a uma ou mais disciplinas, e um aluno apresenta uma nota para cada disciplina. Uma disciplina está ligada a um ou mais alunos.
    
     *   Uma aula de reforço ensina o assunto de uma disciplina, sendo ministrada por um ou dois estagiários. Um estagiário ensina o assunto de uma disciplina em uma ou mais aulas de reforço. O assunto de uma disciplina é ensinado em uma ou mais aulas de reforço por um ou dois estagiários.
    
     *   Uma aula de reforço possui uma lista de presença. Uma lista de presença está presente em muitas aulas de reforço.
    
     *   Uma turma possui uma lista de presença. Uma lista de presença está presente em muitas turmas.
    
     *   Uma turma ocupa uma sala se esta não estiver ocupada. Uma sala pode ser ocupada por uma turma, se esta sala não estiver ocupada.
    
     *   Uma aula de reforço ocupa uma sala se esta não estiver ocupada. Uma sala pode ser ocupada por uma aula de reforço, se esta sala não estiver ocupada.
    
     *   Um aluno faz parte de uma turma. Uma turma tem muitos alunos, de acordo com os limites mínimo e máximo para a criação de uma turma.
    
     *   Uma matrícula adiciona um aluno ao sistema caso a matrícula for paga e o aluno não estiver presente no sistema. Um aluno é adicionado no sistema caso a matrícula esteja paga e o aluno não esteja no sistema.
    
     *   Em uma matrícula é definido um plano de pagamento.  Um plano de pagamento é definido em uma ou mais matrículas.
    
     *   Uma matrícula precisa de um ou dois responsáveis (responsável financeiro e pedagógico, pode ser uma pessoa ou duas). Um responsável é necessário para uma ou mais matrículas.
    
     *   Um aluno depende de um ou dois responsáveis. Um responsável ele tem como dependentes um ou mais alunos.
    
     *   Um responsável está ligado a um coordenador pedagógico. Um coordenador pedagógico está ligado a muitos responsáveis.

   
