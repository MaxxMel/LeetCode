#include <iostream>
using namespace std;

struct ListNode {
    int val;
    ListNode *next;
    ListNode() : val(0), next(nullptr) {}
    ListNode(int x) : val(x), next(nullptr) {}
    ListNode(int x, ListNode *next) : val(x), next(next) {}
};

class Solution {
public:
    ListNode* addTwoNumbers(ListNode* l1, ListNode* l2) {
        ListNode* dummyHead = new ListNode(0);
        ListNode* current = dummyHead; 
        int carry = 0;

        while (l1 != nullptr || l2 != nullptr || carry != 0) {
            int sum = carry;
            if (l1 != nullptr) {
                sum += l1->val;
                l1 = l1->next;
            }
            if (l2 != nullptr) {
                sum += l2->val;
                l2 = l2->next;
            }
            
            carry = sum / 10;
            current->next = new ListNode(sum % 10);
            current = current->next; 
        }

        return dummyHead->next;
    }
};

int main() {
    ListNode l1_2(3);
    ListNode l1_1(4, &l1_2);
    ListNode l1(2, &l1_1);

    ListNode l2_2(4);
    ListNode l2_1(6, &l2_2);
    ListNode l2(5, &l2_1);

    Solution solution;
    ListNode* result = solution.addTwoNumbers(&l1, &l2);

  
    while (result != nullptr) {
        cout << result->val;
        if (result->next != nullptr) cout << " -> ";
        result = result->next;
    }
    cout << endl;

    return 0;
}
// medium 
