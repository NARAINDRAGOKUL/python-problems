# python-problems rat problem
def calculate(r,unit,n,arr):
    if n == 0:
        return -1
    tot = r*unit
    foo = 0
    house = 0
    for house in range(n):
        foo += arr[house]
        if foo >= tot:
            break
    if tot > foo:
        return 0
    return house +1
r = int(input())
unit = int(input())
n = int(input())
arr = list(map(int,input().split()))
print(calculate(r,unit,n,arr))
