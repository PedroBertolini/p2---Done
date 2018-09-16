package mediascomvetor;

import java.util.Scanner;

public class Mediascomvetor {

    public static void main(String[] args) {
        Scanner ler = new Scanner(System.in);
        int qtdCadeiras;
        String menu1;

        System.out.println("Quantas cadeiras o aluno esta pagando?");
        qtdCadeiras = ler.nextInt();
        ler.nextLine();
        double[] gq1 = new double[qtdCadeiras];
        double[] gq2 = new double[qtdCadeiras];
        double[] nfinal = new double[qtdCadeiras];
        String[] cadeiras = new String[qtdCadeiras];
        double[] mediaGq = new double[qtdCadeiras];
        double[] mediaFinal = new double[qtdCadeiras];
        String[] resultado = new String[qtdCadeiras];

        do {
            System.out.println("Informe os nomes das cadeiras");
                String a;
                int contador = 1;
                for (int i = 0; i < cadeiras.length; i = i + 1) {
                    System.out.println("Informe o nome da " + contador + "º cadeira !");
                    contador = contador + 1;
                    cadeiras[i] = ler.nextLine();
                }
                System.out.println("--Cadeiras cadastradas--");

                for (int i = 0; i < cadeiras.length; i = i + 1) {
                    System.out.print(cadeiras[i] + " ");
                }
                System.out.println("confirmar cadeiras ? s/n");
                menu1 = ler.nextLine();
                        
        } while ("n".equals(menu1));
        System.out.println("informe as notas do 1º GQ");
        lerNotas(gq1, cadeiras);
        System.out.println("Informe as notas do 2º GQ");
        lerNotas(gq2, cadeiras);
        mediaGQ(gq1, gq2, mediaGq);
        lerFinal(mediaGq, nfinal, cadeiras);
        mediaFinal(mediaGq, nfinal, mediaFinal);
        rFinal(mediaFinal, resultado, cadeiras);

    }

    //Função ler notas do GQ
    public static void lerNotas(double[] v, String[] vs) {
        Scanner ler = new Scanner(System.in);
        for (int i = 0; i < v.length; i = i + 1) {
            System.out.println("informe a nota de " + vs[i] + " !");
            v[i] = ler.nextInt();
        }

        //Função tirar media GQ
    }

    public static void mediaGQ(double[] v, double[] vs, double[] vm) {
        for (int i = 0; i < v.length; i = i + 1) {
            vm[i] = ((2 * v[i]) + (3 * vs[i])) / 5;
        }
    }

    //Função ler notas da Final
    public static void lerFinal(double[] v,double[] vs, String[] vm) {
        Scanner ler = new Scanner(System.in);
        for (int i = 0; i < v.length; i = i + 1) {
            if (v[i] > 3 && v[i] < 7) {
                System.out.println(v[i] + "**");
                System.out.println("informe a nota final de " + vm[i] + " !");
                vs[i] = ler.nextInt();
            }
        }
    }

    //Função tira media final
    public static void mediaFinal(double[] v, double[] vs, double[] vm) {

        for (int i = 0; i < v.length; i = i + 1) {
            if (v[i] > 3 && v[i] < 7) {
                vm[i] = (v[i] + vs[i]);
            } else {
                vm[i] = v[i];
            }

        }
    }

    public static void rFinal(double[] v, String[] vs, String[] vm) {
        for (int i = 0; i < v.length; i = i + 1) {
            if (v[i] < 7) {
                vs[i] = "Reprovado";
            } else {
                vs[i] = "Aprovado";
            }

        }
        for (int j = 0; j < v.length; j = j + 1) {
            System.out.println("situação em " + vm[j] + " ->" + vs[j] + " com média: **" + v[j] + "**");
            
        }
    }
}
