# evidence
import java.util.Scanner;

public class bubble {
    
    int[] data = {5, 4, 1, 3, 2};
    
    public int max = data.length;
    
    void tukar(int a, int b){
        int temp;
        temp = data[b];
        data[b] = data[a];
        data[a] = temp;
    }
    
    void output(){
        int i;
        for (int j = 0; j <= max-1; j++) {
            System.out.print(data[j]+" ");
        }
        System.out.println();
    }
    
    void sortBubbleAsc(){
        int a, b;
        int n = max-1;
        for (int i = 0; i <= n-1; i++) {
            for (int j = i+1; j <= n; j++) {
                if(data[i] > data[j]){
                    tukar(i, j);
                }
                System.out.print(i+" "+j+" | ");
                output();
            }
        }
    }
    
    
    void sortBubbleDesc(){
        int a, b;
        int n = max-1;
        for (int i = 0; i <= n-1; i++) {
            for (int j = i+1; j <= n; j++) {
                if(data[i] < data[j]){
                    tukar(i, j);
                }
                System.out.print(i+" "+j+" | ");
                output();
            }
        }
    }
    
    
    public static void main(String[] args) {
        bubble ins = new bubble();
        Scanner input = new Scanner(System.in);
		
        /*
                jangan panggil fungsi secara bersamaan. karena array bersifat global variable atau atribut
        */
        System.out.println("1. sortBubbleDesc()");
        System.out.println("2. sortBubbleAsc()");
        System.out.println("==========================");
        System.out.print("Masukan Pilihan : ");
        int p = input.nextInt();

        switch(p){
                case 1:
                        ins.sortBubbleDesc();
                break;
                case 2:
                        ins.sortBubbleAsc();
                break;
        }
    }
}
