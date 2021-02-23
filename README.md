# keycloak-services-social-wechat-work

Keycloak企业微信登录插件

版本：10.0.2，原项目在6.x下也可以使用

## 构建
`mvn clean package`

## 安装

* 将jar包添加到你的keycloak服务:
(create `providers` folder if needed):
  * `$ cp target/keycloak-services-social-wechat-work-{x.y.z}.jar _KEYCLOAK_HOME_/standalone/deployments/` 

* 将页面模板添加到你的keycloak服务:
  * `$ cp themes/base/admin/resources/partials/realm-identity-provider-wechat-work.html _KEYCLOAK_HOME_/themes/base/admin/resources/partials/`
  * `$ cp themes/base/admin/resources/partials/realm-identity-provider-wechat-work-ext.html _KEYCLOAK_HOME_/themes/base/admin/resources/partials/`

基于 https://github.com/kkzxak47/keycloak-services-social-wechatwork

## 配置

| key | value |
| --- | --- |
| First Login Flow  | first broker login |
| Post Login Flow  | 空 |

## 注意

- 原项目和本项目的区别，需要把 `jboss-deployment-structure.xml` 放到 `META-INF` 目录下
- 用户登录之后，为什么登录到管理端显示没有权限？需要有一个初始化角色的过程
    （见：https://wiki.corp.bm-sk.cn/pages/viewpage.action?pageId=30246898）
