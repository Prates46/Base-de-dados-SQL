# Base-de-dados-SQL

CREATE TABLE 'senac','agenda'(

    ID INT NOT NULL,

    Nsocial VARCHAR(50) NOT NULL,

    Nome VARCHAR(50) NOT NULL,

    CPF VARCHAR(14) NOT NULL,

    Fone NUMERIC NOT NULL,

    Clientes_RG VARCHAR(15) NOT NULL,

    Clientes_Endereco VARCHAR(50) NOT NULL,

    Clientes_UF VARCHAR(2) NOT NULL,

    Clientes_CEP VARCHAR(9) NOT NULL,

    Clientes_Email VARCHAR(50) NOT NULL,

    Clientes_Genero VARCHAR(30) NOT NULL,

    Clientes_Idade VARCHAR(2) NOT NULL,

    Clientes_Nauralidade VARCHAR(20) NOT NULL,

    Clientes_Ecivil VARCHAR(10) NOT NULL,

    Clientes_Profissao VARCHAR(50) NOT NULL,

    Clientes_Salario DECIMAL NOT NULL,

    Clientes_Formacao VARCHAR(50) NOT NULL ) ENGINE = InnoDB;

 

CREATE TABLE Pedidos (

    Pedidos_ID INT NOT NULL,

    Pedidos_Data DATE NOT NULL,

    Pedidos_Hora TIME NOT NULL,

    Pedidos_CodPedido VARCHAR(8) NOTE NULL,

    Pedidos_Cupom VARCHAR(8) NOT NULL,

    Pedidos_ValCupom DECIMAL NOT NULL,

    Pedidos_IDCliente VARCHAR(50) NOT NULL,

    Pedidos_TotalPedido DECIMAL NOT NULL,

    Pedidos_TipoPag VARCHAR(30) NOT NULL ) ENGINE = InnoDB;

 

CREATE TABLE Produtos (

    Produtos_OBS VARCHAR(50) NOT NULL,

    Produtos_ValCompra DECIMAL( NOT NULL,

    Produtos_Validade DATE NOT NULL,

    Produtos_ValVenda DECIMAL NOT NULL,

    Produtos_ID INT NOT NULL

    Produtos_NF CHAR(50) NOT NULL,

    Produtos_Descricao CHAR(50) NULL,

    Produtos_DeUCompra DATE NOT NULL,

    Produtos_Fornecedor CHAR(30) NULL,

    Produtos_Qtd NUMERIC NOT NULL ) ENGINE = InnoDB);

 

CREATE TABLE ItemPedido (

    ItemPedido_Id INT NOT NULL,

    ItemPedido_IdCodPedido CHAR(8) NOT NULL,

    ItemPedido_IdIDProduto CHAR() NOT NULL,

    ItemPedido_IdValVenda DECIMAL NOT NULL,

    ItemPedido_IdQtd DECIMAL NOT NULL ) ENGINE = InnoDB;);

 

CREATE TABLE Funcionarios (

    Funcionarios_Nome CHAR(30) NOT NULL,

    Funcionarios_CodFunc CHAR(8) NOT NULL,

    Funcionarios_CPF CHAR(14) NOT NULL,

    Funcionarios_RG CHAR(12) NOT NULL,

    Funcionarios_Cargo CHAR(30) NOT NULL,

    Funcionarios_Salario DECIMAL NOT NULL,

    Funcionarios_Dependentes CHAR(10) NOT NULL,

    Funcionarios_DescontarIMP CHAR(10) NOT NULL,

    Funcionarios_DescontarVT BOOLEAN NOT NULL,

    Funcionarios_Convenio BOOLEAN NOT NULL,

    Funcionarios_Horario TIME NOT NULL,

    Funcionarios_Pensao DECIMAL NOT NULL,

    Funcionarios_Ecivil CHAR(10) NOT NULL,

    Funcionarios_DtAdmissao DATE NOT NULL,

    Funcionarios_DtEncerramente DATE NOT NULL ) ENGINE = InnoDB;);

 

CREATE TABLE Estacionamento (

    Estacionamento_ID INT NOT NULL,

    Estacionamento_CodFunc CHAR(8) NOT NULL,

    Estacionamento_PlacaCarro CHAR(8) NOT NULL,

    Estacionamento_Flamula CHAR(8) NOT NULL,

    Estacionamento_Nvaga CHAR(2) NOT NULL ) ENGINE = InnoDB;);

 

CREATE TABLE POSSUI (

    FK_Clientes_ID INT NOT NULL,

    FK_Clientes_Nsocial CHAR(50) NOT NULL,

    FK_Clientes_Nome CHAR(50) NOT NULL,

    FK_Clientes_CPF CHAR(14) NOT NULL,

    FK_Clientes_Clientes_CEP CHAR(9) NOT NULL,

    FK_Clientes_Clientes_Email CHAR(50) NOT NULL,

    FK_Clientes_Clientes_Genero CHAR(20) NOT NULL,

    FK_Clientes_Clientes_Ecivil CHAR(10) NOT NULL,

    FK_Clientes_Clientes_Profissao CHAR(50) NOT NULL,

    FK_Clientes_Clientes_Salario DECIMAL NOT NULL,

    FK_Pedidos_Pedidos_ID CHAR(50) NOT NULL,

    FK_Pedidos_Pedidos_Data DATE NOT NULL,

    FK_Pedidos_Pedidos_Hora TIME NOT NULL,

    FK_Pedidos_Pedidos_CodPedido CHAR(8) NOT NULL,

    FK_Pedidos_Pedidos_Cupom CHAR(8) NOT NULLL,

    FK_Pedidos_Pedidos_ValCupom DECIMAL NOT NULL,

    FK_Pedidos_Pedidos_IDCliente CHAR(10) NOT NULL,

    FK_Pedidos_Pedidos_TotalPedido DECIMAL NOT NULL,

    FK_Pedidos_Pedidos_TipoPag CHAR(20) NOT NULL, ) ENGINE = InnoDB;);

 

CREATE TABLE PossuiPedido (

    fk_Pedidos_Pedidos_ID INT NOT NULL,

    fk_Pedidos_Pedidos_Data DATE NOT NULL,

    fk_Pedidos_Pedidos_Hora TIME NOT NULL,

    fk_Pedidos_Pedidos_CodPedido CHAR(10) NOT NULL,

    fk_Pedidos_Pedidos_Cupom CHAR(10) NOT NULL,

    fk_Pedidos_Pedidos_ValCupom DECIMAL NOT NULL,

    fk_Pedidos_Pedidos_IDCliente CHAR(8) NOT NULL,

    fk_Pedidos_Pedidos_TotalPedido DECIMAL NOT NULL,

    fk_Pedidos_Pedidos_TipoPag CHAR(20) NOT NULL,

    fk_ItemPedido_ItemPedido_Id CHAR(10) NOT NULL,

    fk_ItemPedido_ItemPedido_IdCodPedido CHAR(20) NOT NULL,

    fk_ItemPedido_ItemPedido_IdValVenda DECIMAL NOT NULL,

    fk_ItemPedido_ItemPedido_IdQtd DECIMAL NOT NULL, ) ENGINE = InnoDB;);

 

 
