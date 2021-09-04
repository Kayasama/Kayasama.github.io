## 集合论
### 集合论发展史
- 1638年，天文学家**伽利略**提出问题：  
全体自然数与全体平方数，谁多谁少？  
这一问题为现代数学基础——集合论的诞生播下了种子。  
- 19世纪末德国数学家乔治康托创造了集合论
  
  - 自古希腊时代以来两千多年里，人类认识史上第一次给无穷建立起抽象的形式符号系统和确定的运算
  - 从本质上揭示了无穷的特性，使无穷的概念发生了一次革命性的变化，并渗透到所有的数学分支
  - 从根本上改造了数学的结构，促进许多新的分支，如实变函数论、代数拓扑、群论、泛函分析等
- 集合论体系
  - 朴素（Naive）集合论
  - 公理（Axiomatic）集合论

### 集合的表示方法
- **枚举法**：列出集合中全部元素或部分元素的方法。
  - 如：集合A用枚举法表示：A = {a,b,c,d}
  - 集合B用枚举法表示：B = {0,1,4,9,16...,n^2,...}
  - 说明：
    
    - 1. 枚举法适合表达一个集合仅含有限个元素，或一个集合的元素之间有明显的特定关系。
    - 2. 枚举表示法的优点是表示效果直观清晰，缺点是集合中元素过多时表达受到一定的局限。
    - 3. 例如集合A是52个大小写的英文字母构成的整体，如果用枚举法表示显然很繁琐
- **描述法**：通过刻划集合中元素所具备的某种特性来表示集合；表示方法：A={x|P(x)},通过谓词P概括集合元素的性质。

  - 说明：适合表达一个集合含有很多或无穷多个元素

- **归纳法**：由三部分组成：
  - 第一部分：**基础Base**
    - 指出某些最基本的元素属于某集合
  - 第二部分：**归纳Inductive**
    - 指出由基本元素造出新元素的方法
  - 第三部分：**极小性**
    - 指出该集合的界限
  - 示例：集合A以归纳法方式定义：
    - 1. 0和1都是A中的元素；
    - 2. 如果a，b是A中的元素，则ab、ba也是A中的元素；
    - 3. 有限次使用a),b)后得到的字符串都是A中的元素。
- **递归指定集合**：通过<font color=red>**计算规则**</font>定义集合中的元素（经典：等比、等差数列）
  - 示例:设a0=1,ai+1=2ai(i>=0),定义S={a0,a1,a2,...}={ak|k>=0},试写出集合S中的所有元素.
- 文氏图法2(Venn Diagram):利用平面上点的集合作成的对集合的图解;用平面上的圆形或方形表示一个集合.


### 幂集
一个集合的幂集数 = 2^n,元素都是集合形式存在.
重点:区分集合和元素,元素使用操作"隶属于",集合与集合之间的关系使用操作"包含"


### 集合的计算机表示
1. 以无序方式存储集合元素
   1. 计算集合间的并、交和差很耗时,因为每个操作都需大量工作用于搜索集合元素
2. 以任何顺序方式存储全集中的元素
   1. 这种集合表示方法使得集合的计算机操作简单
   2. 假设全集U是有限集(n元)
      1. 任意指定集合U元素的顺序
      2. 全集U的子集A表示为长度为ｎ的位串(Bit String)
      3. 使用位运算实现集合的交、差、并、补操作