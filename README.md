#include <stdio.h>
#include <stdlib.h>
#include <limits.h>

#define C 6
#define R 6

int main(){
    int arr[R][C];
    int max_sum = INT_MIN;
    int i, j;
    
    for(i = 0; i < R; i++){
       for(j = 0; j < C; j++){
          scanf("%d",&arr[i][j]);
       }
    }
    
    for (i = 0; i < R-2; i++){
        for (j = 0; j < C-2; j++){
            // hourglass structure 
            int current = arr[i][j] + arr[i][j+1] + arr[i][j+2] + arr[i+1][j+1] + arr[i+2][j] + arr[i+2][j+1] + arr[i+2][j+2];
            if (current > max_sum) {
                max_sum = current;
            }
        }
    }
    printf("%d\n", max_sum);
    return 0;
}


import java.util.Scanner;

public class Solution {

    public static void main(String[] args) {
        Scanner scan = new Scanner(System.in);
        int i = scan.nextInt();
        Double d=scan.nextDouble();
        scan.nextLine();
        String n=scan.nextLine();
       // System.out.print(s);
        // Write your code here.

        System.out.println("String: " + n);
        System.out.println("Double: " + d);
        System.out.println("Int: " + i);
    }
}
import java.util.Scanner;

public class Solution {

    public static void main(String[] args) {
            Scanner sc=new Scanner(System.in);
            System.out.println("================================");
            for(int i=0;i<3;i++){
                String s1=sc.next();
                int x=sc.nextInt();
                //Complete this line
                System.out.printf("%-15s%03d%n",s1,x);
            }
        
            System.out.println("================================");

    }
}

import java.io.*;
import java.util.*;
import java.text.*;
import java.math.*;
import java.util.regex.*;

public class Solution {

    public static void main(String[] args) {
        Scanner in = new Scanner(System.in);
        int n = in.nextInt();
        for(int i=1;i<=10;i++)
            {
            System.out.println(n + " x " +i+" = "+(n*i));
        }
    }
}

import java.util.*;
import java.io.*;



class Solution{
    public static void main(String []argh)
    {



        Scanner sc = new Scanner(System.in);
        int t=sc.nextInt();

        for(int i=0;i<t;i++)
        {

            try
            {
                long x=sc.nextLong();
                System.out.println(x+" can be fitted in:");
                if(x>=-128 && x<=127)
                    System.out.println("* byte");
                if(x>=-(Math.pow(2,15)) && x<=(Math.pow(2,15)-1))
                System.out.println("* short");

                if(x>=-(Math.pow(2,31)) && x<=(Math.pow(2,31)-1))
                System.out.println("* int");

                if(x>=-((Math.pow(2,63))) && x<=((Math.pow(2,63))-1))
                System.out.println("* long");

                //Complete the code
            }
            catch(Exception e)
            {
                System.out.println(sc.next()+" can't be fitted anywhere.");
            }

        }
    }
}

import java.io.*;
import java.util.*;
import java.text.*;
import java.math.*;
import java.util.regex.*;

public class Solution {

    public static void main(String[] args) {
        Scanner in = new Scanner(System.in);
        String month = in.next();
        String day = in.next();
        String year = in.next();
        String finalDate = year+"-"+month+"-"+day;
        Calendar c = Calendar.getInstance();
        Date d1;
        SimpleDateFormat sdf;
        sdf= new SimpleDateFormat("yyyy-MM-dd");
        try
        {
            d1=sdf.parse(finalDate);
        
        c.setTime(d1);
        int dayOfWeek = c.get(Calendar.DAY_OF_WEEK);
        switch(dayOfWeek)
            {
            case 1:System.out.println("SUNDAY");
                    break;
            case 2:System.out.println("MONDAY");
                    break;
            case 4:System.out.println("WEDNESDAY");
                    break;
            case 5:System.out.println("THURSDAY");
                    break;
            case 6:System.out.println("FRIDAY");
                    break;
            case 7:System.out.println("SATURDAY");
                    break;
            case 3:System.out.println("TUESDAY");
                    break;
        }}
        catch(Exception e)
            {
            e.printStackTrace();
        }
    }
}

import java.util.*;
import java.text.*;

