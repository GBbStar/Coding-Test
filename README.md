[Ȳ�Ժ�] [���� 2:56] ���̽� sorted �Լ��� ���� ������ x[0]�� ���ָ�, ���̽� ���ݿ� ���� stable ������ �ȴ�
[Ȳ�Ժ�] [���� 3:00] ������ ������ ������, ������ ���� �� ����� �� �ִ� ���� : �������
[Ȳ�Ժ�] [���� 3:05] �Է� ������ ������ ���� ��� sys.stdin.readline �� ���� �����͸� �о�;� �Ѵ�
[Ȳ�Ժ�] [���� 6:59] ������ �������� ��� ����Ž���� ���డ��
[Ȳ�Ժ�] [���� 7:03] ���ڿ��� �Ǿ��ִ� ������ �ٷ� ������ִ� �Լ� eval()
[Ȳ�Ժ�] [���� 7:05] ���̽��� �⺻������ ���� ����. ���� ���縦 ���ؼ� copy.�� ���� ���� ���縦 ����ؾ� ��
[Ȳ�Ժ�] [���� 7:12] ���̽� �⺻�� 1�ʿ� 2õ�������ۿ� �ȵ�
[Ȳ�Ժ�] [���� 8:37] print('n'.join(result))
[Ȳ�Ժ�] [���� 9:33] queue = [(i, idx) for idx, i in enumerate(queue)]
2021�� 4�� 7�� ������
[Ȳ�Ժ�] [���� 11:16] import heapq

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
