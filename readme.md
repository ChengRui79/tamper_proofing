## 网页防篡改方案设计
### 目的与方法

动态网页防篡改的重点是数据库内容的保护，防止黑客更改数据库内容的方法有很多，其中对数据库内容进行加密是主要方法，对于访问频繁、内容较多的数据库数据，应采用对称加密方法以保证数据访问效率。

本项目使用AES对称加密算法，设计实现了对数据库数据的加密，往数据库添加数据需要加密，从数据库取出的数据在形成动态页面前要先解密，黑客无法在没有加密秘钥的情况下获取数据库信息、篡改数据库从而篡改网页信息。

### 效果展示

本项目使用Django+MySQL+bootstrap搭建了一个学生成绩查询网站，可以对数据库进行查询和插入

![2](https://github.com/KarlRixon/tamper_proofing/blob/master/img/2.png)

![1](https://github.com/KarlRixon/tamper_proofing/blob/master/img/1.png)

数据库中存放的是加密后的信息

![3](https://github.com/KarlRixon/tamper_proofing/blob/master/img/3.png)

若直接对数据库内容进行修改，网页中显示的信息为空，这时就会发现数据库遭到篡改

![4](https://github.com/KarlRixon/tamper_proofing/blob/master/img/4.png)

