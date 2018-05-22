import 模块MySQLdb

#mysqldb
import MySQLdb
1
2
连接数据库，看看连接本地数据库

#打开数据库连接
conn=MySQLdb.connect(host="localhost",user="root",passwd="123456",db="test",charset="utf8")

# 使用cursor()方法获取操作游标
cursor = db.cursor()

# 使用execute方法执行SQL语句
cursor.execute("SELECT * FROM sr_area")

可正常连接到本地数据库

现在连接其他数据库

#打开数据库连接
conn=MySQLdb.connect(host="xxx.xxx.xxx.xxx",user="root",passwd="pwd",db="test",charset="utf8")
