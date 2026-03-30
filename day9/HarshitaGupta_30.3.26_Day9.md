# Problem


## Code (C++)
```cpp
class Solution {
public:
    bool hasCycle(ListNode *head) {
        unordered_map<ListNode* , int>mpi;
        ListNode* temp = head;
        while(temp != NULL){
            if(mpi.find(temp) != mpi.end()){
                return true;
            }
            mpi[temp] = 1;
            temp = temp -> next;
           
        }
         return false;
    }
};