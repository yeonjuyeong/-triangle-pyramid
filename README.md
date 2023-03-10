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
		int i;
		int j;
		int k;
		int n;
		do {
			System.out.println("몇단의 피라미드를 만들까요?");			
			n = sc.nextInt();
		}while(n<=0);
		
		for(i=0;i<=n;i++) {
			for(j=1;j<=n-i;j++) {
				System.out.print(" ");
			}
			for(k=1;k<=(i-1)*2+1;k++) {
				System.out.print("O");
			}
			System.out.println();
		}
	
	}

}
```

### 실행화면
![image](https://user-images.githubusercontent.com/123055714/224196534-150470ba-3597-4d93-b27d-394e704aa699.png)
