# 약수의 합

def solution(n):
    answer = 0
    n = int(n)
    for i in range(1,n+1):
        if n % i  == 0:
            answer += i
    return answer

#print(solution(12))
#ㅡㅡㅡㅡㅡㅡㅡㅡㅡㅡㅡㅡ

def sumDivisor(num):
    # num / 2 의 수들만 검사하면 성능 약 2배 향상
    return num + sum([i for i in range(1, (num // 2) + 1) if num % i == 0])
