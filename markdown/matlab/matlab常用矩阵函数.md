#  matlab常用矩阵函数

## kron

求Kronecker积

用法 C=kron (A,B)

A为m×n矩阵，B为p×q矩阵，则C为mp×nq矩阵

结果为A中每个元素乘于B矩阵，形成一个大矩阵

[百度知道](https://zhidao.baidu.com/question/326548180880205405.html)



## reshape

重组矩阵,变换成i行j列的矩阵

用法 B=reshape(A,i,j)

A、B元素个数需相同,也就是说A矩阵的元素个数需为i*j个

总是先处理低维的，再处理高维的，比如要把4\*6的A变为6*4的B，就要先扫描A的第一列，扫描过程中**行数不断发生变化**，列数隔一段时间变化一次，这就是前面说的：先处理低维再处理高维（行是低维，列比行高一维）

[CSDN](https://blog.csdn.net/xtingjie/article/details/70991097)



## sparse&full

创建稀疏矩阵

用法1 B=sparse(A）

将矩阵A转化为稀疏矩阵的形式，即矩阵A中任何零元素去除，非零元素及其下标（索引）组成矩阵B。

用法2 B = sparse(i,j,s,m,n,nzmax)

由i,j,s三个向量创建一个m*n的稀疏矩阵，并且最多含有nzmax个元素

i,j中每一行元素分别代表稀疏矩阵中元素的行和列，s中表示对应的值，m*n为稀疏矩阵的大小，nzmax代表稀疏元素的数组大小

full为把稀疏矩阵转换为全矩阵

用法 A=full(B)

[CSDN](https://blog.csdn.net/diedie4488/article/details/101593894)



## union

对两个矩阵元素求并集

C = union(A,B)