# 13-05-22-ass-1
import math
class Solution:
    def isPrime(self,n):
        seive=[True for i in range(n+1)]
        seive[0]=seive[1]=False
        x=int(math.sqrt(n))
        for i in range(2,x+1):#i=3<3
            if seive[i]:#seive[2]=True
                for j in range(i*i,n+1,i):#6<6,2
                    seive[j]=False
            if seive[n]:
                return 1
            else:
                return 0

Output:
Output:-
For input- 5
Your output-1
Expected output-1
