# MyBatisCodeHelper-Pro

[![Jetbrains Plugins](https://img.shields.io/jetbrains/plugin/v/9837-a8translate.svg)][plugin]
[![Downloads](https://img.shields.io/jetbrains/plugin/d/9837.svg?style=flat-square)][plugin]
[![加入QQ群](https://img.shields.io/badge/chat-QQ群-46BC99.svg?style=flat-square)](//shang.qq.com/wpa/qunwpa?idkey=6bc11bfe278fa0d1d0d6292fa010b1aa8ddadbfeb70ef893083d5ab800137c1a)


<div align="right">
<a href="README_EN.md">English</a>  
</div>

qq群：542735979（插件bug修复 最新版本及问题讨论）

介绍视频:https://www.bilibili.com/video/av23458308/

Intellij下Mybatis支持插件 

功能
- 从java类生成mybatis crud代码 建表语句 支持生成service，建表支持生成多字段的索引
- 添加一个数据库 从数据库生成crud代码 支持mysql oracle sqlserver postgresql 
- 直接从Intellij自带的数据库生成crud代码
- 通过方法名(不需要方法的返回值和参数 会自动推导出来)来生成sql 可以生成大部分单表操作的sql 只需要一个方法的名字即可 会自动补全好方法的参数和返回值 和springdatajpa的语句基本一致
- xml中的 param的自动提示 if test的自动提示 resultMap refid 等的自动提示
- xml中refid，resultMap等的跳转到定义
- mybatis接口和xml的互相跳转  支持一个mybatis接口对应多个xml
- 检测没有使用的xml 可一键删除
- 检测mybatis接口中方法是否有实现，没有则报红 可创建一个空的xml
- 检测resultmap的property是否有误 
- resultMap中的property的自动提示
- mybatis接口中一键添加param注解
- mybatis接口一键生成xml
- mybatis接口中的方法名重构支持
- 支持spring 将mapper注入到spring中 intellij的spring注入不再报错 支持springboot

-----------------------------------------------------------------------

可以免费试用: http://brucege.com/pay/view

付款过程中有问题请添加微信:
![weichaturl](http://ogyxv3y5w.bkt.clouddn.com/WechatIMG1.jpeg)

不支持的功能
- 不支持生成关联表的sql (如果觉得可以实现可以联系我)

之后会加入更多功能


#### 根据接口的方法名直接生成对应的sql  
![generateMultiple](https://raw.githubusercontent.com/gejun123456/MyBatisCodeHelper-Pro/master/screenshots/2017_08_06_multiple_sql_generate.gif)

#### 根据java对象一键生成 Dao接口，Service，Xml，数据库建表Sql文件  提供dao与xml的跳转  
![generateFile](https://raw.githubusercontent.com/gejun123456/MyBatisCodeHelper-Pro/master/screenshots/20170712_generateFiles.gif)


#### 根据dao中的方法名生成对应的mapper sql并进行方法补全  
![find](https://raw.githubusercontent.com/gejun123456/MyBatisCodeHelper-Pro/master/screenshots/2017_08_06_find_example_2.gif)

![update](https://raw.githubusercontent.com/gejun123456/MyBatisCodeHelper-Pro/master/screenshots/update.gif)


![delete](https://raw.githubusercontent.com/gejun123456/MyBatisCodeHelper-Pro/master/screenshots/delete.gif)


![count](https://raw.githubusercontent.com/gejun123456/MyBatisCodeHelper-Pro/master/screenshots/count.gif)

![all_1](https://raw.githubusercontent.com/gejun123456/MyBatisCodeHelper-Pro/master/screenshots/all_1.gif)

#### mybatis接口方法名重构支持

![refacterMethodName](https://raw.githubusercontent.com/gejun123456/MyBatisCodeHelper-Pro/master/screenshots/refactor_method_name.gif)

#### mybatis xml的自动补全

![autocomplete](https://raw.githubusercontent.com/gejun123456/MyBatisCodeHelper-Pro/master/screenshots/autoComplete.gif)

#### resultMap refid 跳转到定义和重构

![resultMap](https://raw.githubusercontent.com/gejun123456/MyBatisCodeHelper-Pro/master/screenshots/resultMapJump.gif)

#### property refid resultMap等的自动补全

![property complete](https://raw.githubusercontent.com/gejun123456/MyBatisCodeHelper-Pro/master/screenshots/propertyComplete.gif)

### 方法名生成sql时支持if test

![if-test](https://raw.githubusercontent.com/gejun123456/MyBatisCodeHelper-Pro/master/screenshots/mybatis_generate_if_test.gif)

#### 可以使用Intellij自带的datasource来生成（1.9.2版本 1.8.8-1.9.1有bug 详见https://github.com/gejun123456/MyBatisCodeHelper-Pro/issues/170 理论上Intellij支持的数据库都支持 强烈推荐）
![intellijDatasourceGenerateCrud](https://raw.githubusercontent.com/gejun123456/MyBatisCodeHelper-Pro/master/screenshots/IntellijDatasourceGenerateCrudFile.gif)


#### 使用添加的datasource来生成 （目前支持mysql oracle postgresql sqlserver  myql支持5.5及以上  oracle支持oracle10g及以上 postgresql sqlserver支持最新版，老版本未测试 有问题请联系我) 

![mybatis-database-generator](https://raw.githubusercontent.com/gejun123456/MyBatisCodeHelper-Pro/master/screenshots/configDatabaseToUseMybatisGenerator.gif)


#### 使用mybatisGenerator的配置文件来生成

 mybatis generator 配置文件的规则   
  http://www.mybatis.org/generator/configreference/xmlconfig.html

![mybatis-generator](https://raw.githubusercontent.com/gejun123456/MyBatisCodeHelper-Pro/master/screenshots/2017_08_06_mybatis_generator.gif)

#### 一键生成mybatis generator的xml文件

![generate_mybatis_generator_config_file](https://raw.githubusercontent.com/gejun123456/MyBatisCodeHelper-Pro/master/screenshots/generate_mybatis_generator_config_file.gif)

## spring的支持 识别componentscan mapperscan等注解 将mapper自动注入到spring中 可跳转到定义 支持springboot， Intellij注入mapper不再报错

![sprinboot](https://raw.githubusercontent.com/gejun123456/MyBatisCodeHelper-Pro/master/screenshots/springSupport.gif)




安装
----

支持下面产品 2016.2版本及以上版本

- IntelliJ IDEA
- IntelliJ IDEA Community Edition
- Android Studio



**使用 IDE 内置插件系统:**
- <kbd>Preferences(Settings)</kbd> > <kbd>Plugins</kbd> > <kbd>Browse repositories...</kbd> > <kbd>搜索并找到"MybatisCodeHelper-Pro"</kbd> > <kbd>Install Plugin</kbd>

**直接下载** (不要解压zip 直接安装即可) 请根据IDEA的版本来下载对应的版本 
如果链接下载不了 可以加qq群 542735979 群文件里面有最新的版本
- download[`lastest plugin zip`](https://plugins.jetbrains.com/plugin/9837-mybatiscodehelperpro) -> <kbd>Preferences(Settings)</kbd> > <kbd>Plugins</kbd> > <kbd>Install plugin from disk...</kbd>


重启**IDE**.

使用方法
--------------------------------------------------------------------------
- 在java对象上使用alt+insert （generate mybatis files）生成对应的dao xml文件等 （mac上使用 ctrl+N 即getter setter对应的快捷键)
- 当数据库对象添加字段后也可使用alt+insert （generate mybatis files）来生成更新后的xml。（只会更新默认的insert,insertList,update方法 其他自定义的方法不会变）
- 在mybatis的接口文件上的方法名上使用右键 generatedaoxml 生成对应的mybatis sql及方法的补全


需要注意的点
-----------------------------------------------------------------------------

- 使用方法名生成sql 需要在接口中提供一个insert或save或add方法并以数据库对象为第一参数 (可以通过数据库对象自动生成)
- 使用方法名生成的sql的字段会从数据库对象对应的resultMap中的数据库字段来设置。
- java类生成文件这些 java类中的字段只支持对象类型 比如 int需要改写为Integer
- 当mapper文件和xml文件不在一个module中时 可以在设置中选择searchScope为project
- 当mapper对应多个xml文件时 可以在配置中勾选multipleXmlFile选项

常见问题
----------------------------------------------------------------------------
- "please check with your resultMap dose it contain all the property of 
此时可以检查这个接口对应的对象 比如 这个接口有个 insert(User user) 即 User对象
是否有一个对应的完整的resultMap在xml中， 

- 当生成sql时 如果比如UserMapper对应的User对象中含有List或Set类型的属性时，sql会无法生成
请将这些属性设置为transient类型  

- xml文件可以跳转到mapper文件，mapper文件上没图标， 请确保xml文件对应的 resource文件夹 被 mark as resource root
- 由于激活的时候需要联网，某些公司可能设置了拦截 无法联网，此时可以使用vpn 或者 手机开热点，实在不行 可以进行离线激活 离线激活的教程为 1.8.3版本支持

![offline](https://raw.githubusercontent.com/gejun123456/MyBatisCodeHelper-Pro/master/screenshots/offlineActivation.png)

- 购买后会发两个激活码 可以在两台设备上绑定 一个激活码绑定一个设备 解绑可进行下图的操作 (1.8.3版本支持)
![unBind](https://raw.githubusercontent.com/gejun123456/MyBatisCodeHelper-Pro/master/screenshots/unBind.png)









现在支持的数据库对象字段类型

| 字段类型            |  开始支持的版本        |
|----------------------|-------------------  |
| java.lang.Integer    |   v1.2              |
| java.lang.Long       |   v1.2              |
| java.lang.FLoat      |   v1.2              |
| java.lang.Double     |   v1.2              |
| java.lang.Boolean    |   v1.2              |
| java.util.Date       |   v1.2              |
| java.lang.String     |   v1.2              |
| java.math.BigDecimal |   v1.2              |
| java.lang.Short      |   v1.2              |
|java.sql.Date | v1.3|
|java.sql.Time | v1.3|
|java.sql.Timestamp | v1.3|
|java.time.LocalDateTime | v1.3|
|java.time.LocalDate | v1.3|
|java.time.LocalTime | v1.3|
|java.time.OffsetDateTime | v1.3|
|java.time.OffsetTime | v1.3|
|java.time.ZonedDateTime | v1.3|
| java.lang.Byte       |   v1.6.0              |






方法名生成sql
-----------------------------------------------------------------------------------------
数据库对象User

字段名  | 类型
-----   | ------
id      | Integer
userName | String
password | String

表名为user

xml中对应的resultMap为

	<resultMap id="AllCoumnMap" type="com.codehelper.domain.User">
	    <result column="id" property="id"/>
	    <result column="user_name" property="userName"/>
	    <result column="password" property="password"/>
	</resultMap>


以下是方法名与sql的对应关系(方法名的大小写无所谓)


可以跟在字段后面的比较符有

比较符  | 生成sql | 开始支持的版本号
------- | -------- |---------
between |  prop > {} and prop <{}  |v1.3
betweenOrEqualto | prop >={} and prop <={} | v1.3
lessThan  | prop < {} | v1.3
lessThanOrEqualto | prop <={}  |v1.3
greaterThan | prop > {} |v1.3
greaterThanOrEqualto | prop >={} | v1.3
isnull | prop is null |v1.3
notnull | prop is not null |v1.3
like   | prop like {} |v1.3
in     | prop in {} |v1.3
notin  | prop not in {} |v1.3
not    | prop != {} |v1.3
notlike | prop not like {} |v1.3
startingWith | prop like {}% |v1.6.0
endingWith | prop like %{} |v1.6.0
containing | prop like %{}% |v1.6.0



- find方法

支持获取多字段，by后面可以设置多个字段的条件 一个字段后面只能跟一个比较符
支持orderBy,distinct, findFirst

方法名       |  sql
-----------  |  --------------
find         | select * from user
findUserName | select user_name from user
findById	| select * from user where id = {}
findByIdGreaterThanAndUserName | select * from user where id > {} and user_name = {}
findByIdGreaterThanOrIdLessThan | select * from user where id > {} or id < {}
findByIdLessThanAndUserNameIn  | select * from user where id < {} and user_name in {}
findByUserNameAndPassword      | select * from user where user_name = {} and password = {}
findUserNameOrderByIdDesc   | select user_name from user order by id desc
findDistinctUserNameByIdBetween | select distinct(user_name) from user where id >= {} and id <={}
findOneById	| select * from user where id = {}
findFirstByIdGreaterThan | select * from user where id > {} limit 1
findFirst20ByIdLessThan  | select * from user where id < {} limit 20
findFirst10ByIdGreaterThanOrderByUserName  | select * from user where id > {} order by user_name limit 10
findMaxIdByUserNameGreaterThan | select max(id) from user where user_name > {}
findMaxIdAndMinId   | select max(id) as maxId, min(id) as minId from user


- update方法 by后面设置的条件同上

方法名     | sql
---------- |  -------
updateUserNameById | update user set user_name = {} where id = {}
updateUserNameAndPasswordByIdIn  | update user set user_name = {} and password = {} where id in {}

- delete方法
by后面设置的条件同上

方法名  |  sql
------- | ---------
deleteById | delete from user where id = {}
deleteByUserNameIsNull  | delete from user where user_name is null

- count方法
by后面设置的条件同上 支持distinct

方法名  | sql
------- | ----------
count   | select count(1) from user
countDistinctUserNameByIdGreaterThan | select count(distinct(user_name)) from user where id > {}



CHANGELOG
------------------------------------------------
1.9.3
- 可以通过方法名insertList, insertSelective来生成插入语句
- 修复可能的nullPointer

1.9.1 1.9.2
- 修复使用Intellij的数据库生成的默认类型
- 通过数据库生成时 包名可以自动提示

1.9.0
- 修复intellij重启后配置失效的bug

1.8.9
- 支持高清图标
- mybatis接口一键生成testcase 可对复杂的sql 快速进行测试 不需要要启动spring容器
- java生成crud代码支持postgresql
- 数据库生成时支持使用lombok 支持添加mapperscan注解 toString方法等
- 修复alt+enter在方法名生成sql时的thread报错
- 修复数据库生成时勾选列
1.8.8
- 加快mybatis接口和xml关联的速度
1.8.7
- 直接在Intellij的datasource中生成crud代码
- 添加resultMap property是否正确的检测
- sql中的param if test的自动补全的优化
- bug修复

1.8.6
- 添加2018.1及之后版本的spring支持
- 修复resultMap的自动补全
- 优化check resultMap的提示

1.8.4
- 使用数据库生成时可以自定义字段
- Intellij高级版支持 param的自动补全
- 添加spring的支持

1.8.3
- 离线激活支持
- 解绑支持
- 数据库界面优化

1.8.2
- 修复mysql使用mybatis generator生成时的数据库名


1.8.1
- 添加sqlserver和 oracle10g和 mysql8.0的支持
- 修复BaseColumnList重复生成的问题
- 支持mybatis上 insertProvider等注解


1.8.0
- 支持识别resultMap的extend属性
- 添加oracle和postgresql的支持
- mybatis generator的ui优化
- 自动import优化


1.7.7
- 可以直接从java类跳转到xml
- 一键为方法添加param注解
- 更新生成到mysql的编码为uft8mb4
- 修复findByLike


1.7.6
- 记忆用户保存的路径
- java和xml相互跳转添加快捷键
- 修复编码错误
- 可以配置使用project scope还是module scope
- 修复生成mybatis generator的xml
- 支持一个mapper对应多个xml

1.7.4
- 一键生成mybatis generator的xml文件
- 当更新java类的时候添加jdbcType
- 当xml不被使用时使用警告而不是标红

1.7.3
- 修复thread assertion报错
- 使用mybatis generator时不修改dao文件
- 修复java dateTime的jdbcType

1.7.2  
- 修复 html中 select标签报错  

1.7.1 
- 修复intellij 2017.3的报错
- 优化mac下的ui显示
- 修复orderby多个字段
- 通过数据库的表生成sql添加滚动条
- 不使用的xml标红，可以一键删除


1.7.0
- 生成service添加override注解
- 修复生成的service没有导入java包的问题
- 修复findFirstN没有返回List的问题


1.6.9
- 方法名自动生成增强
- 修复Long类型的jdbcType
- 支持transient字段类型
- findOne不再生成limit 1 可用findFirst


1.6.8
- 修复xml变动时图标会消失的问题
- 支持生成jdbcType

1.6.7
- 生成sql可从java类中生成注释
- 支持切换图标
- 支持updateIncVersion语法

1.6.5
- 支持findWithPage
- 支持自定义mapper后缀

1.6.4
- 支持sqlite
- oracel支持生成多字段唯一，多字段索引

1.6.0
- 支持查询条件加上if test
- 支持生成多字段索引和多字段唯一
- 支持生成方法 max,min,sum等方法
- 支持生成 findOne,Before,After等语法
- 当查找多个字段时支持生成DTO
- 支持生成接口和接口实现
- 生成的dao不再使用pojo作为param
- 修复byte类型的生成

1.4.2
- 支持oracle
- 配置使用useGenerateKey
- resultMap refid keyProperty if test的自动补全
- 支持java8 time里的类型
- 添加新图标
- 在通过方法名生成sql如果接口引入其他类型比如（java.util.Date)自动import到接口中
- bugfix 修复生成文件为null和initialize class com.ccnode.codegenerator.freemarker.TemplateUtil exception(大部分mac会出现的问题)

1.3
- 生成mybatis文件时可生成索引及选择是否需要默认值
- 生成mybatis文件加入insertSelective
- 在配置中可选择mybatis接口是否加上@Mapper注解
- 方法名生成sql 支持greaterThanOrEqualTo lessThanOrEqualTo betweenOrEqualto
- 支持resultMap refid跳转至定义及重构
- 支持xml中的方法名重构
- 修复module为空的警告


1.2
- 添加mapper与dao的相互跳转
- 使用alt+insert生成xml
- 添加方法名生成sql
- 添加方法名自动提示
----------------------------------
- 加入qq群  
542735979
![qqGroup](http://ogyxv3y5w.bkt.clouddn.com/qqgroup.png)


截图中的项目来自[https://github.com/gejun123456/codehelperPluginDemo](https://github.com/gejun123456/codehelperPluginDemo)

通过数据库来生成CRUD代码参考了 https://github.com/zouzg/mybatis-generator-gui 项目 已征得该项目作者同意


大家可以学习https://www.imooc.com/learn/924 来掌握更多使用Intellij的技巧 视频讲得很棒


[plugin]: https://plugins.jetbrains.com/plugin/9837





