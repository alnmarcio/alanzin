# alanzin
Mano, esse projetinho aqui é um sistema básico feito em Java que salva os dados da rapaziada (tipo nome, CPF, e-mail e tal) num banco de dados MySQL. Perfeito pra quem quer um CRUD sem complicação.

Esse é o cara que dá o start no bagulho todo. Quando tu roda o programa, ele pergunta teu nome, CPF, email, telefone e onde tu mora. Bem de boas, só digitar e apertar Enter.

Essa classe é tipo a identidade da pessoa: ela guarda os dados de cada um (nome, CPF, etc). É tipo um formulário que você preenche.

DAO é só um nome chique pra dizer que esse arquivo conversa com o banco de dados. Ele tem os comandos pra salvar a pessoa no MySQL e também pra listar todo mundo que já foi cadastrado. Manja? Aqui rola o papo reto com o banco.

É quem faz a ponte do nosso sistema com o banco de dados. Se não tiver essa conexão, nada funciona.

O banco que usamos aqui é o MySQL. Antes de rodar o sistema, vc precisa criar ele com o nome `CadastroPessoas` e criar a tabela `registros`. O script pra isso tá assim:



CREATE DATABASE IF NOT EXISTS CadastroPessoas;
USE CadastroPessoas;

CREATE TABLE IF NOT EXISTS registros (
    codigo INT AUTO_INCREMENT PRIMARY KEY,
    nome_completo VARCHAR(100) NOT NULL,
    documento VARCHAR(14) NOT NULL,
    contato_email VARCHAR(100),
    celular VARCHAR(20),
    local_residencia VARCHAR(255)
);



1. Abre tua IDE (tipo NetBeans ou Eclipse).
2. Cria um projeto novo em Java.
3. Joga os arquivos `.java` lá dentro.
4. Garante que teu MySQL tá rodando e com o banco criado.
5. Roda o `Main.java` (que aqui tá com nome de `Main` mesmo).
6. Digita os dados que ele pedir e pronto, já tá no esquema!