public class Solution {
    
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);
        double payment = scanner.nextDouble();
        scanner.close();
        
        // Write your code here.
        String us = NumberFormat.getCurrencyInstance(Locale.US).format(payment);
        String india = NumberFormat.getCurrencyInstance(new Locale("en","in")).format(payment);
        String china = NumberFormat.getCurrencyInstance(Locale.CHINA).format(payment);
        String france = NumberFormat.getCurrencyInstance(Locale.FRANCE).format(payment);
        
        System.out.println("US: " + us);
        System.out.println("India: " + india);
        System.out.println("China: " + china);
        System.out.println("France: " + france);
    }
}


public class Solution {

        public static void main(String[] args){
            Class student = Student.class; // uses class literal, not a function.
                Method[] methods = student.getDeclaredMethods();

            /* Get names from Methods */
            ArrayList<String> methodNames = new ArrayList<>();
            for (Method method : methods) {
                methodNames.add(method.getName());
            }

            /* Sort and print names */
            Collections.sort(methodNames);
            for (String name: methodNames) {
                System.out.println(name);
            }
        }

    }
    import static java.lang.System.in;

class Prime {
    void checkPrime(int... numbers) {
        for (int num : numbers) {
            if (isPrime(num)) {
                System.out.print(num + " ");
            }
        }
        System.out.println();
    }
    
    boolean isPrime(int n) {
        if (n < 2) {
            return false;
        }
        for (int i = 2; i <= (int) Math.sqrt(n); i++) {
            if (n % i == 0) {
                return false;
            }
        }
        return true;
    }     
}


import java.util.*;
import java.security.*;
interface Food {
     public String getType();
    }
    class Pizza implements Food {
     public String getType() {
     return "Someone ordered a Fast Food!";
     }
    }

    class Cake implements Food {

     public String getType() {
     return "Someone ordered a Dessert!";
     }
    }
    class FoodFactory {
        public Food getFood(String order) {

if(order.equalsIgnoreCase("cake"))
       return new Cake();
    else
       return new Pizza();
       }//End of getFood method

    }//End of factory class

    public class Solution {

     public static void main(String args[]){
            Do_Not_Terminate.forbidExit();

        try{

            Scanner sc=new Scanner(System.in);
            //creating the factory
            FoodFactory foodFactory = new FoodFactory();
    
            //factory instantiates an object
            Food food = foodFactory.getFood(sc.nextLine());
    
            
            System.out.println("The factory returned "+food.getClass());
            System.out.println(food.getType());
        }
        catch (Do_Not_Terminate.ExitTrappedException e) {
            System.out.println("Unsuccessful Termination!!");
        }
     }

    }
    class Do_Not_Terminate {
         
        public static class ExitTrappedException extends SecurityException {

            private static final long serialVersionUID = 1L;
        }
     
        public static void forbidExit() {
            final SecurityManager securityManager = new SecurityManager() {
                @Override
                public void checkPermission(Permission permission) {
                    if (permission.getName().contains("exitVM")) {
                        throw new ExitTrappedException();
                    }
                }
            };
            System.setSecurityManager(securityManager);
        }
    }   
        




import java.io.*;
import java.util.*;
import java.text.*;
import java.math.*;
import java.util.regex.*;
import java.lang.reflect.*;


import java.util.Scanner;
import java.lang.reflect.Constructor;

class Singleton {
    private Singleton() {}
    public String str;
    private static Singleton instance = null;
    public static Singleton getSingleInstance() {
        if (instance == null) {
            instance = new Singleton();
        }
        return instance;
    }

}

import java.io.*;
import java.util.*;

public class Solution {

    public static void main(String[] args) {
        
        Scanner sc=new Scanner(System.in);
        String A=sc.next();
        String B=sc.next();
        int sum =B.length()+ A.length();
        System.out.println(sum);
        int res=A.compareTo(B);
        if(res<0 || res==0)
            {
            System.out.println("No");
        }else
            {
            System.out.println("Yes");
        }
        String outputA = A.substring(0, 1).toUpperCase() + A.substring(1);
        String outputB = B.substring(0, 1).toUpperCase() + B.substring(1);
        System.out.println(outputA+" "+outputB);
        
        
        /* Enter your code here. Print output to STDOUT. */
        
    }
}


import java.io.*;
import java.util.*;
import java.text.*;
import java.math.*;
import java.util.regex.*;

public class Solution {

    public static void main(String[] args) {
        Scanner in = new Scanner(System.in);
        String S = in.next();
        int start = in.nextInt();
        int end = in.nextInt();
        System.out.println(S.substring(start, end));
    }
}

