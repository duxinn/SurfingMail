此文档用于发送邮件，分三个步骤

1.导入
    from SurfingMail import server
2.实例化一个服务对象

  
    host = "smtp.163.com"
    sender = "chenqin_1990@163.com"
    username = "chenqin_1990"
    password = "12110010_wy"
    
    s = server(host, sender, password, username)
  或者
   
    para_d = {
        'host': host,
        'sender': sender,
        'password': password,
        'username': '',
        'port': 25,
    }
    
    s = server(**para_d)
    
3.发送邮件

    s.send_mail('xxx@xxx.com',
            a='text.txt',
            subject='subject', 
            content='content',
            )
            