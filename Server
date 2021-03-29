```
package tcp;
 
import java.util.Scanner;
 
public class Server {
    public static void main(String arg[])
    {
        Scanner sc = new Scanner(System.in);//숫자 받기

        
        Mariadb data = new Mariadb(); //마리아db클래스를 불러오기위한 객체
         
	    ServerThread st = new ServerThread();//서버 스레드 서버는 게속해서 사용자의 접속을 받음  
	    st.start();      
        
        try {       
            while(true) //로그 출력 삭제 입력받아서 실행
            {
                System.out.println("1: 로그 출력 2: 로그 삭제");
                System.out.print("번호 입력: \n");
                int a =sc.nextInt();
               
                switch (a) {
                case 1 :
                	System.out.println("로그 출력");
                	data.select();
                	break;
                case 2 :
                	System.out.println("로그 삭제");
                	data.delete();
                	break;
                default: 
                	System.out.println("없는 번호임 ㅠ");
                }
            }
        }catch(Exception e) { 
        };
        System.out.println("db 종료");//자원누수때문에 종료시 db종료
        data.end();
    }
}


```
