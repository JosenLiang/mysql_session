前提：

在mysql.odp里面有所有创建表的SQL语句，大家可以都执行一下；
然后请运行data.sql文件中的所有语句，这将向数据库添加一些数据；

作业如下：

现在在数据库中有四个表：
CUSTOMERS
CATEGORIES
PRODUCTS
PURCHASES

所有Customer购买Product的记录都保存在PURCHASES表中，其中包含Customer 的ID（CUSTOMER_ID）、Product的ID（PRODUCT_ID）、购买的数量（QUANTITY）、购买日期（CREATE_TIME）；
Product的价格保存在PRODUCTS表中（PRICE）；

假设这就是一个商场的数据库，包含了顾客、商品、交易信息；
现在商场有一个需求，我们想要得到每个月购买量最大的客户信息列表（包括：Customer ID、Customer Name、当月购买商品的总金额）；

所谓当月购买量是指 当月所有购买的商品的“数量乘以价格”的总和：SUM( QUANTITY * PRICE );
如果当月存在交易信息，则必须查出购买量最大的那个Customer；如果当月没有交易信息，可以不用管它；