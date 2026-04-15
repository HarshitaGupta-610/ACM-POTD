# Problem


## Code (C++)
```cpp
class Solution {
public:
    int remaining; 
    int answer;

    void inorder(TreeNode* root) {
        if (root == NULL || remaining == 0) {
            return;
        }

        inorder(root->left);

        remaining--;
        if (remaining == 0) {     
            answer = root->val;
            return;
        }

        inorder(root->right);
    }

    int kthSmallest(TreeNode* root, int k) {
        remaining = k;
        inorder(root);
        return answer;
    }
};
