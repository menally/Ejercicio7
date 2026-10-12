import java.util.Scanner;
public class Main {
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);
        System.out.print("Introduce un año cualquiera (ej. 2024): ");

        int n = scanner.nextInt();
        //int n: Guarda el año//

        boolean bandera = false;
        //boolean bandera: Guarda verdadero o falso//

        if ((n % 4 == 0 && n % 100 != 0) || (n % 400 == 0)) {
            //% : Obtiene el residuo de una división//

            bandera = true;
            //bandera = true → Indica que cumple la condición//
        }

        if (bandera) {
            //if (bandera): Decide qué resultado mostrar//

            System.out.println("El año " + n + " tiene la propiedad: TIPO_A");
        } else {
            System.out.println("El año " + n + " tiene la propiedad: TIPO_B");
        }
        scanner.close();
    }
}
//El programa recibe un año y determina si cumple la condición
// establecida para clasificarlo como TIPO_A o TIPO_B