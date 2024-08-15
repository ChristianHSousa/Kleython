package javaapplication1;

public class JavaApplication1 {

    public static void main(String[] args) {

        int[] v = {2, 5, -20, 7, 100, 1, -14, 78, 30, 0};
        System.out.println(SomaPrimo(100));

    }

    // 1
    public static double HiperFat(double n) {
        if (n <= 0) {
            return 1;
        }
        return Math.pow(n, n) * HiperFat(n - 1);
    }

    //2
    public static boolean Primo(int n, int z) {
        if (z == 1) {
            return true;
        } else if (n == 1) {
            return false;
        } else if (n % z == 0) {
            return false;
        }
        return Primo(n, z - 1);
    }

    //3.1
    public static double SomaPrimo(int n) {
        if (n == 1) {
            return 0;
        } else if (Primo(n, n - 1)) {
            return n + SomaPrimo(n - 1);
        } else {
            return SomaPrimo(n - 1);
        }
    }

    //3.2
    public static double Fibo(int n){
        if (n == 0 || n == 1){
            return 1;
        }
        return Fibo(n-1) + Fibo(n-2);
    }

    public static double VezesParFibo(int n){
        if(n == 0){
            return 1;
        }else if(Fibo(n)%2 == 0){
            return Fibo(n) * VezesParFibo(n-1);
        }else{
            return VezesParFibo(n-1);
        }
    }
    
    
    
    // 4
    public static double calcPot(double base, double expoente) {
        if (expoente <= 0) {
            return 1;
        }
        return base * calcPot(base, expoente - 1);
    }

    // 6
    public static double somaVect(int[] vect, int tamanho) {
        if (tamanho <= 0) {
            return 0;
        }
        return vect[tamanho - 1] + somaVect(vect, tamanho - 1);
    }

    //7
    public static double VectCont(int[] vect, int tamanho) {
        if (tamanho <= 0) {
            System.out.println();
            return 0;
        }
        System.out.print(vect[tamanho - 1] + " ");
        return VectCont(vect, tamanho - 1);
    }

}
