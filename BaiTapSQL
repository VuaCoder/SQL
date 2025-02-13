CREATE DATABASE FUH_company1
use FUH_company1
create table tblDepartment
(
depNum int primary key,
depName nvarchar(50) not null, 
mgrSSN varchar(11), 
mgrAssDate date 
)
create table tblEmployee
(
empSSN varchar(11) primary key, 
empName nvarchar(30) not null,
empAddress nvarchar(50) default N'Đà Nẵng',
empSalary numeric(9, 0),
empSex char(1),
empBoD date,
depNum int, 
suppervisorSSN varchar(11),
empStartDate date
constraint fk_emp foreign key(depNum) references tblDepartment(depNum) 
)

create table tblDependent
(
depName nvarchar(30),
empSSN varchar(11),
depSex char(1),
depBoD date,
depRelationship nvarchar(10) 
constraint pk_dep primary key(depName, empSSN), 
constraint fk_dep foreign key(empSSN) references tblEmployee(empSSN)
)

create table tblLocation(
locNum varchar(11) primary key,
locName nvarchar(50)
)
create table DepLocation(
depNum int,
locNum varchar(11),
constraint pk_location primary key(depNum,locNum),
constraint fk_location foreign key(depNum) references tblDepartment(depNum),
constraint fk_locate foreign key(locNum) references tblLocation(locNum)
)
create table tblProject(
proNum int primary key,
proName nvarchar(30),
locNum varchar(11),
depNum int,
constraint fk_project foreign key(depNum) references tblDepartment(depNum)
)
create table tblWorksOn(
workHours int,
empSSN varchar(11),
proNum int
constraint pk_work primary key(empSSN, proNum),
constraint fk_work1 foreign key(empSSN) references tblEmployee(empSSN),
constraint fk_work2 foreign key(proNum) references tblProject(proNum)
)
insert into tblDepartment
values(1, N'Phòng phần mềm trong nước','30121050037','2003-01-10')
insert into tblDepartment
values(2, N'Phòng phần mềm nước ngoài','30121050142','2005-01-06')
insert into tblDepartment
values(3, N'Giải pháp mạng truyền thông','30121050254','2000-01-01')
insert into tblDepartment
values(4, N'Phòng dịch vụ chăm sóc khách hàng','30121050037','2003-01-10')
insert into tblDepartment
values(5, N'Phòng Nghiên cứu và phát triển','30121050037','2003-01-10')
insert into tblLocation
values(1,N'TP Hà Nội')
insert into tblLocation
values(2,N'TP Hải Phòng')
insert into tblLocation
values(3,N'TP Đà Nẵng')
insert into tblLocation
values(4,N'TP Huế')
insert into tblLocation
values(5,N'TP Hồ Chí Minh')
insert into tblLocation
values(6,N'TP Cần Thơ')
insert into DepLocation
values(1,1)
insert into DepLocation
values(1,2)
insert into DepLocation
values(1,3)
insert into DepLocation
values(1,5)
insert into DepLocation
values(2,1)
insert into DepLocation
values(2,2)
insert into DepLocation
values(2,4)
insert into DepLocation
values(3,1)
insert into DepLocation
values(3,4)
insert into DepLocation
values(4,1)
insert into DepLocation
values(4,3)
insert into DepLocation
values(4,5)
insert into DepLocation
values(5,1)
insert into DepLocation
values(5,2)
insert into DepLocation
values(5,4)
insert into tblEmployee
values ('30121050004', N'Mai Duy An', N'Long An', 30000, 'F', '1968-02-17', 1, '30121050037', '2000-01-10')
insert into tblEmployee
values('30121050015', N'Huỳnh Mai Anh', N'TP. Hồ Chí Minh', 58000, 'F', '1963-05-04', 1, '30121050004', '2005-01-14')
insert into tblEmployee
values('30121050027', N'Nguyễn Thúy Quỳnh Anh', N'Nam Định', 91000, 'F', '1977-04-10', 1, '30121050004', '2005-02-25')
insert into tblEmployee
values('30121050035', N'Tống Thị Lan Anh', N'Vũng Tàu', 78000, 'F', '1978-10-28', 1, '30121050037', '2004-04-15')
insert into tblEmployee
values('30121050037', N'Võ Việt Anh', N'Khánh Hoà', 111000, 'M', '1974-11-11', 1, NULL, '2000-05-23')
insert into tblEmployee
values('30121050038', N'Vũ Thụy Hồng Anh', N'TP. Hồ Chí Minh', 104000, 'F', '1966-06-13', 2, '30121050142', '2000-05-24')
insert into tblEmployee
values('30121050049', N'Trần Nguyễn Phương Bình', N'TP. Hồ Chí Minh', 83000, 'M', '1959-05-17', 2, '30121050038', '2005-05-12')
insert into tblEmployee
values('30121050060', N'Trần Thiện Bảo', N'TP. Hồ Chí Minh', 75000, 'M', '1955-12-26', 2, '30121050038', '2008-10-20')
insert into tblEmployee
values('30121050142', N'Nguyễn Hoàng Dũng', N'TP. Hồ Chí Minh', 114000, 'M', '1956-02-26', 2, NULL, '2006-12-25')
insert into tblEmployee
values('30121050158', N'Lê Hoàng Linh Giang', N'Huế', 98000, 'F', '1957-07-16', 2, '30121050142', '2006-11-20')
insert into tblEmployee
values('30121050180', N'Tân Ngọc Như Hằng', N'TP. Hồ Chí Minh', 59000, 'F', '1970-05-29', 5, '30121050184', '2007-01-15')
insert into tblEmployee
values('30121050184', N'Nguyễn Thị Minh Hưng', N'Thanh Hoá', 92000, 'F', '1976-12-23', 5, NULL, '2007-03-18')
insert into tblEmployee
values('30121050254', N'Bùi Thị Thu Hương', N'TP. Hà Nội', 117000, 'F', '1970-01-06', 4, NULL, '2008-06-24')
insert into tblEmployee
values('30121050254', N'Phạm Thị Ngọc Thảo', N'Gia Lai', 35000, 'F', '1975-02-04', 3,'30121050254', '2008-08-10')
insert into tblEmployee
values('30121050294', N'Trịnh Hạnh', N'TP. Đà Nẵng', 94000, 'M', '1977-02-12', 3, '30121050295', '2005-05-05')-- done
insert into tblEmployee 
values('30121050295', N'Huỳnh Thị Như Hồng', N'TP. Cần Thơ', 110000, 'F', '1970-08-14', 4, NULL, '2008-12-17')
insert into tblEmployee
values('30121050322', N'Đỗ Thị Thúy Hùng', N'Sông Bé', 76000, 'F', '1963-01-22', 3, '30121050254', '2002-11-11')
insert into tblEmployee
values('30121050336', N'Trương Thanh Hiền', N'TP. Hải Phòng', 102000, 'F', '1963-05-16', 4, '30121050295', '2003-04-27')
insert into tblEmployee
values('30121050341', N'Nguyễn Đặng Hiếu', N'TP. Hồ Chí Minh', 46000, 'M', '1970-08-30', 4, '30121050295', '2008-08-09')
insert into tblEmployee
values('30121050418', N'Võ Phạm Minh Hương', N'TP. Hà Nội', 30000, 'F', '1971-08-17', 5, '30121050184', '2009-07-25')
insert into tblEmployee
values('30121050982', N'Hồ Việt Hoà', N'Đồng Nai', 95000, 'M', '1970-02-03', 5, '30121050254', '2005-11-24')
insert into tblProject
values(1,'ProjectA',1,3)
insert into tblProject
values(2,'ProjectB',1,2)
insert into tblProject
values(3,'ProjectC',3,2)
insert into tblProject
values(4,'ProjectD',2,1)
insert into tblProject
values(5,'ProjectE',5,4)
insert into tblWorksOn
values(7,'30121050027',1)
insert into tblWorksOn
values(5,'30121050027',2)
insert into tblWorksOn
values(7,'30121050027',1)
insert into tblWorksOn
values(18,'30121050027',4)
insert into tblWorksOn
values(15,'30121050035',4)
insert into tblWorksOn
values(10,'30121050037',1)
insert into tblWorksOn
values(10,'30121050037',2)
insert into tblWorksOn
values(15,'30121050037',4)
insert into tblWorksOn
values(5,'30121050037',5)
insert into tblWorksOn
values(33,'30121050038',2)
insert into tblWorksOn
values(12,'30121050038',3)
insert into tblWorksOn
values(24,'30121050049',2)
insert into tblWorksOn
values(6,'30121050049',3)
insert into tblWorksOn
values(21,'30121050060',2)
insert into tblWorksOn
values(27,'30121050060',3)
insert into tblWorksOn
values(9,'30121050142',2)
insert into tblWorksOn
values(12,'30121050142',3)
insert into tblWorksOn
values(21,'30121050158',2)
insert into tblWorksOn
values(12,'30121050158',3)
insert into tblWorksOn
values(24,'30121050254',1)
insert into tblWorksOn
values(40,'30121050265',1)
insert into tblWorksOn
values(5,'30121050294',3)
insert into tblWorksOn
values(15,'30121050294',5)
insert into tblWorksOn
values(15,'30121050295',5)
insert into tblWorksOn
values(30,'30121050322',1)
INSERT INTO tblDependent VALUES (N'Bùi Phương Ngọc', '30121050180', 'M', '1967-03-30', N'Chồng')  
INSERT INTO tblDependent VALUES (N'Đoàn Minh Đạo', '30121050038', 'M', '1962-10-04', N'Chồng')
INSERT INTO tblDependent VALUES (N'Hà Mỹ Duyên', '30121050037', 'F', '1980-06-15', N'Vợ')  
INSERT INTO tblDependent VALUES (N'Hồ Đức Trung Hữu', '30121050158', 'M', '1960-04-16', N'Chồng')  
INSERT INTO tblDependent VALUES (N'Huỳnh Thị Ngọc Diệp', '30121050049', 'F', '1970-06-13', N'Vợ') 
INSERT INTO tblDependent VALUES (N'Nguyễn Thạc Hải', '30121050254', 'M', '1970-09-17', N'Chồng')
INSERT INTO tblDependent VALUES (N'Nguyễn Thị Minh Hà', '30121050184', 'F', '1980-03-06', N'Em') 
INSERT INTO tblDependent VALUES (N'Nguyễn Thị Minh Hằng', '30121050060', 'F', '1965-01-04', N'Vợ') 
INSERT INTO tblDependent VALUES (N'Nguyễn Thị Thu Hằng', '30121050142', 'F', '1969-03-30', N'Vợ') 
INSERT INTO tblDependent VALUES (N'Nguyễn Thị Thùy Dung', '30121050027', 'F', '1953-10-01', N'Mẹ') 
INSERT INTO tblDependent VALUES (N'Phạm Nguyên Dũng', '30121050015', 'M', '1965-04-16', N'Chồng')
INSERT INTO tblDependent VALUES (N'Phan Thành Đăng', '30121050035', 'M', '1970-02-24', N'Chồng')  
INSERT INTO tblDependent VALUES (N'Vương Thị Kim Cúc', '30121050004', 'F', '1978-03-20', N'Em')
