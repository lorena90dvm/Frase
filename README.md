# Frase
import java.util.Scanner;
public class Frase {
	public static void main(String[] args){
		Scanner scanf = new Scanner(System.in);
		System.out.print("--> ");
		System.out.flush();// fuerza a sacar la cadena por pantalla
		String frase = scanf.nextLine();//recoge la entrada de teclado
		System.out.println("+----- Metodo 1 ----------+");
		
		String[] arrayPalabras=frase.split("");
		for(String unaPalabra: arrayPalabras){
			System.out.println(unaPalabra);
		}
		System.out.println("+----- Metodo 2 ---------+");
		
		arrayPalabras=frase.split("\\s+");
		for(String unaPalabra: arrayPalabras){
			System.out.println(unaPalabra);
		}
		System.out.println("+----- Metodo 3 ---------+");
		for(int i = 0; i<frase.length(); i++){
			if(frase.charAt(i) == ' '){
				System.out.println("");
			}
			else {
				System.out.print(frase.charAt(i));
			}
		}
		System.out.println("");
		System.out.println("+-----##FIN##-----------+");
		scanf.close();
	}
}
