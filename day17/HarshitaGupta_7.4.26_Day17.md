# Problem


## Code (C++)
```cpp
class MyStack {
public:
queue<int>q;
    MyStack() {
        
    }
     
    void push(int x) {
        q.push(x);
        int n = q.size();
        if(n>1){
            for(int i = 0; i < n-1 ; i++){
            int f = q.front();
            q.push(f);
            q.pop();
            }
        }
    }
    
    int pop() {
       if(q.empty()){
        return -1;
       }
        else{
            int a = q.front();
            q.pop();
            return a;

        }
    }
    
    int top() {
        if(q.empty()){
        return -1;
       }
       else{
        return q.front();
       }
    }
    
    bool empty() {
      int n = q.size();
        if(n == 0){
            return true;
        }
        else{
            return false;
        }
    }
};
