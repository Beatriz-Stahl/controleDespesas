Sistema de controle de despesas - POO

 Para criar um sistema de controle de despesas permitindo gerenciar despesas e pagamentos:
  primeiro devemos iniciar com:
   - CRIAR USUARIO
  classe Usuario : nessa classe iremos utilizar dados para identificar quem esta usando o programa
  atributos: 
  nome ( que sera o login)
  email :(cadastrando o email tornaria possivel notificar quando chegar a data de pagamento da despesa)
  cpf ( para um controle de nao crirar usuarios iguais)
  senha ( de forma criptografada )
  ID
  como metodo podemos colocar um auto incremento para adicionar um ID para cada novo usuario

  -GERENCIAR USUARIO: essa classe ira extender(herdar) de usuario para que possamos ter acesso as informações
  ja cadastradas para assim modificarmos quando solicitado.
  classe Gerenciar extends Usuario 
  metodos: selecionar ID do usuario
  modificar qualquer atributo que esteja em usuario atraves do ID
  listar todos os usuarios criados mostrando nome,email e cpf

  -DESPESA: 
  classe abstrata despesa
descrição(nome da despesa)
 valor (qual o valor da despesa)
 data de vencimento (data limite para ser feito o pagamento)
 categoria ( podemos exemplificar como despesas fixas: aluguel,agua,luz ou despesas variaveis:roupas,entreterimento)
 ID da despesa. ( e criamos um id da despesa para que toda vez que for criado uma nova despesa possa assim mais facil identifica-la)
 como metodo podemos obrigatoriamente colocar um incremento para toda vez q alguem fizer uma nova despesa gerar um id para ela


 
 -ADICIONAR DESPESA:
quando o usuario solicitar adicionar despesa tera um metodo contendo a forma de preencher todos os campos contidos na classe despesa

 -LEMBRETE DE PAGAMENTO : aqui criamos uma classe pagamento e herdamos da classe despesa para que assim seja possivel acessar 
 o id das despesas com deus respectivos data de vencimento e valor. 

 classe pagamento
 atributo: 
 ID da despesa - para identificar a despesa que deseja colocar o lembrete de pagamento
 data de pagamento ( data ja atribuida na despesa para realizar o pagamento)
 valor : o valor que possui na despesa
 email: para enviar a notificação ao usuario

 os metodos são  lembrarpag que ao identificar a data de venc da despesa envie a notificação ao usuario atravez do email


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

 -GERENCIAR TIPOS DE DESPESAS nessa opção o usuario tera total controle sobre todas as depesas podendo entao manipular de acordo com sua necessidade, podendo organizar de acordo com sua categoria  
 criar uma despesa, editar essa despesa criada, excluir despesa escolhida, e listar todas as despesas 
 classe Gerenciar
 metodos: criar/editar/listar/excluir

 









