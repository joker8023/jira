基于docker 的jira 安装及破解
-----
### 克隆项目

```
git clone git@github.com:joker8023/jira.git
```
### 启动docker-compose


```
sudo docker-compose up -d
```

### 破解 jira


破解文件和中文包都在crackfile文件夹内

#### 进入jira
```
sudo docker exec -it jira /bin/sh
```
#### 备份文件


```

 mv /opt/atlassian/jira/atlassian-jira/WEB-INF/lib/atlassian-extras-2.2.2.jar      /opt/atlassian/jira/atlassian-jira/WEB-INF/lib/atlassian-extras-2.2.2.jar.bak

 #atlassian-universal-plugin-manager-plugin的版本可能不一致,按照实际情况备份
 
mv /opt/atlassian/jira/atlassian-jira/WEB-INF/atlassian-bundled-plugins/atlassian-universal-plugin-manager-plugin-2.19.1.jar /opt/atlassian/jira/atlassian-jira/WEB-INF/atlassian-bundled-plugins/atlassian-universal-plugin-manager-plugin-2.19.1.jar.bak

# 退出容器
exit
```

#### 将破解文件复制到相应位置
```
sudo docker cp ~/jira/crackfile/atlassian-extras-2.2.2.jar jira:/opt/atlassian/jira/atlassian-jira/WEB-INF/lib/atlassian-extras-2.2.2.jar
# 破解文件atlassian-universal-plugin-manager-plugin可能版本不一样，改名字成你自己的版本名字然后复制
docker cp ~/jira/crackfile/atlassian-universal-plugin-manager-plugin-2.19.1.jar jira:/opt/atlassian/jira/atlassian-jira/WEB-INF/atlassian-bundled-plugins/atlassian-universal-plugin-manager-plugin-2.19.1.jar
```
#### 重启docker

```
sudo docker stop jira
sudo docker start jira
```
####
设置 -系统 -授权
输入

```
Description=JIRA: Commercial,
CreationDate=2017-03-25,
jira.LicenseEdition=ENTERPRISE,
Evaluation=false,
jira.LicenseTypeName=COMMERCIAL,
jira.active=true,
licenseVersion=2,
MaintenanceExpiryDate=2099-12-31,
Organisation=GENCH,
SEN=SEN-L9480575,
ServerID=BTTV-B5E7-W7QX-ZYT0,
jira.NumberOfUsers=-1,
LicenseID=LIDSEN-L2651368,
LicenseExpiryDate=2099-12-31,
PurchaseDate=2017-05-25,
```
> Organisation改成你自己的组织，可以随便写
SEN ，ServerID在授权信息上有的，改掉 确定就可以了







