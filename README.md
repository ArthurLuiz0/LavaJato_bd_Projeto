# LavaJato_bd_Projeto


-- Criando e utilizando o banco de dados
create database LavaJato_bd;
use `lavajato_bd`;
-- Criando tabelas
create table Clientes(
	cliente_id INT AUTO_INCREMENT PRIMARY KEY,
	nome varchar(100) not null,
	telefone varchar(15),
	email varchar(100),
	data_contratacao date not null
);

create table Funcionarios(
    nome_funcionario VARCHAR(100) not null,
    especialidade varchar(50),
    telefone varchar(20),
    email varchar(100)
);

create table Veiculos(
	veiculo_id INT AUTO_INCREMENT PRIMARY KEY,
    numero_chassi int,
    placa int,
    data_consulta DATETIME
);

create table Servicos(
	conserto_id int auto_increment primary key,
    consulta_id int,
	data_pagamento date,
    termino_servico date
);

create table Procedimentos(
	procedimento_id int auto_increment primary key,
    nome VARCHAR(100) not null,
    custo decimal (10,2) not null
);

ALTER TABLE Veiculos
ADD COLUMN consulta_id int,
ADD COLUMN data_pagamento DATETIME,
ADD COLUMN termino_servico DATETIMe,
ADD COLUMN conserto_id int;

INSERT INTO Veiculos (conserto_id, consulta_id, data_pagamento, termino_servico, veiculo_id, numero_chassi, placa, data_consulta) VALUES
	(1, 1, '2024-09-10', '2024-09-15 10:00:00', 101, '1HGBH41JXMN109186', 'ABC-1234', '2024-09-01'),
	(2, 2, '2024-09-11', '2024-09-16 11:00:00', 102, '1HGBH41JXMN109187', 'DEF-5678', '2024-09-02'),
	(3, 3, '2024-09-12', '2024-09-17 12:00:00', 103, '1HGBH41JXMN109188', 'GHI-9012', '2024-09-03'),
	(4, 4, '2024-09-13', '2024-09-18 13:00:00', 104, '1HGBH41JXMN109189', 'JKL-3456', '2024-09-04'),
	(5, 5, '2024-09-14', '2024-09-19 14:00:00', 105, '1HGBH41JXMN109190', 'MNO-7890', '2024-09-05'),
	(6, 6, '2024-09-15', '2024-09-20 15:00:00', 106, '1HGBH41JXMN109191', 'PQR-2345', '2024-09-06'),
	(7, 7, '2024-09-16', '2024-09-21 16:00:00', 107, '1HGBH41JXMN109192', 'STU-6789', '2024-09-07'),
	(8, 8, '2024-09-17', '2024-09-22 17:00:00', 108, '1HGBH41JXMN109193', 'VWX-0123', '2024-09-08'),
	(9, 9, '2024-09-18', '2024-09-23 18:00:00', 109, '1HGBH41JXMN109194', 'YZA-4567', '2024-09-09'),
	(10, 10, '2024-09-19', '2024-09-24 19:00:00', 110, '1HGBH41JXMN109195', 'BCD-8910', '2024-09-10'),
	(11, 11, '2024-09-20', '2024-09-25 20:00:00', 111, '1HGBH41JXMN109196', 'EFG-1230', '2024-09-11'),
	(12, 12, '2024-09-21', '2024-09-26 21:00:00', 112, '1HGBH41JXMN109197', 'HIJ-4561', '2024-09-12'),
	(13, 13, '2024-09-22', '2024-09-27 22:00:00', 113, '1HGBH41JXMN109198', 'KLM-7892', '2024-09-13'),
	(14, 14, '2024-09-23', '2024-09-28 23:00:00', 114, '1HGBH41JXMN109199', 'NOP-0123', '2024-09-14'),
	(15, 15, '2024-09-24', '2024-09-29 08:00:00', 115, '1HGBH41JXMN109200', 'QRS-4567', '2024-09-15'),
	(16, 16, '2024-09-25', '2024-09-30 09:00:00', 116, '1HGBH41JXMN109201', 'TUV-8910', '2024-09-16'),
	(17, 17, '2024-09-26', '2024-10-01 10:00:00', 117, '1HGBH41JXMN109202', 'WXY-1234', '2024-09-17'),
	(18, 18, '2024-09-27', '2024-10-02 11:00:00', 118, '1HGBH41JXMN109203', 'ZAB-5678', '2024-09-18'),
	(19, 19, '2024-09-28', '2024-10-03 12:00:00', 119, '1HGBH41JXMN109204', 'CDE-9012', '2024-09-19'),
	(20, 20, '2024-09-29', '2024-10-04 13:00:00', 120, '1HGBH41JXMN109205', 'FGH-3456', '2024-09-20');



