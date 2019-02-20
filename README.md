# Prova-Projeto-de-Software
Prova Projeto de Software


Funcionalidades:

- Adição de informações sobre um projeto: implementada na classe Projetos, através do método AddInformações, que pedirá que o 
usuário indique a informação que deseja adicionar, e logo após ele deverá informá-la para que esta possa ser adicionada em seu
atributo específico.

- Remoção de informações sobre um projeto: implementada na classe Projetos, através do método RemoverInformações, que pedirá que o 
usuário indique a informção que deseja remover, e esta logo será removida. Se for um inteiro ele se tornará 0, se for uma 
informação contida num arrayList este será removido do mesmo, o coordenador não poderá ser removido, a não ser que o usuário
informe um substituto, que deverá também ser da classe Professor.

- Adição de informações sobre uma atividade: implementada na classe Atividades, através do método AddInformações, que pedirá que o 
usuário indique a informação que deseja adicionar, e logo após ele deverá informá-la para que esta possa ser adicionada em seu
atributo específico.

- Remoção de informações sobre uma atividade: implementada na classe Atividades, através do método RemoverInformações, o usuário deverá indicar a informação que
deseja remover e esta será excluída, exceto o reponsável pela atividade, nesse caso o usuário deverá informar outro responsável
que o substitua.

- Associação de usuários: implementada na classe Projetos, através do método AssociarUsuario, deverá ser indicado o tipo de usuário, daí deverão ser informados
todos os atributos referentes a este tipo, então o construtor de sua classe vai criar um novo Usuario, que será adicionado
no ArrayList de Usuario, que é um dos atributos da classe Projetos.

- Alteração do status: implementada na classe Projetos, através do métodos alterarStatus, cada projeto se inicia com o 
status “Em processo de criação”, com o método citado, o usuário poderá mudar o status de seu estado inicial para "Iniciado"
caso constem todas as informações básicas. Para alterar o estado para "Em andamento" o projeto deverá está com o status
"Iniciado" e apenas o coordenador poderá realizar esta mudança, assim como para alterar de "Em andamento" para "Finalizado",
apenas o coordenador poderá fazê-lo, e somente se houver descrição do projeto e atividades.

- Consultas: implementada na main, deverá ser indicado que se deseja consultar, usuários, projetos ou atividades.
No caso de projetos e atividades deverá ser informada a identificação, e no caso de usuários, o nome. Daí, uma busca
será realizada, e através de um método toString as informções sobre o que se deseja consultar serão exibidas.

- Relatório: implementada na main, mostrará cada Projeto e suas respectivas informações e atividades, com cada ativida contendo
também suas informações, percorrendo o ArrayList de Projetos através de um método toString.


Classe:

- Projetos:
      
      * Motivação: A necessidade de uma classe que lidasse com os projetos e pudesse gerenciá-los.
      * Solução: Uma classe chamada Projetos, que contém todas as informações básicas de um projeto, como identificação,
      descrição, status, coordenador, entre outros. Possui os métodos addInformações, removerInformações, AssociarUsuário
      e AlterarStatus.
      * Vantagens: A possibilidade de gerenciar todas as informações inerentes a um projeto em apenas uma classe.
      
- Atividades:

      * Motivação: Cada atividade possui uma série de atributos próprios que deveriam ser gerenciados, não haveria outra forma
      de fazer isto a não ser criando uma classe própria para essa finalidade.
      * Solução: Uma classe chamada Atividades, que contém esses atributos necessários a cada atividade, como identificação,
      datas de início e fim, responsável, usuários envolvidos e tarefas. Possui os métodos AddInformações e RemoverInformações.
      * Vantagens: A possibilidade de guardar todas as informações referentes às atividades.
      
- Main:

      * Motivação: A necessidade de uma classe que gerenciasse toda a parte principal do sistema, como as outras classes e seus 
      métodos.
      * Solução: A classe main, contendo o método main, que possuirá um arrayList de Projetos, onde todos estes serão alocados.
      Deverá haver um login, para que se possa gerenciar tudo. Nela haverá o menu de opções com cada funcionalidade, os relatórios
      e consultas serão feitos nela pois é nela que se localiza o ArrayLista de Projetos, que contém todas as informações necessárias
      para a realização destas funcionalidades, nela também haverá o tratamento de exceções, que cobrirá todo o programa.
      * Vantagens: Poder gerenciar todo o sistema através de um menu principal.
      
- Usuario:

      * Motivação: A necessidade de uma classe que contivesse as informações básicas de cada usuário, fosse ele professor, aluno,
      profissional, pesquisador ou técnico.
      * Solução: Uma superclasse abstrata chamada Usuarios, que conterá informações comuns a todos os usuários, como nome, email e cpf, é
      uma superclasse pois assim poderá se evitar a repetição de código, e abstrata para que não se crie nenhum usuário sem tipo específico.
      * Vantagens: Evita a repetição de código através dos conceitos de herança e traz assim um sistema mais limpo e organizado e menos propício a erros.
      
