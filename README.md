# Given-an-integer-N.-What-is-the-smallest-integer-greater-than-N-in-java

// you can also use imports, for example:
// import java.util.*;

// you can write to stdout for debugging purposes, e.g.
// System.out.println("this is a debug message");

class Solution {
    public int getSum(int n){

        int sum=0;
        while (n != 0){
            sum=sum+n%10;
            n=n/10;
        }
        return sum;
    }
    public int solution(int N) {
        // write your code in Java SE 8
        int i= getSum(N);
        int d=i*2;
        int k=N;
        while (k<100000){
            if (getSum(k)==d){
                /System.out.println(k);/
                return k;
            }
            k++;
        }
        return N;
    }
    
    
}
