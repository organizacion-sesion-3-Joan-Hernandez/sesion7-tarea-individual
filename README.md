# sesion7-tarea-individual
---------------------------------------------------------------------------------------------------------------------------
EJERCICIO 1
---------------------------------------------------------------------------------------------------------------------------
CREATE TABLE ALUMNOS (
NIF VARCHAR(9) CONSTRAINT ALU_NIF_PK PRIMARY KEY,
Nombre VARCHAR(50),
Apellido1 VARCHAR(50),
Apellido2 VARCHAR(50),
Direccion VARCHAR(200),
Sexo VARCHAR(1) CONSTRAINT ALU_SEX_CK CHECK (Sexo in ('M','H')),
FechaNacimiento DATE,
CodigoCurso VARCHAR(10) NOT NULL CONSTRAINT ALU_COD_FK REFERENCES
CURSOS );
CREATE TABLE CURSOS (
Codigo VARCHAR(10) CONSTRAINT CUR_COD_PK PRIMARY KEY,
Nombre VARCHAR(50) UNIQUE,
NIFProfesor VARCHAR(9),
MaximoAlumnos NUMBER(2),
FechaInicio DATE,
FechaFin DATE,
Horas NUMBER(4) NOT NULL,
CONSTRAINT CK_CUR_FEC CHECK (FechaInicio < FechaFin) );
CREATE TABLE PROFESORES (
NIF VARCHAR(9) CONSTRAINT PRO_NIF_PK PRIMARY KEY,
Nombre VARCHAR(50) UNIQUE,
Apellido1 VARCHAR(50),
Apellido2 VARCHAR(50),
Direccion VARCHAR(200),
Titulacion VARCHAR(80),
Salario NUMBER(6) NOT NULL );
---------------------------------------------------------------------------------------------------------------------------
EJERCICIO2
---------------------------------------------------------------------------------------------------------------------------
Crea un nuevo atributo llamado Edad de tipo numérico a la tabla ALUMNOS.
ALTER TABLE ALUMNOS ADD (Edad NUMBER(3));
Modifica el campo que has creado anteriormente para que la edad del alumno o alumna esté
comprendida entre 14 y 65 años.
ALTER TABLE ALUMNOS ADD CONSTRAINT CK_ALU_EDA CHECK (Edad Between 14 And
65);
Modifica el campo Número de horas del CURSO de manera que solo pueda haber cursos con 30,
40 o 60 horas.
ALTER TABLE CURSOS ADD CONSTRAINT CK_CUR_HOR CHECK (Horas In (30,40,60));
No podemos añadir un curso si su número máximo de alumnos es inferior a 15.
ALTER TABLE CURSOS ADD CONSTRAINT CK_CUR_MAX CHECK (MaximoAlumnos >= 15);
Elimina la restricción que controla los valores que puede tomar el atributo Sexo.
ALTER TABLE ALUMNOS DROP CONSTRAINT ALU_SEX_CK;
Elimina la columna Dirección de la tabla PROFESORES.
ALTER TABLE PROFESORES DROP COLUMN Direccion;
Cambia la clave primaria de la tabla PROFESORES por Nombre y Apellidos.
ALTER TABLE PROFESORES DROP CONSTRAINT PRO_NIF_PK;
ALTER TABLE PROFESORES ADD CONSTRAINT PRO_NOM_AP1_AP2_PK PRIMARY
KEY(Nombre, Apellido1, Apellido2);
Renombra la tabla PROFESORES por TUTORES.
RENAME PROFESORES TO TUTORES;
Elimina la tabla ALUMNOS.
DROP TABLE ALUMNOS;
Crea un usuario con tu nombre y clave BD02 y dale todos los privilegios sobre la tabla CURSOS.
CREATE USER JOSEMARIA IDENTIFIED BY BD02;
GRANT ALL PRIVILEGES ON SYSTEM.CURSOS TO JOSEMARIA;
Ahora al usuario anterior quítale permisos para modificar o actualizar la tabla CURSOS.
REVOKE UPDATE, ALTER ON SYSTEM.CURSOS FROM JOSEMARIA;
