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
