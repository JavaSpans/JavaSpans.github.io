---
title: Mysql
description: ' '
tags:
  - Mysql
  - 笔记
categories: Mysql
copyright: true
abbrlink: 54e1373e
---

### Mysql


```mysql
-- 查询所有住在南昌的女学生
SELECT * from yd_student where sex='女' and  address = '南昌';
-- 查询所有男生的信息
SELECT * FROM yd_student WHERE sex='男';
-- 查询所有女生的姓名，学号，地址
SELECT name,sno,address FROM yd_student WHERE sex='女';
-- 把南昌的女的学生删除
DELETE from yd_student where sex='女' and  address='南昌';

-- 查询yd_user 按年龄排序
SELECT * FROM yd_user ORDER BY age DESC;  -- 降序(大到小)
SELECT * FROM yd_user ORDER BY age ASC;   -- 升序

-- 分组查询
SELECT * from yd_user GROUP BY sex,id;-- 分组查询
-- 分组查询所有男生女生各有多少人
SELECT sex,COUNT(sex) FROM yd_user GROUP BY sex;
SELECT COUNT(*) from yd_user; -- 统计查询
-- 分组查询，并且设置分组条件
-- 1.查询按照性别分组后数量大于2的那个性别，输出性别及数量
SELECT sex,COUNT(sex) from yd_user GROUP BY sex;
HAVING COUNT(sex)>2;
-- 2.查询按照性别分组后年龄大于两岁，数量大于2的那个性别，输出性别及数量
SELECT sex,COUNT(sex) from yd_user where age>2 GROUP BY sex;
HAVING COUNT(sex)>2;

-- 限制查询数量 limit
-- 1.查前面两个人数据
SELECT * from yd_user LIMIT 2;
SELECT * from yd_user LIMIT 0,2;
-- 2.查询从第二开始查询两条数据  前面的数字代表从第几条开始，后面的数字代表查询几条
SELECT * from yd_user LIMIT 2,2;
-- 3.查询从第二开始查询两条数据中的男的
SELECT * from yd_user where sex='男' LIMIT 2,2;
-- 4查询从第二开始查询两条数据中的男的并按照年龄排序
SELECT * from yd_user where sex='男' ORDER BY age DESC LIMIT 0,3;




-- 去除重复
SELECT address from yd_student; -- 去除来自重复的地址
SELECT DISTINCT address from yd_student; -- 地址
SELECT DISTINCT name from yd_student;-- 名字



-- 别名
SELECT s.sex as '性别',COUNT(*) as '总人数' from yd_student as s GROUP BY sex;-- 查询男生女生个有多少人数


SELECT name as '姓名',sex as'性别',address as '地址' from yd_student;

#查询工资>12000的员工信息
SELECT * from employees where salary>12000;
#查询部门编号不等于90的员工名和部门编号
SELECT first_name,department_id from 
employees where department_id !=90;
#查询工资在10000到20000之间的员工名、工资以及奖金
SELECT first_name,salary,commission_pct from 
employees where salary>10000 and salary<20000;

SELECT first_name,salary,commission_pct from 
employees where salary BETWEEN 10000 and 20000;
#查询部门编号不是在90到100之间，或者工资高于15000的员工信息
SELECT * from employees where 
(department_id<=90 and department_id>=100) or salary>15000;
#查询员工last_name中包含字符a的员工信息
SELECT * from employees where last_name like "%a%";
#查询员工last_name的第二个字符为a，第五个字符为e的员工信息
SELECT * from employees where last_name like "_a__e%";
#查询员工last_name的第二个字符为_的员工信息
SELECT * from employees where last_name like "_\_%";
#查询工资在10000到20000之间的员工名、工资以及奖金
SELECT first_name,salary,commission_pct from 
employees where salary>10000 and salary<20000;
#查询员工的工种编号为 IT_PROG，AD_VP，AD_PRES中的一个的员工信息
SELECT * from employees where 
job_id in('IT_PROG','AD_VP','AD_PRES');

#查询没有奖金的员工信息
select * from employees where commission_pct is null;
#查询有奖金的员工信息
select * from employees where commission_pct is not null; 
#查询员工号为176的员工的姓名、部门号和年薪
select last_name,first_name,job_id from employees where employee_id = 176;

#查询年龄最大的那个人

Select max(age) from yd_user ;

#查询年纪最小的那个人

select min(min) from yd_user;

#统计所有岁数的和
select SUM(age) from yd_user;

#查询数据库yd_users age 内为 2，3，30
SELECT * FROM yd_users WHERE age in(2,3,30);
#查询数据库yd_users age 内不为 2，3，30
SELECT * FROM yd_users WHERE age  NOT	in(2,3,30);
#查询数据库yd_users age 内字符串为空
SELECT * FROM yd_users WHERE age = ' ';
#查询数据库yd_users age 内为null的值
SELECT *FROM yd_users WHERE age is NULL;
#查询数据库yd_users age 内为不为null的值
SELECT * FROM yd_users WHERE age is not null;
#查询性别不是男的人
SELECT * FROM yd_users WHERE sex != '男';
SELECT * FROM yd_users WHERE sex <> '男';
#模糊查询
#查询名字是包含e的人
SELECT * FROM yd_study WHERE name LIKE '%e%';
#查询名字是J开头的人
SELECT * FROM yd_study WHERE name like 'j%';
#查询身份证号减去年龄等于360109的人
SELECT * FROM yd_study WHERE idcard-age = 360109;


```

