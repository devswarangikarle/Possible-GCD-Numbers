# Possible-GCD-Numbers
 1) The sum a+b lies between l and r inclusive. 2) The greatest common divisor(GCD) of a and b isn't 1. are possible or not? If no such numbers exist, print "No" else print "Yes". Input contains two integers l and r (1 ≤ l ≤ r ≤ 10^6). Output Print "Yes" if it's possible to find two numbers satisfying both the conditions, "No" 

def find_numbers(l, r):
   
    def gcd(a, b):
        while b:
            a, b = b, a % b
        return a

    for a in range(2, r + 1):
        b = r - a
        if a > 1 and b > 1 and gcd(a, b) != 1:
            return "Yes"

    return "No"
l, r = map(int, input().split())
print(find_numbers(l, r))
