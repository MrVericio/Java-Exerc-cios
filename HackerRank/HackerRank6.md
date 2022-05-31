import java.util.*;
import java.io.*;

class Solution6 {
    public static void main(String[] argh) {
        Scanner in = new Scanner(System.in);

        /*
         * (a + 2º * b) (a + 2º * b + 2¹ * b) (a + 2º * b + 2¹ * b ... + 2n-¹ *b) // a
         * potência vai ser o indice do for.
         */
    
        int t = in.nextInt();
        for (int i = 0; i < t; i++) {
            int a = in.nextInt();
            int b = in.nextInt();
            int n = in.nextInt();

//            int [] resultados = new int [n];
            String resultados = "";
            int somaTotal = 0;

            for (int j = 0; j < n; j++) {
                int result = (int) (Math.pow(2, j)*b);
    
                somaTotal = somaTotal + result;
    
                if (j == 0) {
                    somaTotal = somaTotal + a;
                    resultados = resultados + somaTotal;
                }
                else {
                    resultados = resultados + " " + somaTotal;
                }
    
    
            }
    
            System.out.println(resultados);
    
        }
    
        in.close();
    }

}
