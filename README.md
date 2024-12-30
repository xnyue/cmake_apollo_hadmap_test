# cmake_apollo_hadmap_test

///////////////////////////////////////////part1: 配置ssh秘钥
//生成秘钥
ssh-keygen -t rsa -C "13659260727@163.com"
id_rsa_xxx
cat ~/.ssh/id_rsa_xxx
//验证ssh 配置是否成功
ssh -T git@github.com
//touch config,并在其中配置不同的服务器
# gitlab
Host gitlab.ylwnl.com  　
HostName gitlab.xxx.com 　　
PreferredAuthentications publickey  
IdentityFile ~/.ssh/gitlab_id_rsa 

# github
Host github.com
HostName github.com
PreferredAuthentications publickey
IdentityFile ~/.ssh/github_id_rsa

# gitee
Host gitee.com
HostName gitee.com
PreferredAuthentications publickey
IdentityFile ~/.ssh/gitee_id_rsa

教程：https://blog.csdn.net/qq_55558061/article/details/124117445

////////////////////////////////////////////part2: 下拉上传代码
echo "# cmake_apollo_hadmap_test" >> README.md
git init
git add README.md
git commit -m "first commit"
git branch -M main
git remote add origin https://github.com/xnyue/cmake_apollo_hadmap_test.git
git push -u origin main
