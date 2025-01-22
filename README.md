# azwellplus-dataiku
postgres=# create user "eh.choi" password '123123' ;
CREATE ROLE
postgres=# create user "eh.choi2" password '123123';


create schema result_data;

CREATE TABLE public.tb_dsp_user (
	eno varchar(10) NOT NULL,
	user_name varchar(10) NULL,
	CONSTRAINT tb_dsp_user_pkey PRIMARY KEY (eno)
);

drop table public.tb_dsp_user;

create schema result_data;


grant all on database dataiku_data to "user1";

grant all on schema result_data to "user1";

grant all on schema public to "user1";



revoke all on schema result_data from "eh.choi";
revoke all on schema public from "eh.choi";

CREATE TABLE result_data.tb_dsp_user (
	eno varchar(10) NOT NULL,
	user_name varchar(10) NULL,
	CONSTRAINT tb_dsp_user_pkey PRIMARY KEY (eno)
);





grant connect on database dataiku_data to "eh.choi";
grant usage,create on schema public to "eh.choi";


grant connect on database dataiku_data to "eh.choi2";
grant usage,create on schema public to "eh.choi2";

grant usage on schema result_data to user1;

grant select on table result_data.tb_dsp_user to user1;


revoke all on database dataiku_data from "eh.choi";




grant usage on schema result_data to "eh.choi";

revoke all on schema result_data from "eh.choi";