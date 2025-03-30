# Estudo-de-casos-Faculdade-simples



/* Lógico_1 Faculdade: */

CREATE TABLE Aluno (
    id_Aluno INT PRIMARY KEY,
    Nome VARCHAR(255),
    CPF VARCHAR(14),
    Endereço VARCHAR(255),
    Telefone VARCHAR(20),
    Email VARCHAR(255),
    Data de nascimento DATE,
    fk_id_Matéria INT
);

CREATE TABLE Curso (
    id_Curso INT PRIMARY KEY,
    Nome VARCHAR(255),
    Duração INT,
    fk_id_Matéria INT
);

CREATE TABLE Matéria (
    id_Matéria INT PRIMARY KEY,
    Nome VARCHAR(255),
    Carga INT,
    fk_id_Curso INT,
    fk_id_Professor INT
);

CREATE TABLE Professor (
    id_Professor INT PRIMARY KEY,
    Nome VARCHAR(255),
    CPF VARCHAR(14),
    Endereço VARCHAR(255),
    Telefone VARCHAR(20),
    Email VARCHAR(255),
    Especialidade  VARCHAR(255)
);

CREATE TABLE Nota (
    id_Nota INT PRIMARY KEY,
    fk_id_Aluno INT,
    Valor_Nota DECIMAL(4,2),
    fk_id_Matéria INT
);
