表示四元数的数据格式一共有三种，分别是: tf::Quaternion、geometry_msgs::Quaternion和Eigen::Quaterniond，他们的使用方法如下

**1 tf::Quaternion**
   初始化：
   > tf::Quaternion qua(qx, qy, qz, qw);  // 直接初始化 顺序是x y z w；<br>
   > tf::Quaternion qua; ///定义四元数;<br>
   > qua.setRPY(roll,pitch,yaw); //将欧拉角转换成四元数<br>
   取值 :
   > qua.w() = w;
   > qua.x() = x;
   > qua.y() = y;
   > qua.z() = z;

**２ geometry_msgs::Quaternion**
  初始化：
  取值  :
  > qua.w = w;
  > qua.x = x;
  > qua.y = y;
  > qua.z = z;

**3 Eigen::Quaterniond**
  初始化：
  >Quaterniond qua(1.0, 0.0, 0.0, 0.0); // 要注意Eigen中四元数赋值的顺序，实数w在首；但是实际上它的内部存储顺序是[x y z w]。实际上后面输出系数的时候也是按内部存储顺序输出
  取值  :
  > qua.w() = w;
  > qua.x() = x;
  > qua.y() = y;
  > qua.z() = z;
   