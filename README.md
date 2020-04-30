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



