Sistema de controle de despesas - POO

 Para criar um sistema de controle de despesas permitindo gerenciar despesas e pagamentos:
  primeiro devemos iniciar um CRUD com o seguinte menu:
 
 -ENTRAR DESPESAS:
  criaremos uma classe abstrata(para que dessa forma seja mais generico) com o nome de despesa
  para que posteriormente possa ser herdada para outras classes
podemos definir alguns atributos dessa classe que serao genericos e usados para qualquer tipo de despesa:

 classe abstrata Despesas
atributos:
 descrição(nome da despesa)
 valor (qual o valor da despesa)
 data de vencimento (data limite para ser feito o pagamento)
 categoria ( podemos exemplificar como despesas fixas: aluguel,agua,luz ou despesas variaveis:roupas,entreterimento)
 ID da despesa. ( e criamos um id da despesa para que toda vez que for criado uma nova despesa possa assim mais facil identifica-la)
 
 como metodo podemos obrigatoriamente colocar um incremento para toda vez q alguem fizer uma nova despesa gerar um id para ela

 -ANOTAR PAGAMENTO : aqui criamos uma classe pagamento e herdamos da classe despesa para que assim seja possivel acessar 
 o id das despesas com deus respectivos data de vencimento e valor. 

 classe pagamento
 atributo: ID da despesa - para identificar a despesa que deseja pagar 
 data de pagamento ( data ja atribuida na despesa para realizar o pagamento)
 valor

 como metodo podemos realizar pagamento, o usuario ira utilizar o nome ou o id e o sistema pode fazer uma verificação se é aquela data do pagamento para ser efetuado



 -LISTAR DESPESAS: deve realizar um filtro para despesas pagas/ despesas em aberto, ao mostrar todas as despesas com o filtro de pagas ou nao
 apresentar opçoes para o usuario editar ou excluir o todas as despesas criadas, e opçao de  voltar ao menu principal
 deve conter metodos para mostrar todas as despesas, mostar despesas pagas, despesas pendentes.
 e metodo para manipular a despesa escolhida pelo usuario

 classe listarAbertas extends Despesas 
 metodo: para editar
 metodo: para excluir

 classe ListarPagas extends Despesas 
 metodo:para editar
 metodo: para excluir

 -GERENCIAR TIPOS DE DESPESAS nessa opção o usuario tera total controle sobre todas as depesas podendo entao manipular de acordo com sua necessidade 
 criar uma despesa, editar essa despesa criada, excluir despesa escolhida, e listar todas as despesas 
 classe Gerenciar
 metodos: criar/editar/listar/excluir

 -CRIAR USUARIO uma classe para ser feita a criação de usuarios do controle de despesa. podemos usar o cpf como forma de controle para que nao sejam criados usuarios iguais
 Classe Usuario 
 atributos: nome 
 email :(cadastrando o email tornaria possivel ao agendar o pagamento de uma despesa, depois de paga mostrasse no email uma notificação de confirmação de pagamento)
 cpf (deve conter um verificador de cpf para nao repetir, nem colocar um cpf inexistente)
 senha (deve ser criptografada)

-GERENCIAR USUARIO extends Usuario : atraves dessa classe de gerenciamento de usuarios seja possivel listar usuarios, e editar cadastros
classe gerenciarUsuario
metodos para: cadastrar
editar
listar usuarios existentes










