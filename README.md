ANEXO A: README.md

# Blog em node.js

Este é um projeto de Blog

# Pré requisitos

Node.js ( 11.4.1 ) + MySQL + Express + EJS
Npm

# Instalação

1 - Instalar o Nodejs de acordo com o sistema operacional
2 - Clonar este repositório com git clone: https://github.com/DenadaiSenai/Login
3 - Instalar os módulos utilizados pelo aplicativo npm install
4 - Instalar o MySQL e criar o banco de dados (mydb) e executar o arquivo mydb.sql na pasta SQL, no MySQL
Ajuste o usuário e a senha do banco de dados para a conexão do Nodejs, no arquivo 'app.js' (
Login/app.js
// Configurar a conexão com o banco de dados MySQL
const db = mysql.createConnection({
host: 'localhost',
user: 'root',
password: '',
database: 'mydb',
});
)

# Execução e Teste

5 - Executar o aplicativo node app.js
6 – Verificar qual aonde está a porta e executar o Browser
7- Entrar na porta do Local Host
8 - Testar o aplicativo
Windows 10 Education 22H2
XAMPP - v3.3.0 (Apache + MySQL)
Nodejs - v16.16.0
Linux Ubuntu 20.04.6 LTS
MariaDB - v10.3
Nodejs - v18.17.1
Criptografar as senhas no banco de dados
Configurar o banco de dados a usar somente comparação 'BINÁRIA', para evitar o efeito de 'cadastro duplicado'
Criar um campo extra na página de cadastro para verificar a senha antes de realizar a inclusão no banco de dados

# Principais Rotas/Funcionalidades

GET / sobre : Exibe o conteúdo da página “Sobre”  
GET “/” : Página inicial (index.ejs) com links para ‘/ sobre’ e ‘/ info’  
GET / info : Exibe conteúdo da página “Info”  
GET / cadastro : Exibe o formulário de cadastro de usuario  
POST / cadastro : Processa o dados do cadastro. Verifica se o usuário já existe e insere no banco de dados. Redireciona para POST / login ou para GET / register_invalid  
GET / login : Pagina de login de usuário  
POST / login : Valida o usuário com base no username e password. Se valido, cria sessão e redireciona para /dashboard caso incorreto vai para /invalid_login  
GET / logout : Encerra a sessão criada do usuário e redireciona para /. (index.ejs)  
GET / dasboard : Área restrita. Exibe todos usuários cadastrados  
GET / usuários : Renderiza a tabela parcial (usertable.ejs) com todos os users  
GET / register_failed : Mensagem de Erro ou falha no cadastro  
GET / invalid_login : Exibe erro no login

# Autor

Marcio Denadai - Instrutor de Formação Profissional / SENAI 'Celso Charuri' - Sumaré - SP 5.12
