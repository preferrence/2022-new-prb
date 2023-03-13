vector<pair<string, map<unsigned, vector<ClassicTBInfo *>>>> dpuSPMVec;

map<string, Stmt *> allPreCaledVEB;

InstanceConfItem *item = new InstanceConfItem();
(item->baseAddr)[idx] = addr; 
class InstanceConfItem{
    ...
    long long baseAddr[BASE_NUM];
    ...}

map<int, map<VarDecl *, ArrayInfo *>> allSPMArrayInfos;

vector<unsigned> subAddr;
vector<unsigned> newAllAddr;
newAllAddr.push_back(subAddr[d]);

收集数组引用点语句
map<VarDecl *, vector<ArraySubscriptExpr *>> tmpAllArrayRef;


ClassicThreadInfo *nowEBInfo;
struct ClassicThreadInfo {
  unsigned threadIdx;
  Dim3 threadCoo; // The coordinates of threads in the grid space
  map<VarDecl *, vector<map<VarDecl *, int>>> lowAllIdxVarValForSubStmt;
  map<VarDecl *, vector<int>> ebLowUpGap;
  map<VarDecl *, pair<vector<Stmt *>, vector<Stmt *>>> lowUpArraySubStmt;
};

map<VarDecl *, int> &allIdxVarVal /// 循环索引变量储存

