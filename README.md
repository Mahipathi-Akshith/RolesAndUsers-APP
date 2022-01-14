# RolesAndUsers-APP

#include<iostream>
#include<string>
using namespace std;

class Node
  
{
  
public:
  
    string pos;
    Node *left;
    Node *right;

    Node(string pos)
    {
        this->pos = pos;
        left = right = NULL;
    }
};

Node *buildRoot()
  
{
  
    cout << "Enter Root Role Name: ";
    string str;
    cin >> str;

    Node *n = new Node(str);
    n->left = NULL;
    n->right = NULL;
    return n;
}

Node *buildtree()
  
{
  
    cout << "Enter sub role name :";
    string str;
    cin >> str;

    Node *n = new Node(str);
    n->left = NULL;
    n->right = NULL;
    return n;
}

void printtree(Node *root)
  
{
  
    if (root == NULL)
    {
        return;
    }

    cout << root->pos;
}

int main()
  
{
  
    Node *root = buildRoot();
    printtree(root);

    cout << "1.Add Sub Roles\n";
    Node *sub = buildtree();
    printtree(sub);
    return 0;
}
