# ZTE-Homework
15 practice items writen in Java

No.1

public class EvenNumberInTen{

     public static void main(String []args){
         System.out.println("10以内的偶数为：");
         for(int i = 0; i<=10; i++){
             if((i%2) == 0){
                 System.out.println(i);
             }
         }
     }
}



No.2

public class Fibonacci{

     public static void main(String []args){
         System.out.println("100以内的斐波那契额数列为：");
         int sum = 0;
         for(int i = 0; i<=100; i++){
             if(i == 0){
                 System.out.println(i);
             }else if(i == 1){
                 System.out.println(i);
             }else{
                 sum = sum + i;
                 if(sum > 100){
                 break;
                }
                 System.out.println(sum);
             }
         }
     }
}


No.3

import java.util.Scanner;
import java.util.HashMap;
public class Year_Month_Day{

     public static void main(String []args){
         HashMap<Integer, Integer> map1 = new HashMap<>();
         HashMap<Integer, Integer> map2 = new HashMap<>();
         map1.put(1,31);
         map1.put(2,28);
         map1.put(3,31);
         map1.put(4,30);
         map1.put(5,31);
         map1.put(6,30);
         map1.put(7,31);
         map1.put(8,31);
         map1.put(9,30);
         map1.put(10,31);
         map1.put(11,30);
         int index = 0;
         
         Scanner sc = new Scanner(System.in);
         System.out.println("请输入年份：");
         
         int y = sc.nextInt();
         System.out.println("请输入月份：");
         int m = sc.nextInt();
         System.out.println("请输入日期：");
         int d = sc.nextInt();

         int sum = 0;
         if((y%100) == 0){
             if((y%400) == 0){
                 index = 1;
             }
         }else if((y%4) == 0){
             index = 1;
             
         }
         for(int i = 1; i <= m-1; i++){
             sum = sum + map1.get(i);
         }
         sum = sum + d;
         if(m > 2 && index == 1){
             sum = sum + index;
         }
         System.out.println(sum);
         
     }
}


No.4

import java.util.Scanner;
import java.util.HashMap;
import java.lang.Math;
public class NarcissisticNumber{

     public static void main(String []args){
         System.out.println("所有的“水仙花数”为：");
         for(int i = 100; i <= 999; i++){
             int a = Integer.parseInt(String.valueOf(i).substring(0,1));
             int b = Integer.parseInt(String.valueOf(i).substring(1,2));
             int c = Integer.parseInt(String.valueOf(i).substring(2,3));
             int comparenumber = (int)(java.lang.Math.pow(a,3) + java.lang.Math.pow(b,3) + java.lang.Math.pow(c,3));
             if(i == comparenumber){
                 System.out.println(i);
             }import java.util.Scanner;
import java.util.HashMap;
import java.lang.Math;
public class BounceBall{

     public static void main(String []args){
         System.out.println(第10次落地经过的路程为：);
         double highStart = 100;
         double longsum = 0;
         for(int i = 1; i = 10; i++){
             double mid = highStartjava.lang.Math.pow(2,i-1);
             longsum = longsum + mid2;
             
         }
         longsum = longsum + highStart;
         System.out.println(longsum);
         System.out.println(第10次谈起的高度为：);
         System.out.println(highStartjava.lang.Math.pow(2,10));

     }
}


No.5

import java.util.Scanner;
import java.util.HashMap;
import java.lang.Math;
public class BounceBall{

     public static void main(String []args){
         System.out.println(第10次落地经过的路程为：);
         double highStart = 100;
         double longsum = 0;
         for(int i = 1; i = 10; i++){
             double mid = highStartjava.lang.Math.pow(2,i-1);
             longsum = longsum + mid2;
             
         }
         longsum = longsum + highStart;
         System.out.println(longsum);
         System.out.println(第10次谈起的高度为：);
         System.out.println(highStartjava.lang.Math.pow(2,10));

     }
}
             
         }

     }
}


No.6

public class Peach{
    public static void main(String []args){
        System.out.println("第一天摘的桃子个数为：");
        int a = peach(10);
        System.out.println(a);
    }
    public static int peach(int n){
        if(n == 1){
            return 1;
        }else{
            return (peach(n-1) + 1) * 2;
        }


    }
}


No.7
import java.util.Iterator;
import java.util.HashSet;
public class DifferentNumber {
    public static void main(String[] args){
        HashSet<Integer> number = new HashSet<>();
        for(int i = 1; i <= 4; i++){
            for(int j = 1; j <= 4; j++){
                for(int k = 1; k <= 4; k++){
                    if(i != k && k != j && i != j){
                        int test = i*100 + j*10 + k;
                        number.add(test);
                    }

                }
            }
        }
        int numbersize = number.size();
        System.out.println("由1，2，3，4组成的数字不重复的不同三位数有" + numbersize + "个");
        System.out.println("它们分别是：");
        Iterator a = number.iterator();
        while(a.hasNext()){
            System.out.println(a.next());
        }
    }
}


No.8
public class multiplicationTalbe99 {
    public static void main(String[] args){
        for(int i = 1; i <= 9; i++){
            for(int j = 1; j <= i; j++) {
                System.out.print(j + "*" + i + "=" + i * j + ";" + " ");
            }
            System.out.println();
        }

    }
}


No.9
import java.util.Scanner;

public class charnumber {
    public static void main(String[] args){
        System.out.println("请输入一串字符");
        Scanner sc = new Scanner(System.in);
        String charline = sc.nextLine();
        char[] chararray = charline.toCharArray();
        int charnumber = chararray.length;
        int numbersum = 0;
        int charsum = 0;
        int spacesum = 0;
        int othersum = 0;
        for(int i = 0; i < charnumber; i++){
            if((chararray[i] >= 'a' && chararray[i] <= 'z') || (chararray[i] >= 'A' && chararray[i] <= 'Z')){
                charsum++;
            }else if(chararray[i] >= '0' && chararray[i] <= '9' ){
                numbersum++;
            }else if(chararray[i] == ' '){
                spacesum++;
            }else{
                othersum++;
            }
        }
        System.out.println("该字符串中字母的个数为：" + charsum);
        System.out.println("该字符串中数字的个数为：" + numbersum);
        System.out.println("该字符串中空格的个数为：" + spacesum);
        System.out.println("该字符串中其他字符的个数为：" + othersum);
    }
}


No.10
public class teamlist {
    public static void main(String[] args){
        char[] team1 = {'a','b','c'};
        char[] team2 = {'x','y','z'};
        int[] teamone = {1,1,1,3};
        int[][] relation = {{0,1,1,2,0},{1,1,1,3,0},{0,0,1,1,0}};//行表示第一队的队员，列表示第二队的队员，前三列0表示确定不比赛，第四列表示不确定的数量，第五列表示该队员的对手序号

        while(teamone[3] != 0){
            for(int i = 0; i <= 2; i++){
                if((teamone[i] != 0) && (relation[i][3] == 1)){
                    for(int j = 0; j <= 2; j++){
                        if(relation[i][j] == 1){
                            for(int k = 0; k <= 2; k++){
                                relation[k][j] = 0;
                                relation[k][3]--;
                            }
                            relation[i][j] = 1;
                            relation[i][4] = j;
                        }
                    }
                    teamone[i] = 0;
                    teamone[3]--;
                }
            }
        }
        System.out.println("比赛对阵名单为");
        for(int i = 0; i <= 2; i++){
            System.out.println(team1[i] + "-" + team2[relation[i][4]]);
        }
    }
}


No.11

