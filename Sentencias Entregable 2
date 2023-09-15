# bases_de-datos2
CREATE DATABASE Cerveza;
CREATE TABLE categoria (
    -> id_categoria INT PRIMARY KEY AUTO_INCREMENT,
    -> nombre_categoria VARCHAR (255) NOT NULL,
    -> detalle_categoria VARCHAR (255) NOT NULL);

CREATE TABLE cerveza (
    -> id_cerveza INT PRIMARY KEY AUTO_INCREMENT,
    -> nombre_cerveza VARCHAR (255) NOT NULL,
    -> detalle_cerveza VARCHAR (255) NOT NULL,
    -> id_categoria INT NOT NULL,
    -> FOREIGN KEY(id_categoria) REFERENCES categoria(id_categoria)
    -> );

CREATE TABLE materia_prima (
    -> id_materia_prima INT PRIMARY KEY AUTO_INCREMENT,
    -> nombre_materia_prima VARCHAR (255) NOT NULL,
    -> detalle_materia_prima VARCHAR (255) NOT NULL);

CREATE TABLE cerveza_materia_prima (
    -> id_cerveza_materia_prima INT PRIMARY KEY AUTO_INCREMENT,
    -> id_materia_prima INT NOT NULL,
    -> id_cerveza INT NOT NULL,
    -> cantidad_materia_prima DECIMAL(10,2) NOT NULL,
    -> unidad_materia_prima VARCHAR (30) NOT NULL,
    -> FOREIGN KEY (id_materia_prima) REFERENCES materia_prima (id_materia_prima),
    -> FOREIGN KEY (id_cerveza) REFERENCES cerveza (id_cerveza)
    -> );

CREATE TABLE tipo (
    -> id_tipo INT PRIMARY KEY AUTO_INCREMENT,
    -> nombre_tipo VARCHAR (255) NOT NULL);

CREATE TABLE tipo_categoria (
    -> id_tipo_categoria INT PRIMARY KEY AUTO_INCREMENT,
    -> id_tipo INT NOT NULL,
    -> id_categoria INT NOT NULL,
    -> FOREIGN KEY (id_tipo) REFERENCES tipo (id_tipo),
    -> FOREIGN KEY (id_categoria) REFERENCES categoria (id_categoria)
    -> );

// INSERCIÓN DE REGISTROS EN LAS TABLAS.

INSERT INTO categoria (id_categoria, nombre_categoria, detalle_categoria) VALUES
    -> (1, 'Lagers', 'detalle_1'),
    -> (2, 'Ales', 'detalle_2');

INSERT INTO tipo (id_tipo, nombre_tipo) VALUES
    -> (100, 'Dark'),
    -> (101, 'Pale'),
    -> (102, 'Bocks'),
    -> (103, 'Stouts'),
    -> (104, 'Porters'),
    -> (105, 'Belgians'),
    -> (106, 'Sours');

INSERT INTO materia_prima (
    -> id_materia_prima,
    -> nombre_materia_prima,
    -> detalle_materia_prima) VALUES
    -> (200, 'agua', 'detalle_agua'),
    -> (201, 'levadura', 'detalle_levadura'),
    -> (202, 'lúpulo', 'detalle_lupulo'),
    -> (203, 'malta', 'detalle_malta');

INSERT INTO cerveza (id_cerveza, nombre_cerveza, detalle_cerveza, id_categoria)VALUES
    -> (300, 'poker', 'detalle_poker', 1),
    -> (301, 'Aguila', 'detalle_aguila', 2),
    -> (302, 'Light', 'detalle_light', 1),
    -> (303, 'Redds', 'detalle_redds', 2);

INSERT INTO tipo_categoria
    -> (id_tipo_categoria, id_tipo, id_categoria) VALUES
    -> (400, 100, 1),
    -> (401, 101, 1),
    -> (402, 102, 1),
    -> (403, 103, 2),
    -> (404, 104, 2),
    -> (405, 105, 2),
    -> (406, 106, 2),
    -> (407, 101, 2);
