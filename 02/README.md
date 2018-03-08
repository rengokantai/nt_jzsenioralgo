Nearest exit:
lc 286
walls and gates
```
public class Solution{
  static final int INF = 2147483467;
  int n,m;
  public void wallsAndGates(int[][] rooms){
    n=rooms.length;
    if(n==0)return;
    m=rooms[0].length;
    int dx[] ={0,1,0,-1};
    int dy[]={1,0,-1,0};
    Queue<Integer> qx=new LinkedList<>();
    Queue<Integer> qy=new LinkedList<>();
    for(int i=0;i<n;i++){
      for(int j=0;j<m;j++){
        if(rooms[i][j]==0){
          qx.add(i);
          qy.add(j);
        }
      }
    }
    
    while(!qx.isEmpty()){
      int ox=qx.poll();
      int oy=qy.poll();
      for(int i=0;i<4;i++){
        int nx= ox+dx[i];
        int ny= oy+dy[i];
        if(0<=nx && nx<n&&0<=ny&&ny<m&&rooms[nx][ny]==INF){
          qx.add(nx);
          qy.add(ny);
          rooms[nx][ny]=rooms[ox][oy]+1;
        }
      }
    }
  }
}
```

lc 254
Factor combinations
```
public class Solution{
  List<List<Integer>> ans= new ArrayList<>();
  List<Integer> ans_item = new ArrayList<>();
  void dfs(int lastF,int remain){
    if(!ans_item.isEmpty()){
      ans_item.add(remain);
      ans.add(
    }
    
    for(int
  }
  
  
  public List<List<Integer>> getFactors(int n){
    dfs(2,n);
    return ans;
  }
}
```
