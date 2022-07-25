//比赛时可通过判断n的范围，分成多个subtask来做（确保较小的数据用暴力可以过，与较大数据范围的互不干扰）

//优先队列（从大到小）
#include<queue>
priority_queue<int> q;

//从小到大
priority_queue<int,vector<int>,greater<int> > q;

//结构体从小到大
struct heap{
    int id,val;
    bool operator <(const heap &rhs)const{
        return rhs.id<id;
    }
};
priority_queue<heap> q;

//树状数组
int lowbit(int x){
    return x&-x;
}

//并查集时间复杂度
o(α(n))≈o(log log n)

//并查集
int find(int x){
    return fa[x]==x?x:fa[x]=find(fa[x]);
}

//集合
#include<set>
set <int> s;
s.insert(a)//加入新元素（复杂度log n）
s.erase(a)//删除元素
s.find(a)//查找元素
s.size()//长度
*s.begin()//最小元素
*--s.end()//最大元素
for(auto i:s){}//遍历(C++11)


//用set去重
set <int> s;
long long a[]={1,2,3,4,5,2,3,4,1,2,5,2,3,5,5,1,4,2,1,3,0,123456789}
int main(){       
	for(int i=0;i<20;i++){
        s.insert(a[i]);
    }
    return 0;
}

//string
string a="luoguluogu";
int x=a.find("gu");//返回该字符串第一次出现的位置，找不到则返回string::npos
//结果：x=3

//自动类型
auto a;

//map（可以用于判断是否相同）（可用任意类型做下标）（根据key的值进行排序，如是string，按位来比，与长度无关）
#include<map>
map <key,value> s;//key为键值，value是权值，均为类型
s[a]=b//加入新映射
s[a]//直接访问映射
s.clear()//清空
//遍历（C++11）
for(auto i:s){
    cout<<i.first<<" ";
    cout<<i.second<<endl;
}
//例
map <string,int> mp;
mp["bcd"]=3;
mp["abc"]=1;
mp["cde"]=2;
for(auto i:mp){
    cout<<i.first<<" ";
    cout<<i.second<<endl;
}
/*输出结果：
abc 1
bcd 3
cde 2*/

//sort
//可以排序字符串（将所有字符ASCII码相加（“”=0），即长度短的在前）