# python29
Alphabet Letters
n=int(input("Enter the size:"))
matrix=[[' ']*n for _ in range(n)]
ch=65
top,left=0,0
right,bottom=n-1,n-1

while top<=bottom and left<=right:
    for i in range(left,right+1):
        matrix[top][i]=chr(ch)
        ch+=1
        if ch>90:
            ch=65
    top+=1
    for i in range(top,bottom+1):
        matrix[i][right]=chr(ch)
        ch+=1
        if ch>90:
            ch=65
    right-=1
    for i in range(right,left-1,-1):
        matrix[bottom][i]=chr(ch)
        ch+=1
        if ch>90:
            ch=65
    bottom-=1
    for i in range(bottom,top-1,-1):
        matrix[i][left]=chr(ch)
        ch+=1
        if ch>90:
            ch=65
    left+=1
for row in matrix:
    for val in row:
        print(f"{val:2}",end=' ')
    print()

    




