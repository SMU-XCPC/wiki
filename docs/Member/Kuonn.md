# kuonn

## 线段树板子

### 最大值

```cpp


#include<iostream>
#include <cstring>
#include <algorithm>
//#define int long long
using namespace std;

const int N = 500010;
int w[N];
int n,m;

struct node{
    int l,r;
    int sum,lmax,rmax,tmax;
}tree[N*4];

void push_up(node &i,node &l,node &r){
    i.sum = l.sum + r.sum;
    i.lmax = max(l.lmax, l.sum + r.lmax);
    i.rmax = max(r.rmax, r.sum + l.rmax);
    i.tmax = max(max(l.tmax, r.tmax), l.rmax + r.lmax);
}

void push_up(int i){
    push_up(tree[i],tree[i<<1],tree[i<<1|1]);
}

void build(int i,int l,int r){
    if(l==r) tree[i]={l,r,w[l],w[l],w[l],w[l]};
    else{
        tree[i]={l,r};
        int mid=l+r>>1;
        build(i<<1,l,mid);
        build(i<<1|1,mid+1,r);
        push_up(i);
    }
}

void add(int i,int dis,int k){
    if(tree[i].l==dis&&tree[i].r==dis) tree[i]={dis,dis,k,k,k,k};
    else{
        int mid=tree[i].l+tree[i].r>>1;
        if(dis<=mid) add(i<<1,dis,k);
        else add(i<<1|1,dis,k);
        push_up(i);
    }
}

node query(int i,int l,int r){
    if(tree[i].l>=l&&tree[i].r<=r){
        return tree[i];
    }else{
        int mid=tree[i].l+tree[i].r>>1;
        if(r<=mid) return query(i<<1,l,r);//忘记写返回值的后果就是溢出
        else if(l>mid) return query(i<<1|1,l,r);
        else{
            node res;
            auto left=query(i<<1,l,r);
            auto right=query(i<<1|1,l,r);
            push_up(res,left,right);
            return res;
        }
    }
}

int main(){
    cin >> n >> m;
    //memset(w,0,sizeof w);
    for(int i=1;i<=n;i++) cin >> w[i];
    build(1,1,n);
//    for(int i=1;i<=n;i++) cout << w[i] << " ";
//    cout << "\n";
    while(m--){
        int op,x,y;
        cin >> op >> x >> y;
        if(op==1){
            if(x>y) swap(x,y);
            cout <<  query(1,x,y).tmax << "\n";
        }else add(1,x,y);
    }
    return 0;
}

```

