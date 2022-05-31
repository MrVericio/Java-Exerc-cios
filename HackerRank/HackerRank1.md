import java.io.*;
import java.math.*;
import java.security.*;
import java.text.*;
import java.util.*;
import java.util.concurrent.*;
import java.util.function.*;
import java.util.regex.*;
import java.util.stream.*;

import javax.sound.sampled.spi.FormatConversionProvider;

import static java.util.stream.Collectors.joining;
import static java.util.stream.Collectors.toList;

class Result {

    /*
     * Complete the 'fizzBuzz' function below.
     *
     * The function accepts INTEGER n as parameter.
     */
    
    public static void fizzBuzz(int n) {
        // Write your code here
        // If i is a multiple of both 3 and 5, print FizzBuzz.
    
        for (int i = 1; i <= n; i++) {
    
            if (i % 3 == 0 && i % 5 == 0){
                System.out.println("FizzBuzz");
            }
            //If i is a multiple of 3 (but not 5), print Fizz.
            if (i % 3 == 0 && i % 5 != 0) {
                System.out.println("Fizz");
            }
            //If i is a multiple of 5 (but not 3), print Buzz.
            if (i % 5 == 0 && i % 3 != 0) {
                System.out.println("Buzz");
            }
            //If i is not a multiple of 3 or 5, print the value of i.
            if (i % 3 != 0 && i % 5 != 0) {
                System.out.println(i);
            }
    
        }
    
    }

}

public class Solution {
    public static void main(String[] args) throws IOException {
        BufferedReader bufferedReader = new BufferedReader(new InputStreamReader(System.in));

        int n = Integer.parseInt(bufferedReader.readLine().trim());
    
        Result.fizzBuzz(n);
    
        bufferedReader.close();
    }

}
