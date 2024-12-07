# Spiral-
Spiral in java
import javax.security.sasl.SaslClient;
import java.util.Scanner;

public class Spiral {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        int n = sc.nextInt();
        int m = sc.nextInt();
        int arr[][]= new int[n][m];
        for (int i =0;i<n;i++){
            for (int j =0;j<m;j++){
                arr[i][j]= sc.nextInt();
            }
        }
        System.out.println("Enter the spiral:");
        int rowStart = 0;
        int rowEnd = n-1;
        int colStart = 0;
        int colEnd = m-1;
        while (rowStart<=rowEnd&& colStart<=colEnd){
            for (int col =colStart;col<=colEnd;col++){
                System.out.println(arr[rowStart][col]);
            }
            rowStart++;
            for (int row = rowStart;row<=rowEnd;row++){
                System.out.println(arr[row][colEnd]);
            }
            colEnd--;
            for (int col = colEnd;col>=colStart;col--){
                System.out.println(arr[rowEnd][col]);
            }
            rowEnd--;
            for (int row = rowEnd;row>=rowStart;row++){
                System.out.println(arr[row][colStart]);
            }
            colStart++;


            System.out.println();

        }


    }
}