import java.io.*;
import java.util.*;
import java.text.*;
import java.math.*;
import java.util.regex.*;

public class Solution {

    public static void main(String[] args) {
        /* Enter your code here. Read input from STDIN. Print output to STDOUT. Your class should be named Solution. */
         Scanner sc = new Scanner(System.in);

    String str = sc.next();
    int k = sc.nextInt();

    int len = str.length() - k + 1;

    String[] arr = new String[len];

    for(int i=0; i<len; i++){

        arr[i] = str.substring(i,i+k);
        //System.out.println(arr[i]);
    }

    Arrays.sort(arr);

    System.out.println(arr[0]);
    System.out.println(arr[len-1]);
        
    }
}
import java.io.*;
import java.util.*;

public class Solution {

    public static void main(String[] args) {
        
        Scanner sc=new Scanner(System.in);
        String A=sc.next();
        /* Enter your code here. Print output to STDOUT. */
       String aRew =new StringBuffer(A).reverse().toString(); 
        if(A.equals(aRew))
            {System.out.println("Yes");}
        else
            {System.out.println("No");}
        
    }
}

String s = a.toLowerCase() + b.toLowerCase();
        char ch = '1';
        for(char c : s.toCharArray()){
            ch ^= c;
        }
        return ch == '1' ? true : false;

//Regex Vala
import java.util.Scanner;
import java.util.regex.*;

public class Solution
{
   public static void main(String[] args){
      Scanner in = new Scanner(System.in);
      int testCases = Integer.parseInt(in.nextLine());
       
      while(testCases>0){
         String pattern = in.nextLine();
             //Write your code
         try {
            Pattern.compile(pattern);
             System.out.println("Valid");
        } catch (PatternSyntaxException exception) {
            System.out.println("Invalid");
             //System.err.println(exception.getDescription());
            
        }
          
      }
   }
}

import java.util.regex.Matcher;
import java.util.regex.Pattern;
import java.util.Scanner;

class Solution{

    public static void main(String []args){
        Scanner in = new Scanner(System.in);
        while(in.hasNext()){
            String IP = in.next();
            System.out.println(IP.matches(new MyRegex().pattern));
        }

    }
}

class MyRegex()
    {
     String pattern = "(\\d|\\d{2}|[0-2][0-5]{2})\\.(\\d|\\d{2}|[0-2][0-5]{2})\\.(\\d|\\d{2}|[0-2][0-5]{2})\\.(\\d|\\d{2}|[0-2][0-5]{2})";
}
}
import java.io.*;
import java.util.*;
import java.text.*;
import java.math.*;
import java.util.regex.*;

public class Solution {

   public static void main(String[] args) {
      Scanner in = new Scanner(System.in);
      BigInteger n = in.nextBigInteger();
      in.close();
      // Write your code here.
       if(n.isProbablePrime(1)==true) 
       { System.out.println("prime"); } 
       else { System.out.println("not prime");
   }
}
}

public class Solution {
    static int mode(int []a){
        int val = 0;
        int maxCou = 0;
        int N = a.length;
        Map<Integer,Integer> pair = new HashMap<Integer,Integer>();
        for(int i=0;i<N;i++){
            if(pair.get(a[i])!=null){
                pair.put(a[i],pair.get(a[i])+1);
            }else{
                pair.put(a[i],1);
            }
            if(pair.get(a[i])== maxCou && a[i]< val){
                val = a[i];
            }
            if(pair.get(a[i])>maxCou){
                maxCou = pair.get(a[i]);
                val = a[i];
            }
        }
        return val;
    }
    public static void main(String[] args) {
        Scanner s = new Scanner(System.in);
        int N = s.nextInt();
        if(N<10 ||N>2500){
            System.out.println("Number out of range.");
            return;
        }
        int []num = new int[N];
        int sum=0;
        for(int i=0;i<N;i++){
            num[i] = s.nextInt();
            sum += num[i];
        }
        double mean = (double) sum/N;
        System.out.println(mean);
        Arrays.sort(num);
        if(num.length%2==0){
            System.out.println(0.5*num[N/2]+0.5*num[N/2-1]);
        }else{
            System.out.println(num[N/2-1]);
        }
        int m = mode(num);
        System.out.println(m);
        return;
    }
}
