import java.util.Scanner;

public class Stand2 {
    public static void main(String[] args) {

        Scanner Resposta = new Scanner(System.in);
        String SAIR = "";

        do {
            String Marca;
            double Cilindrada;
            String Mudancas;
            int NI;

            System.out.printf("Qual é a marca do carro? ");
            Marca = Resposta.nextLine();

            System.out.printf("\nQual é a cilindrada do carro? ");
            Cilindrada = Resposta.nextDouble();
            Resposta.nextLine(); // limpar ENTER

            System.out.print("\nQual é o tipo de mudanças do carro? ");
            Mudancas = Resposta.nextLine();

            System.out.printf("\nQual é o número de identificação do carro? ");
            NI = Resposta.nextInt();
            Resposta.nextLine(); // limpar ENTER

            if (Marca.equalsIgnoreCase("Audi") || Marca.equalsIgnoreCase("BMW")) {
                System.out.printf("\nCarro Alemão!");
            } else {
                System.out.println("\nOutro fabricante");
            }

            if (Cilindrada >= 2000){
                System.out.println("\nMotor potente!");
            } else {
                System.out.println("\nMotor moderado");
            }

            if (Mudancas.equalsIgnoreCase("Automática")){
                System.out.println("\nCaixa automática");
            } else {
                System.out.println("\nCaixa manual");
            }

            System.out.println("\nO número de identificação foi alterado para: " + NI);

            // Perguntar no fim
            System.out.println("\nEscreva SAIR se quiser sair, ou ENTER para continuar:");
            SAIR = Resposta.nextLine();

        } while (!SAIR.equalsIgnoreCase("SAIR"));
    }
}