insert into Servicos (conserto_id, consulta_id, data_pagamento, termino_servico) VALUES
	(1,1, '2024-09-10', '10:00:00'),
	(2,2, '2024-09-11', '11:00:00'),
	(3,3, '2024-09-12', '09:00:00'),
	(4,4, '2024-09-13', '14:00:00'),
	(5,5, '2024-09-14', '15:00:00'),
	(6,6, '2024-09-15', '08:00:00'),
	(7,7, '2024-09-16', '13:00:00'),
	(8,8, '2024-09-17', '16:00:00'),
	(9,9, '2024-09-18', '12:00:00'),
	(10,10, '2024-09-19','17:00:00');


INSERT INTO Funcionarios (nome_funcionario, telefone, email) VALUES
	('Carlos Silva', '11987654321', 'carlos@gmail.com'),
	('Maria Oliveira', '11976543210', 'maria@gmail.com'),
	('José Santos', '11965432109', 'jose@gmail.com'),
	('Ana Pereira', '11954321898', 'ana@gmail.com'),
	('Roberto Lima', '11943210987', 'roberto@gmail.com'),
	('Patrícia Costa', '11932109876', 'patricia@gmail.com'),
	('Fernando Almeida', '11921098765', 'fernando@gmail.com'),
	('Juliana Martins', '11910987654', 'juliana@gmail.com'),
	('Renato Sousa', '11909876543', 'renato@gmail.com'),
	('Roberta Ferreira', '11998765432', 'roberta@gmail.com'),
	('Fernanda Ribeiro', '11987654321', 'fernanda@gmail.com'),
	('Marcos Rocha', '11976543210', 'marcos@gmail.com'),
	('Tatiane Almeida', '11965432109', 'tatiane@gmail.com'),
	('Gustavo Mendes', '11954321098', 'gustavo@gmail.com'),
	('Aline Santos', '11943210987', 'aline@gmail.com'),
	('Ricardo Nascimento', '11932109876', 'ricardo@gmail.com'),
	('Daniela Lima', '11921898765', 'daniela@gmail.com'),
	('Leonardo Silva', '11910987654', 'leonardo@gmail.com'),
	('Sofia Costa', '11909876543', 'sofia@gmail.com'),
	('André Martins', '11998765432', 'andre@gmail.com');
    
    
    
INSERT INTO Clientes (nome, telefone, email) VALUES
	('Lucas Almeida', '11900000001', 'lucas@gmail.com'),
	('Fernanda Costa', '11900000002', 'fernanda@gmail.com'),
	('Juliano Silva', '11900000003', 'juliano@gmail.com'),
	('Tatiane Souza', '11900000004', 'tatiane@gmail.com'),
	('Marcelo Santos', '11900000005', 'marcelo@gmail.com'),
	('Carla Dias', '11900000006', 'carla@gmail.com'),
	('Bruno Ferreira', '11900000007', 'bruno@gmail.com'),
	('Patrícia Lima', '11900000008', 'patricia@gmail.com'),
	('André Nascimento', '11900000009', 'andre@gmail.com'),
	('Cláudia Rocha', '11900000010', 'claudia@gmail.com'),
	('Leonardo Almeida', '11900000011', 'leonardo@gmail.com'),
	('Bruna Martins', '11900000012', 'bruna@gmail.com'),
	('Gustavo Ribeiro', '11900000013', 'gustavo@gmail.com'),
	('Eduardo Silva', '11900000014', 'eduardo@gmail.com'),
	('Renata Ferreira', '11900000015', 'renata@gmail.com');
