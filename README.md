# 注意事项

  在加密解密方法的Cipher cipher = Cipher.getInstance("RSA/None/PKCS1Padding");语句中 ；
  getInstance（）里面的参数如果是本地加密解密就可以直接使用keyFactory.getAlgorithm()
  
  但如果是从Java服务器端传递过来的密文要使用"RSA/None/PKCS1Padding"才能解密成功，否则会报错。
  
  Android客户端使用公钥加密，在getInstance（）里面的参数要使用"RSA/ECB/PKCS1Padding"，这样Java服务器端才能解密成功！
 
