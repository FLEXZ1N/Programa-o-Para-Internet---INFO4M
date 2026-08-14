# Programa-o-Para-Internet---INFO4M
Atividade de Programação para internet

Funcionamento do sistema de login

O sistema de login é formado por cinco arquivos PHP, e cada um tem uma função diferente no controle de acesso ao site.

O Conexao.php faz a conexão do PHP com o banco de dados MySQL. Para isso, usa as informações de host, usuário, senha e nome do banco. Caso aconteça algum erro, uma mensagem é exibida avisando que não foi possível realizar a conexão.

O Index.php é onde fica a tela de login. O usuário informa o e-mail e a senha, e o sistema confere esses dados no banco. Se estiver tudo certo, é iniciada uma sessão com session_start() e algumas informações do usuário, como ID e nome, são salvas em $_SESSION. Depois disso, o usuário é levado para o painel.

O Painel.php é a página que o usuário acessa depois de fazer login. Antes de mostrar o conteúdo, ele usa o Protect.php para verificar se existe uma sessão ativa. O nome salvo em $_SESSION['nome'] também pode ser usado para mostrar uma mensagem de boas-vindas ao usuário.

O Protect.php serve justamente para impedir que alguém entre no painel sem fazer login. Ele verifica se existe $_SESSION['id']. Se não existir, o sistema entende que o usuário não está logado e o manda de volta para a página de login.

Já o Logout.php é usado para sair da conta. Ele inicia a sessão e depois usa session_destroy() para encerrá-la. Com isso, os dados que estavam salvos na sessão, como o ID e o nome do usuário, deixam de estar disponíveis. Por fim, o header() envia o usuário novamente para o index.php.

Resumindo, o funcionamento é simples: o usuário faz o login, o sistema verifica os dados no banco e cria uma sessão. Com a sessão ativa, ele consegue acessar o painel. Quando escolhe sair, a sessão é destruída e ele volta para a tela de login.
