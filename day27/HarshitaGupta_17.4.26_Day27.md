# Problem


## Code (C++)
```cpp
class Solution {
public:
    int diameterOfBinaryTree(TreeNode* root) {
        int diam = 0;
        height(root, diam);
        return diam;
    }

    int height(TreeNode* node, int &diameter) {
        if (node == NULL){
           return 0;
        } 

        int leftH = height(node->left, diameter);
        int rightH = height(node->right, diameter);

        
        diameter = max(diameter, leftH + rightH);

        return max(leftH, rightH) + 1;
    }
};