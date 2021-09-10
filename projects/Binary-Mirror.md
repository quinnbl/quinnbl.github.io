---
layout: project
type: project
image: images/binsquare.jpg
title: Binary Mirror
permalink: projects/Binary-Mirror
# All dates must be YYYY-MM-DD format!
date: 2021-05-12
labels:
  - C
  - Recursion
summary: A program I developed for EE 367 which checks if a binary tree is a mirror of itself.
---

<img class="ui image" src="{{ site.baseurl }}/images/bin.png">

Binary Mirror is a program I developed which takes a binary tree as an input and determines if the tree on the left side of the root matches the tree on the right side of the root. It uses recursion and two node pointers to go through the tree each side in the same way and check if there are nodes in the same places and whether they are the same nodes or not. In the helper function I implemented for recursion purposes, the left searching pointer would focus priority on going to the left, then if it had already visited everything to the left it would go to the right. In a similar way, the right searching pointer would search to the right unless it could no longer go right, then head back and search to teh left. At every new node, the left and right searching pointers would check themselves against each other. The function would then return false (0) if they did not match, or keep going until the whole tree was searched. If the whole tree was searched without incident, the return value would be true (1).

Here is the important part of the code:

```c
int mirror(struct node* root)
{
    if (root->left->val == root->right->val)
    {
        return mirror_helper(root->left, root->right);
    }
    else
    {
        return 0;
    }
}

/*Quinn's helper*/
int mirror_helper(struct node * left, struct node * right)
{
    int solution = 1;

    if (left->left == NULL && right->right != NULL) return 0;
    if (left->left != NULL && right->right == NULL) return 0;
    if (left->right == NULL && right->left != NULL) return 0;
    if (left->right != NULL && right->left == NULL) return 0;

    if (left->left != NULL && right->right != NULL)
    {
        if (left->left->val == right->right->val)
        {
            solution = mirror_helper(left->left, right->right);
            if (solution == 0) return solution;
        }
        else 
        {
            return 0;
        }
    }

    if (left->right != NULL && right->left != NULL)
    {
        if (left->right->val == right->left->val)
        {
            solution = mirror_helper(left->right, right->left);
            if (solution == 0) return solution;
        }
        else
        {
            return 0;
        }
    }

    return solution;
}
```

