def ArmstrongNumber(num):
    order = len(str(num))
    return num == sum(int(digit)**order for digit in str(num))
def ArmstrongNumbersUpTon(n):
    return [num for num in range(1, n+1) if ArmstrongNumber(num)]
n = int(input("Enter the value of n: "))
print(f"Armstrong numbers from 1 to {n}: {ArmstrongNumbersUpTon(n)}")
