1.	Declare
2.	Cursor emp is select salary,empname from employee;
3.	Salary number(10,2);
4.	Empname char(20);
5.	Begin
6.	Open emp;
7.	If emp%isopen then
8.	Dbms
9.	Endif;
10.	Loop
11.	Fetch emp into salary,empame;
12.	Exit when emp%notfound;
13.	Dbms
14.	End loop;
15.	Dbms
16.	Close emp;
17.	End
18.	/


1.	Declare cursor rollcursor(proll number,pname varchar2) is
2.	Select roll,number from orc
3.	Where roll=proll and name=pname;
4.	Begin
5.	For rec in (select roll,name from nrc)
6.	Loop
7.	Open rollcursor(rec.roll,rec.name);
8.	Fetch rollcursor into rec.roll,rec.name;
9.	If rollcursor%notfound then 
10.	Insert into orc(roll,name) values(rec.roll,rec.name);
11.	Endif;
12.	Close rollcursor;
13.	End loop;
14.	Commit;
15.	End;
16.	/
![image](https://github.com/user-attachments/assets/aab93a81-9c8a-43dc-a459-e28bbe76499d)
