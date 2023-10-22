# 20231021 TIL 반복문 while / 배수 / 가까운수

[문제]
1에서 200 사이의 숫자 중 다음 조건에 맞는 숫자를 출력하시오.


조건) 6의 배수 중에서 100에 가장 가까운 수를 출력하시오.


[정답] 102

  		
```java		public class _08연습문제 {
		public static void main(String[] args) {
				
		int limit = 100; 
		int answer = 0; 
		int i = 1;
		while ( i <= 200) {
			if(i % 6 == 0 && i <= limit) { 	
				answer = i;
				}
			i += 1;
			}
		System.out.println("answer = " + answer);
		int nextAnswer =  answer + 6;
		System.out.println("nextAnswer = " + nextAnswer);

		if(limit - answer < limit - nextAnswer) {
		System.out.println(answer); 
		}else {
		System.out.println(nextAnswer); 
				}
			}
		}
```


# check point
여기서 고민해봐야할게 무조건 100이하라고 했기때문에 100보다 작은수 밖에 나올수밖에 없다.


잘 생각해보면 96 다음에 6의 배수가 102가 있다. 100을 가운데로 두고 보면 96과 100의 차이는 4이고, 102와 100의 차이는 2이다.


사실상 100이라는 숫자에 더 가까운 숫자는 102이다. 여기서 끝나면 안되기 때문에 하나의 변수(nextAnswer)를 더 만든다. 즉 96 다음 숫자까지도 고려





	




