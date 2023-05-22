# -
数据库技术课程项目——图书借阅系统
一、数据表 
1.借阅人：证件号，姓名，类别（教师，学生），已借数目，电话
2.图书：图书编号，书名，类别，是否借出
3.借阅信息：证件号，图书编号，借出日期，应归还日期（计算字段），实际归还日期
二、功能设计
1.创建视图显示所有逾期未归还的借阅信息（包括借阅人姓名，借阅人类别，书名，借出日期，应归还日期，逾期时长）；
2.创建存储过程，每借出一本图书，向借阅信息表中加入一条记录；
3.创建存储过程，每归还一本图书，修改借阅信息表中相应的记录；
4.创建存储函数，根据图书编号查借阅人姓名，并调用该函数查询‘张三’已借未还的图书情况；
5.创建存储函数，计算某借阅人还能借阅的图书数目，学生限额5本，教师限额10本。
6.创建存储函数，查询某本图书逾期未还的时长，并调用该函数显示所有逾期未归还图书的书名，借阅人和逾期时长并按逾期时长排序；
7.创建存储函数，查询某借阅人有几本逾期未还图书，并调用该函数显示有逾期未归还图书的借阅人和未归还图书数目；
8.创建存储函数，利用游标计算计算某借阅人逾期未还图书应缴纳的罚款，逾期30日内罚款1元，逾期90日内罚款3元，逾期超过90日罚款5元。调用该函数显示所有应缴纳罚款的借阅人的姓名，逾期罚款和电话；
9.创建两个触发器，分别在借出或归还图书时，修改借阅人表中的已借数目字段；
10.创建触发器，当借阅者已借阅的书籍数目达到限额时，禁止借入新的书籍。
