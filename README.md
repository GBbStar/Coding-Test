[황규빈] [오후 2:56] 파이썬 sorted 함수에 람다 기준을 x[0]로 해주면, 파이썬 성격에 의해 stable 정렬이 된다
[황규빈] [오후 3:00] 데이터 개수는 많으나, 범위가 좁을 때 사용할 수 있는 정렬 : 계수정렬
[황규빈] [오후 3:05] 입력 데이터 개수가 많을 경우 sys.stdin.readline 을 통해 데이터를 읽어와야 한다
[황규빈] [오후 6:59] 범위가 한정적인 경우 완전탐색을 수행가능
[황규빈] [오후 7:03] 문자열로 되어있는 계산식을 바로 계산해주는 함수 eval()
[황규빈] [오후 7:05] 파이썬은 기본적으로 얉은 복사. 깊은 복사를 위해선 copy.을 통해 직접 복사를 명령해야 함
[황규빈] [오후 7:12] 파이썬 기본은 1초에 2천만정도밖에 안됨
[황규빈] [오후 8:37] print('n'.join(result))
[황규빈] [오후 9:33] queue = [(i, idx) for idx, i in enumerate(queue)]
2021년 4월 7일 수요일
[황규빈] [오전 11:16] import heapq

def solution(scoville, K):
    heap  = []
    
    answer = 0
    for i in range(len(scoville)):
        heapq.heappush(heap, scoville[i])
    
    while heap[0] < K:
        if len(heap) <= 1:
            return -1

        answer += 1
        temp1 = heapq.heappop(heap)
        temp2 = heapq.heappop(heap)
        heapq.heappush(heap, temp1 + temp2*2)
            
    
    return answer
