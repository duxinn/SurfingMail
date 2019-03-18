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
    参数：
    to： str（必须） 收件人邮箱
    subject: str（可选）主题，默认'未命名主题'
    content: str（可选）内容，默认'未命名内容'
    cc: str（可选） cc收件人，默认空
        to 和 cc 都支持传输多个收件人，支持列表、元组、字符串，比如
        to = ['tom@xxx.com', 'lucy@xxx.com']
        或者
        to = ('tom@xxx.com', 'lucy@xxx.com')
        或者
        to = 'tom@xxx.com,lucy@xxx.com'
        邮件格式不对会报TypeError错。
    a: str（可选） 附件，文件不存在会报FileNotFoundError
    email_subtype: str（可选）邮件的类型，默认mixed， 可选'related','alternative'
    text_subtype: str（可选）文本的类型，默认'plain', 可选'html'
            
            
            