- Aluno:

      * Motivação: A necessidade de uma classe que lidasse com as especificidades dos alunos.
      * Solução: Uma subclasse, que herda conceitos da classe Usuario, e poderá guardar informações referentes aos alunos, como 
      o tipo do aluno, o atributo tipo deverá receber uma string: Graduação, Mestrado ou Doutorado, para que seja especificado o tipo de aluno.
      * Vantagens: Herda atributos e funções de Usuario, evitando a clonagem de código.
      
- Professor:

      * Motivação: A necessidade de uma classe que lidasse com as especificidades dos professores.
      * Solução: Uma subclasse, que herda conceitos da classe Usuario, e poderá guardar informações referentes aos professores,
      uma vez que apenas estes deverão ser capazes de coordenar um projeto.
      * Vantagens: Herda atributos e funções de Usuario, evitando a clonagem de código.
      
- Profissionais:

      * Motivação: A necessidade de uma classe que lidasse com as especificidades dos profissionais.
      * Solução: Uma subclasse, que herda conceitos da classe Usuario, e poderá guardar informações referentes aos profissionais,
      o atributo tipo deverá ser preenchido com Desenvolvedor, Testador ou Analista, o que especificará o tipo de profissional com
      o qual o sistema está lidando.
      * Vantagens: Herda atributos e funções de Usuario, evitando a clonagem de código.
      
- Pesquisador:

      * Motivação: A necessidade de uma classe que lidasse com as especificidades dos pesquisadores.
      * Solução: Uma subclasse, que herda conceitos da classe Usuario, e poderá guardar informações referentes aos pesquisadores.
      * Vantagens: Herda atributos e funções de Usuario, evitando a clonagem de código.      
 
- Tecnico:

      * Motivação: A necessidade de uma classe que lidasse com as especificidades dos usuários tecnicos.
      * Solução: Uma subclasse, que herda conceitos da classe Usuario, e poderá guardar informações referentes aos técnicos.
      * Vantagens: Herda atributos e funções de Usuario, evitando a clonagem de código. 
      

Distribuição dos métodos:

* Motivação: Eram necessários métodos para que fossem cumpridas as funcionalidades requisitadas, como associar usuário,
adicionar e remover informações, e alterar status.
* Solução: 
      - Era necessário que houvesse a adição de informações referentes a projetos e a atividades, por isso foram criados dois
      métodos chamados addInformações, um se localiza na classe Projetos, pois facilitaria a alocação de novas informações
      aos atributos correspondentes a esta classe. Pelas mesmas razões o outro método de mesmo nome se localiza na classe 
      Atividades, pois é mais convenienete de se realizar a adição de informações aos atributos desta.
      - Também era preciso a remoção de informações, funcionalidade contrária à anterior, por isso também foram criados
      dois métodos com o nome removerInformações, um na classe Projetos pois seria mais fácil remover informações dentro da própria
      classe e outro na classe Atividades, pelas mesmas razões.
      - Cada projeto tem sua própria lista de usuários, e por conta disso era mais conveniente de se colocar o método AssociarUsuario
      dentro da classe Projetos, pois criando um novo usuário era mais fácil adicioná-lo à lista de usuário de um projeto já estando
      dentro desse próprio projeto.
      - O método alterarStatus se localiza na classe Projetos, pois é nela que está o atributo status de um projeto, então era a solução
      mais óbvia colocar esta função nessa classe.
*Vantagens: Cada classe tem os métodos necessários apenas a ela, diminuindo a possibilidade de erros.


Herança:

* Motivação: O sistema pede que hajam cinco tipos diferentes de usuários, implementá-los separadamente resultaria na clonagem
de código, dezorganização e aumento do tamanho do programa.
* Solução: Uma superclasse Usuario, com os atributos e métodos comuns a todos os tipos de usuários, e as subclasses 
Aluno, Professor, Tecnico, Pesquisador e Profissionais, que herdam os atributos e métodos da superclasse.
* Vantagens: Diminuição do tamanho do programa, evita a necessidade de implementar os atributos e métodos comuns a todos separadamente.


Tratamento de Exceções:

* Motivação: o menu principal se dará através da leitura de inteiros, uma entrada incorreta e o sistema pararia. Além disso há
outros erros que poderiam ser cometidos pelo usuário do programa.
* Solução: O uso de Exceptions, que seria implementada na main através de try e catch, que pegaria um Exception genérica e exibiria
uma mensagem ao usuário que ocorreu um erro e ele deve tentar novamente, corrigindo tal erro, então ele seria reconduzido ao menu principal.
* Vantagens: Evita que o programa pare com um erro do usuário, e o dá a possibilidade de tentar novamente aquela ação ao invés de recomeçar a execução do sistema desde o início.
* Desvantagens: Por ser implementada na main, o usuário será reconduzido a ela, e não de volta à funcionalidade onde ele se localizará.

Abstrata:

* Motivação: Como há o uso de herança, não se poderia dar ao usuário do sistema a possibilidade de criar um Usuario sem tipo específico,
deveria-se criar um Usuario com tipo Aluno, Professor, Pesquisador, Tecnico ou Profissional.
* Solução: o uso de abstrata, que impede que o usuário do sistema crie um Usuario sem tipo específico, logo ele terá que se voltar a uma das subclasses.
* Vantagens: A solução do problema de um usuário do sistema criar um Usuario sem tipo específico.
      
      
      
