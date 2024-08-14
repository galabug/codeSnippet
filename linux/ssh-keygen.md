- 生成 ssh 密钥
  ssh-keygen -t rsa

- 复制当前服务器的公钥到目标服务器 - 需要输入用户名对应密码
  ssh-copy-id -i ~/.ssh/id_rsa.pub 用户名@ip

- 使用 ssh 登录目标服务器
  ssh pmbt@197.68.21.155

- 没有 ssh-copy-id 命令时
  - 当前服务器
    cat ~/.ssh/id_rsa.pub
  - 复制上面的公钥 到 追加到目标服务器的 authorized_keys 文件末尾
    echo '公钥' >> ~/.ssh/authorized_keys
