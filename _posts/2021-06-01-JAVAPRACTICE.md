학생점수 입출력해보기

package ex;



import java.util.Scanner;



public class Exercise08 {



​	public static void main(String[] args) {

​		

​		boolean run = true;

​		int studentNum = 0;

​		int[]scores = null;

​		Scanner scanner = new Scanner(System.***in\***);

​		

​		while(run) {

​			System.***out\***.println("----------------------------------------");

​			System.***out\***.println("1.학생수 | 2.점수입력 | 3.점수리스트 | 4.분석 | 5.종료");

​			System.***out\***.println("----------------------------------------");

​			System.***out\***.print("선택> ");

​			

​			int selectNo = scanner.nextInt();

​			

​			

​			switch(selectNo) {

​				case 1:

​					System.***out\***.print("학생수> ");

​					studentNum = scanner.nextInt();

​					scores = new int[studentNum];

​					break;

​				case 2:	

​					for(int i = 0; i <scores.length; i++) {

​						System.***out\***.print("socres["+i+"]> ");

​						scores[i]=scanner.nextInt();

​					}

​					break;

​				case 3:

​					for(int i= 0; i < scores.length; i++){

​						System.***out\***.println("socres["+i+"]: "+scores[i]);

​					}

​					break;

​				case 4:

​					int max = 0;

​					int sum = 0;

​					double avg = 0.0;

​					

​					

​					for(int score : scores) {

​						sum+=score;

​						if(score > max) {

​							max = score;

​						}

​					};

​					avg = (double)sum /studentNum;

​					

​					System.***out\***.println("최고 점수: "+max);

​					System.***out\***.println("평균 점수: "+avg);

​					break;

​				case 5:

​					run = false;

​					break;

​			};

​		}

​		System.***out\***.println("프로그램 종료");

​	}



}

