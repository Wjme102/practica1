import java.util.Scanner;

public class CribaEratostenes {
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);
        System.out.print("Ingrese un número para N: ");
        int n = scanner.nextInt();

        long inicio = System.nanoTime(); 
        boolean[] esPrimo = new boolean[n + 1];
        for (int i = 2; i <= n; i++) {
            esPrimo[i] = true;
        }

        for (int i = 2; i * i <= n; i++) {
            if (esPrimo[i]) {
                for (int j = i * i; j <= n; j += i) {
                    esPrimo[j] = false;
                }
            }
        }
        long fin = System.nanoTime();

        System.out.println("Números primos menores o iguales a " + n + ":");
        for (int i = 2; i <= n; i++) {
            if (esPrimo[i]) {
                System.out.print(i + " ");
            }
        }
        System.out.println("\nTiempo de ejecución: " + (fin - inicio) + " nanosegundos.");
        scanner.close();
    }
}
