Paillier加密算法（Paillier Pascal）是基于复合剩余类的困难性问题
  具体过程：

密钥生成：
  1、随机选择两个大质数p和q满足gcd（pq,(p-1)(q-1)）=1。 这个属性是保证两个质数长度相等。
  2、计算 n = pq和λ= lcm (p - 1,q-1)。
  3、选择随机整数g使得gcd(L(g^lambda % n^2) , n) = 1,满足g属于n^2;
  4、公钥为（N，g）
  5、私钥为lambda。
  加密
  选择随机数r满足
  计算密文
  其中m为加密信息
  
  解密：
  m = D(c,lambda) = ( L(c^lambda%n^2)/L(g^lambda%n^2) )%n;
  其中L(u) = (u-1)/n;

