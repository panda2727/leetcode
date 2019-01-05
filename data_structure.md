# List
## List-Search(L, k)
```
x = L.head
while x != NIL & x.key != k
	x = x.next
return x
```

## List-Insert(L, x)
```
x.next = L.head
if L.head != NIL
	L.head.prev = x
L.head = x
x.prev = NIL
```

## List-Delete(L, x)
```if x.prev != NIL
    x.prev.next = x.next
else L.head = x.next
if x.next != NIL
    x.next.prev = x.prev
```

## List-Insert(L, x) # use the dummy head
```
x.next = L.nil.next
L.nil.next.prev = x
L.nil.next = x
x.prev = L.nill
```
