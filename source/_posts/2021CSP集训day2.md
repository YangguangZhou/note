//在Linux下，x1,y1均为关键字，万能头和using namespace二选一

/*平板电视
1.平衡树*/
//平板电视#include<wxt/pb_ds/…….hpp>，不包含在万能头中
#include<ext/pb_ds/tree_policy.hpp>//平衡树
//#include<bits/extc++.h>在Dev中不可用
using namespace __gnu_pbds;//pbds需要开的命名空间
tree<long long,null_type,less<long long>,rb_tree_tag,tree_order_statistics_node_update> tr;
//（less在algorithm中）