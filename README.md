
## Reverse Single Linked List

**easy**

```java
/**
 * Definition for singly-linked list.
 * public class ListNode {
 *     int val;
 *     ListNode next;
 *     ListNode() {}
 *     ListNode(int val) { this.val = val; }
 *     ListNode(int val, ListNode next) { this.val = val; this.next = next; }
 * }
 */
class Solution {
    public ListNode reverseList(ListNode head) {
      if(head == null || head.next == null) return head;
      ListNode curr = head;
      ListNode next = head.next;
      head.next = null;
      while(true) {
        ListNode nextNext = next.next;
        next.next = curr;
        if(nextNext == null) {
          return next;
        }
        curr = next;
        next = nextNext;
      }
    }
}
```
