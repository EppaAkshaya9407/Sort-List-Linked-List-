# Sort-List-Linked-List-
# Definition for singly-linked list.
# class ListNode:
#     def __init__(self, val=0, next=None):
#         self.val = val
#         self.next = next
class Solution:
    def sortList(self, head: Optional[ListNode]) -> Optional[ListNode]:
        if head is None or head.next is None:
            return head
        temp=head
        r=[]
        while temp:
            r.append(temp.val)
            temp=temp.next
        r.sort()
        d=ListNode(0)
        temp=d
        for i in r:
            temp.next=ListNode(i)
            temp=temp.next
        return d.next
