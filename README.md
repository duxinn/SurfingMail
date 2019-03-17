此文档用于发送邮件，分三个步骤

1.导入
    from SurfingMail import server
2.实例化一个服务对象

  
    host = "xxx.xxx.com"
    sender = "xxx@xxx.com"
    username = "username"
    password = "password"
    
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
            