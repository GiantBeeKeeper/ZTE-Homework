# ZTE-Homework
15 practice items writen in Java

No.1*************************
从大到小输出10以内的偶数。

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



No.2*************************
输出小于100的斐波那契数列。

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


No.3*************************
输入某年某月某日，判断这一天是这一年的第几天。

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


No.4*************************
打印出所有的“水仙花数”，所谓“水仙花数”是指一个三位数，其各位数字立方和等于该数本身。

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


No.5*************************
一球从100米高度自由落下，每次落地后反跳回原高度的一半，再落下，求它在第10次落地时，共经过多少米？第10次反弹多高？

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


No.6*************************
猴子吃桃问题：猴子第一天摘下若干个桃子，当即吃了一半还不过瘾，又多吃了一个，第二天早上又将剩下的桃子吃了一半，又多吃了一个。以后每天早晨都吃了前一天的一半零一个。到第10天早上再想吃时，见只剩下一个桃子，求第一天共摘了多少？

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


No.7*************************
有1、2、3、4这4个数字，能组成多少个互不相同且无重复数字的三位数？都是多少？

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


No.8*************************
打印输出9 * 9乘法表

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


No.9*************************
输入一行字符，分别统计出英文字母、空格、数字和其他字符的个数

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


No.10*************************
两个乒乓球队进行比赛，各处三人。甲队为a、b、c三人，乙队为x、y、z三人。已经抽签决定比赛名单。有人向队员比赛的名单。a说他不和x比，c说他不和
x、z比，请编程找出三队赛手的名单。

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


No.11*************************
人们书的文字常常超过屏幕的最大宽度，编写一个程序，在一个文本文件中查找长度大于80个字符的文本行。从接近80个字符的单词断行，把剩余文件插入到下一行
处，程序执行完毕后，应该没有80个字符的文本行了。

import java.io.File;
import java.io.BufferedReader;
import java.io.FileReader;
import java.io.IOException;
import java.util.Scanner;
import java.util.LinkedList;

public class textline {
    public static void main(String[] args){
        System.out.println("请输入文本文件的地址：");
        Scanner sc = new Scanner(System.in);
        String filename = sc.nextLine();
        System.out.println("文本内容为：");
        //String[] wordarray = readFilecontent(filename).split(" ");
        LinkedList<String> linearr = readFilecontent(filename);
        for(int i = 0; i < linearr.size(); i++){
            cutlong(linearr.get(i), i, linearr);
        }
        for(String o : linearr){
            System.out.println(o.length());
            System.out.println(o);
        }


    }
    public static LinkedList<String> readFilecontent(String fileName){
        File file = new File(fileName);
        BufferedReader reader = null;
        //StringBuffer textstr = new StringBuffer();
        LinkedList<String> strlist = new LinkedList<>();
        try{
            reader = new BufferedReader(new FileReader(file));
            String tempStr;
            while((tempStr = reader.readLine()) != null){
                strlist.add(tempStr);
                //textstr.append(tempStr);
                //reader.close();
                //return textstr.toString();

            }
        }catch(IOException e){
            e.printStackTrace();
        }finally{
            if(reader != null){
                try{
                    reader.close();
                }catch(IOException e1){
                    e1.printStackTrace();
                }
            }
        }
        return strlist;
    }


    public static void cutlong(String str,int index, LinkedList<String> linkedline){
        if(str.length() > 80){
            String[] words = str.split(" ");
            int sum = words[0].length();
            String str1 = words[0];
            String strmid  = null;
            int eightyindex = 1;
            while(sum < 80 && eightyindex < words.length - 1){
                //sum = sum + words[eightyindex].length();
                strmid = str1;
                str1 = str1 + " " +  words[eightyindex];
                eightyindex++;
                sum = str1.length();
            }
            String str2 = words[(eightyindex - 1)];
            for(int i = (eightyindex); i < words.length; i++){
                str2 = str2 + " " + words[i];
            }
            linkedline.remove(index);
            linkedline.add(index,strmid);
            linkedline.add(index+1,str2);
        }

    }

}


No.12**************************
每次考试之后，教师都要统计考试成绩，一般包括：平均分，对所有人按成绩从高到低排队，谁成绩最好，谁成绩最查。为了简化，以字典（map）形式表示考试成绩记录，例如：{“zhangsan”：90，“lisi”：78，“wangermazi”：39}

import java.util.LinkedList;
import java.util.Scanner;

public class score {
    public static void main(String[] args){
        LinkedList<String> scorelist = new LinkedList<>();
        int index = 1;

        Scanner sc = new Scanner(System.in);
        System.out.println("请输入学生的人数");
        int studentnumber = Integer.parseInt(sc.nextLine());
        System.out.println("请输入学生姓名和成绩");
        String firstname = sc.nextLine();
        System.out.println(firstname);
        int firstscore = Integer.parseInt(sc.nextLine());;
        System.out.println(firstscore);
        scorelist.add(firstname + "@" + firstscore);
        while(index < studentnumber){
            int moveindex = 0;
            String name = sc.nextLine();
            System.out.println(name);
            //String testname = sc.nextLine();
            int score = Integer.parseInt(sc.nextLine());
            System.out.println(score);
            String data = name + "@" + score;
            while(moveindex < index  && (score < Integer.parseInt(scorelist.get(moveindex).split("@")[1]))){
                moveindex++;
            }
            scorelist.add(moveindex,data);
            index++;
        }
        System.out.println("学生成绩排名为：");
        for(int i = 0; i < index; i++){
            String[] scoredata = scorelist.get(i).split("@");
            System.out.println(scoredata[0] + " " + scoredata[1]);
        }
    }
}

No.13**********************
正则表达式识别后面的字符串：“bat”、“bit”、“but”、“hat”、“hit”和“hut”

import java.util.regex.*;
import java.util.Scanner;

public class strdetection {
    public static void main(String[] args){
        System.out.println("请输入待检测的字符串");
        Scanner sc = new Scanner(System.in);
        String strdec = sc.nextLine();
        boolean is = Pattern.matches("b[aiu]t|h[aiu]t",strdec);
        System.out.println("是否是字符串bat、but、bit、hat、hut或hit");
        System.out.println(is);
    }
}

No.14*********************
将年月日的时间格式通过正则表达式的方式表达为日月年

import java.util.regex.Pattern;
import java.util.Scanner;
public class datereverse {
    public static void main(String[] args){
        System.out.println("请输入日期，例如：2008-12-25");
        Scanner sc = new Scanner(System.in);
        String str = sc.nextLine();
        String[] strarr = Pattern.compile("-").split(str);
        System.out.println(str + "对应的日月年的形式为：");
        System.out.println(strarr[2] + "/" + strarr[1] + "/" + strarr[0]);

    }
}

No.15*******************************
从电子邮件地址中提取登录名和域名

import java.util.Scanner;
public class emailaddress {
    public static void main(String[] args){
        System.out.println("请输入邮箱地址，例如ny@qq.com");
        Scanner sc = new Scanner(System.in);
        String emailaddress = sc.nextLine();
        String[] strarr = emailaddress.split("@");
        System.out.println(emailaddress + "的");
        System.out.println("登录名为：" + strarr[0]);
        System.out.println("域名为：" + strarr[1]);
    }
}
