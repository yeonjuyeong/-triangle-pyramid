# -triangle-pyramid

### triangle

```java
import java.util.Scanner;
public class Sungil21110_Test05 {

	public static void main(String[] args) {
		// TODO Auto-generated method stub

		Scanner sc = new Scanner(System.in);
		
		int n;
		
		System.out.println("직각삼각형 출력합니다");
		
		do {
			System.out.print("몇단 직각삼각형입니까?");
			n = sc.nextInt();
		}while(n <= 0);
		for(int i=1; i<=n; i++) {
			for (int j=1; j<=n-i; j++)
				System.out.print("");
			for(int a=1; a<(i-1)*2+1;a++) {
			System.out.print("*");
			}			
			System.out.println();
		}
	}

}
```
### 실행화면
![image](https://user-images.githubusercontent.com/123055714/224196982-7820a91b-dbdc-405a-acd9-10f33eeee7e2.png)


### Pyramid

```java
import java.util.Scanner;
public class Sungil21110_Test06 {

	public static void main(String[] args) {
		// TODO Auto-generated method stub
		Scanner sc = new Scanner(System.in);
		int i,j,n,k;
		do {
			System.out.println("몇단의 피라미드를 만들까요?");
			n = sc.nextInt();
		}while(n<=0);
		
		for(i=0;i<n;i++) {
			for(j=1;j<n-i;j++) {
				System.out.print(" ");
			}
			for(k=0;k<i*2+1;k++) {
				System.out.print("*");
			}
			System.out.println();
		}
	
	}

}
```

## 설명
Scanner로 값을 입력받고 만약 1,2같은 수가 아니라 -1,-2같은 수라면 다시 질문하도록 do while문을 만들었다.
```java
import java.util.Scanner;
public class Sungil21110_Test06 {

	public static void main(String[] args) {
		// TODO Auto-generated method stub
		Scanner sc = new Scanner(System.in);
		int i,j,n,k;
		do {
			System.out.println("몇단의 피라미드를 만들까요?");
			n = sc.nextInt();
		}while(n<=0);

```

for문으로 피라미드를 만들기 위해서는<br>
--0<br>
-000<br>
00000<br>
이런식으로 공백을 써서 별의 줄을 맞춰야하는데
공백의 식으로는 전체층-현재층인데 for문으로 만들면 이렇게 나온다
```java
for(j=1;j<n-i;j++) {
	System.out.print(" ");
	}
```
전체층(n)-현재층(i) 이런식으로 만들 수 있다. 공백은 해결되었으니 이제 "*"을 만들면되는데
별의 식은 (현재층-1)*2+1로 for문으로 보면 이렇게 나온다.
```java
			for(k=1;k<=(i-1)*2+1;k++) {
				System.out.print("*");
			}
```
(1-1)*2+1은 1로 별 1개가 나오고
(2-1)*2+1은 3으로 별 3개가 나온다.그리고 이작업을 b번만큼 반복시키면
```java
for(i=0;i<=n;i++) {
			for(j=1;j<=n-i;j++) {
				System.out.print(" ");
			}
			for(k=1;k<=(i-1)*2+1;k++) {
				System.out.print("*");
			}
			System.out.println();
		}
```
이렇게 나온다

### 실행화면
![image](https://user-images.githubusercontent.com/123055714/224196534-150470ba-3597-4d93-b27d-394e704aa699.png)
