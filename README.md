"# meu projeto"
 Para criar um sistema de controle de despesas primeiro devemos iniciar um CRUD com o seguinte menu:
 
 -Entrar Despesas:
  Abstract classe Despesas
 atributos: descrição(nome da despesa)
 valor
 data de vencimento
 categoria
 ID da despesa.

 metodos:

 -Anotar Pagamento:
 classe pagamento
 atributo: ID da despesa - para identificar a despesa que deseja pagar 
 data
 valor

 metodos:

 -Listar Despesas: deve separar as em aberto das despesas pagas/ como tambem separar por categoria 
 classe listarAbertas extends Despesas 
 metodo: para editar
 metodo: para excluir

 classe ListarPagas extends Despesas 
 metodo:para editar
 metodo: para excluir

 -Gerenciar Tipos de Despesas
 classe Gerenciar
 metodos: criar/editar/listar/excluir

 -Criar Usuario
 Classe Usuario 
 atributos: nome
 cpf (deve conter um verificador de cpf para nao repetir, nem colocar um cpf inexistente)
 senha (?deve ser criptografada)







