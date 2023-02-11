Part 1: W.a.p that declares two arrays named ‘even’ and ‘odd’. Accept 
numbers from the user and move them to respective arrays depending on 
whether they are even or odd.
Part 2: Implement a java function that finds 2 neighboring numbers in an array
with the smallest distance to each. The function should return the index of the 
1st number.
Part 3: Write a Java program to convert an array into ArrayList and vice versa.
PART 1 :
INPUT:
import java.util.Scanner;
public class Even_Odd
{
 public static void main(String[] args)
 {
 int n, j = 0, k = 0;
 Scanner s = new Scanner(System.in);
 System.out.print("Enter no. of elements you want in array:");
 n = s.nextInt();
 int a[] = new int[n];
 int odd[] = new int[n];
 int even[] = new int[n];
 System.out.println("Enter all the elements:");
 for(int i = 0; i < n; i++)
 {
 a[i] = s.nextInt();
 }
 for(int i = 0; i < n; i++)
 {
 if(a[i] % 2 != 0)
 {
 odd[j] = a[i];
 j++;
 }
 else
 {
 even[k] = a[i];
 k++;
 }
 }
 System.out.print("Odd:");
 if(j > 1)
 {
 for(int i = 0;i < (j-1); i++)
 {
 System.out.print(odd[i]+",");
 }
 System.out.print(odd[j-1]);
 }
 else
 {
 System.out.println("No number");
 }
 System.out.println("");
 System.out.print("Even:");
 if(k > 1)
 {
 for(int i = 0; i < (k-1); i++)
 {
 System.out.print(even[i]+",");
 }
 System.out.print(even[k-1]);
 }
 else
 {
 System.out.println("No number");
 }
 }
}
OUTPUT:
PART 2:
INPUT:
public int getIndexOfMinimumDistance() {
 int index = 0;
 int[] numbers = new int[]{999,0,5,8,10,89,54};
 for (int i = 1; i < numbers.length - 1; i++) {
 if ( Math.abs( numbers[index] - numbers[index + 1]) >
 Math.abs( numbers[i] - numbers[i + 1])) {
 index = i;
 }
 }
PART 3:
import java.util.Arrays;
import java.util.Scanner;
public class SecondSmallest {
 private static int[]arr=new int[100];
 private static int arrI=0;
 public static void main(String[]args) throws Exception
 {
 Scanner s=new Scanner(System.in);
 System.out.println("Enter numbers (-1 to stop)");
 int n;while((n=s.nextInt()) != -1)
 {
 arr[arrI] =n;
 arrI++;
 }
 s.close();
 System.out.println("Second Smallest number is: "+secondSmallest());
 }
 private static int secondSmallest()throws Exception
 {
 int[]sub=Arrays.copyOfRange(arr,0,arrI);
 Arrays.sort(sub);
 if(sub.length>0)return sub[1];
 else throw new Exception("Not enough elements in Array");
 }
}
OUTPUT:
