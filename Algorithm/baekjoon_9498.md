## 문제 :: if 문  
 시험 점수를 입력받아 90 ~ 100점은 A, 80 ~ 89점은 B, 70 ~ 79점은 C, 60 ~ 69점은 D, 나머지 점수는 F를 출력하는 프로그램을 작성하시오.  
## 코드
 ```
 public static void main(String[] args) {
  Scanner scan = new Scanner(System.in);
	
	int score;
	score = scan.nextInt();
	if(0<=score && score <=100) {
		if(90<=score && score<=100) {
			System.out.println("A");
		}else if(80<= score && score <=89) {
			System.out.println("B");
		}else if(70<= score && score<=79) {
			System.out.println("C");
		}else if(60<=score && score<=69) {
			System.out.println("D");
		}else {
			System.out.println("F");
		}
	}else {
		System.out.println("에러입니다.");
	}
}

 ```  
 
## 정답
<img width="719" alt="스크린샷 2020-07-03 오후 3 42 07" src="https://user-images.githubusercontent.com/33210124/86440876-38693200-bd46-11ea-940c-1cd26be14b81.png">
