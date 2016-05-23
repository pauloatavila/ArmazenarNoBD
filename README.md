# ArmazenarNoBD
Trabalho para armazenar os dados de um arquivo csv para um Banco de Dados

Primeiramente, crie uma tabela no aplicativo Postgres. Utilize o código abaixo:
CREATE TABLE public.geraltable
(
  id integer NOT NULL DEFAULT nextval('geraltable_id_seq'::regclass),
  campus character varying(50) NOT NULL,
  cod_curso character varying(50) NOT NULL,
  curso character varying(100) NOT NULL,
  matricula character varying(10) NOT NULL,
  nome character varying(256) NOT NULL,
  versao_curso character varying(30) NOT NULL,
  forma_ingr character varying(50) NOT NULL,
  ano_ingr character varying(10) NOT NULL,
  periodo_ingr character varying(20) NOT NULL,
  form_evasao character varying(100) NOT NULL,
  ano_evasao character varying(10) NOT NULL,
  periodo_evasao character varying(20) NOT NULL,
  email_um character varying(200),
  email_dois character varying(200),
  fone_res character varying(20),
  fone_cel character varying(20),
  fone_com character varying(20),
  dt_ingr character varying(10) NOT NULL,
  dt_conclusao character varying(10) NOT NULL,
  dt_colacao character varying(10) NOT NULL
)
WITH (
  OIDS=FALSE
);

Agora baixe e adicione uma biblioteca de dependência JAR através do link: https://jdbc.postgresql.org/download.html

Para finalizar, altere as configurações de conexão (servidor, porta e nome do banco de dados) nas classes: ArmazenarDB e MostrarDB.
