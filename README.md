# the-use-of-class
the class of sellecting course
from tkinter import *
from tkinter import messagebox

import pymysql
from pymysql.cursors import Cursor
conn = pymysql.Connect(
host='localhost',
port=3306,
user='root',
passwd='12345',
db='天朝理工学院',
charset="utf8"
)  # 连接数据库

def c1():                                                                                            #提交按钮事件
    pass

root=Tk()
root.title("课程管理系统-注册")
root['width']=300
root['height']=400
root['bg']='pink'
root.geometry('400x600-100-100')

f1=Frame(root);f1.pack()
f2=Frame(root);f2.pack()

Label(f1,text="\n欢迎进入！\n \n",font=('Helvetica',12,'bold'),bg='pink').pack()
Label(f2,text="天朝皇家理工学院\n 学生选课中心\n（纺织类）\n    \n",font=('Helvetica',12,'bold'),bg='pink').pack()

def callCheckbutton():
    cursor = conn.cursor()
    #sql = "insert into login(number,password) values(%s,%s)on duplicate"
    #value = ((v3, v4))
    # cursor.execute(sql, value)
    sql1 = "SELECT *FROM login"                                                        # 查询数据没问题，不能插入
    cursor.execute(sql1)
    print(cursor.rowcount)
    conn.commit()
    cursor.close()
    conn.close()
Checkbutton(root,text = '       纺织工程',command = callCheckbutton,bg='pink').pack()

def callCheckbutton():
    cursor = conn.cursor()
    #sql = "insert into login(number,password) values(%s,%s)on duplicate"
    #value = ((v3, v4))
    # cursor.execute(sql, value)
    sql1 = "SELECT *FROM login"                                                        # 查询数据没问题，不能插入
    cursor.execute(sql1)
    print(cursor.rowcount)
    conn.commit()
    cursor.close()
    conn.close()
Checkbutton(root,text = '       洗漂原理',command = callCheckbutton,bg='pink').pack()

def callCheckbutton():
    cursor = conn.cursor()
    #sql = "insert into login(number,password) values(%s,%s)on duplicate"
    #value = ((v3, v4))
    # cursor.execute(sql, value)
    sql1 = "SELECT *FROM login"                                                        # 查询数据没问题，不能插入
    cursor.execute(sql1)
    print(cursor.rowcount)
    conn.commit()
    cursor.close()
    conn.close()
Checkbutton(root,text = '       材料导论',command = callCheckbutton,bg='pink').pack()

def callCheckbutton():
    cursor = conn.cursor()
    #sql = "insert into login(number,password) values(%s,%s)on duplicate"
    #value = ((v3, v4))
    # cursor.execute(sql, value)
    sql1 = "SELECT *FROM login"                                                        # 查询数据没问题，不能插入
    cursor.execute(sql1)
    print(cursor.rowcount)
    conn.commit()
    cursor.close()
    conn.close()
Checkbutton(root,text = ' 纺织工程导论',command = callCheckbutton,bg='pink').pack()

def callCheckbutton():
    cursor = conn.cursor()
    #sql = "insert into login(number,password) values(%s,%s)on duplicate"
    #value = ((v3, v4))
    # cursor.execute(sql, value)
    sql1 = "SELECT *FROM login"                                                        # 查询数据没问题，不能插入
    cursor.execute(sql1)
    print(cursor.rowcount)
    conn.commit()
    cursor.close()
    conn.close()
Checkbutton(root,text = '       纺织机械',command = callCheckbutton,bg='pink').pack()

f3=Frame(root);f3.pack()
Button(f3,text="提交",command=c1).pack(side=RIGHT)

root.mainloop()
