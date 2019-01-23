# 021_merge_two_sorted_list.py
```
class Solution(object):
   def mergeTwoLists(self, l1, l2):
       # dummy head
       pos = dummyHead = ListNode(-1)
       while l1 is not None and l2 is not None:
           if l1.val <= l2.val:
	       pos.next = l1
	       l1 = l1.next
	   else:
	       pos.next = l2
	       l2 = l2.next
	   pos = pos.next
        # merge residual l1
	if l1 is not None:
	    pos.next = l1
	# merge residual l2
	if l2 is not None:
	    pos.next = l2
	return dumyHead.next

```

# Merge(_A_, _p_, _q_, _r_)
```
n_{1} = q - p + 1
n2 = r - q # r - (q - 1) + 1
Let L[1 .. n1 + 1] and R[1.. n2 + 1] be new arrays
for i = 1 to n1
    L[i] = A[p + i -1]
for j = 1 to n2
    R[j] = A[q + j]
L[n1 + 1] = \infty
R[n2 + 1] = \infty
i = 1
j = 1
for k = p to r
    if L[i] <= R[i]
        A[k] = L[i]
	i = i + 1
    else A[k] = R[i]
        j = j + 1
```

# List
## List-Search(*L*, *k*)
```
x = L.head
while x != NIL & x.key != k
	x = x.next
return x
```

## List-Insert(*L*, *x*)
```
x.next = L.head
if L.head != NIL
	L.head.prev = x
L.head = x
x.prev = NIL
```

## List-Delete(*L*, *x*)
```
if x.prev != NIL
    x.prev.next = x.next
else L.head = x.next
if x.next != NIL
    x.next.prev = x.prev
```

## List-Insert(*L*, *x*) # use the dummy head
```
x.next = L.nil.next
L.nil.next.prev = x
L.nil.next = x
x.prev = L.nill
```
