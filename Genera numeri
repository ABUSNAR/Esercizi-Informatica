import java.util.Scanner;
import java.util.Random;

public class Main {
    public static void main(String[] args) {
        Scanner tastiera = new Scanner(System.in);
        String[] opzioni = {"Menu", "1 Genera Numeri Casuali", "2 Visualizza Numeri", "3 Esci"};
        boolean esci = true;
        int[] nEstratti = new int[5]; 
        
        do {
            int scelta = Menu(opzioni, tastiera);
            switch (scelta) {
                case 1:
                    System.out.println("Generazione numeri casuali...");
                    generaNumeri(nEstratti);
                    break;
                case 2:
                    System.out.println("Visualizzazione dei numeri generati:");
                for (int i = 0; i < nEstratti.length; i++) {
    int numero = nEstratti[i];
                        if (numero != 0) { 
                            System.out.println(numero);
                        }
                    }
                    break;
                case 3:
                    System.out.println("Fine del programma.");
                    esci = false;
                    break;
                default:
                    System.out.println("Opzione non valida. Riprova.");
                    break;
            }
        } while (esci);
        
        tastiera.close(); 
    }

    public static int Menu(String[] opzioni, Scanner tastiera) {
        for (String opzione : opzioni) {
            System.out.println(opzione);
        }
        System.out.println("Scegli un'opzione: ");
        return tastiera.nextInt();
    }

    public static void generaNumeri(int[] vettore) {
        Random numeroRandom = new Random();
        int count = 0; 

        while (count < vettore.length) {
            int numero = numeroRandom.nextInt(100) + 1; 
            boolean duplicato = false;

     
            for (int i = 0; i < count; i++) {
                if (vettore[i] == numero) {
                    duplicato = true;
                    break;
                }
            }

            if (!duplicato) {
                vettore[count] = numero;
                count++;
            }
        }
    }
}


