# Programa-o-Para-Internet---INFO4M
Atividade de Programação para internet

Descrevendo o código do sistema de login, que possui um total de 5 arquivos:

Conexao.php:
Arquivo responsável por fazer a conexão do banco de dados com o PHP, utilizando as variáveis $host, $root, $senha e $database. Caso ocorra algum erro, será exibida a mensagem "Não deu certo fazer a conexão". Se a conexão for estabelecida corretamente, o arquivo index.php poderá realizar o envio dos dados ao banco.

Index.php:
Arquivo principal responsável pelo funcionamento do formulário de login. Quando a conexão estiver estabelecida e os dados cadastrados forem iguais aos dados digitados no formulário de login, o usuário poderá acessar sua conta. Caso os dados não sejam iguais, será exibida uma mensagem de falha ao realizar o login.

Logout.php:
Arquivo responsável por fazer com que o usuário saia da página principal e retorne para a página de login.

Painel.php:
Arquivo referente à página principal, que será exibida quando o login funcionar e o usuário acessar sua conta no site.

Protect.php:
Arquivo responsável por impedir que o usuário acesse a página principal sem ter realizado o login.
