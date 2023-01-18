import java.util.Scanner;

//Versión de Java: (jdk-18.0.2) ---- TP Nro 0 / Punto (3) 

public class Modulos {

	// Permite al usuario elegir si quiere escribir un número, o si quiere
	// seleccionar un número aleatorio

	public static void Menu() {
		String valido = "S";
		while (valido == "S") {
			System.out.println("Seleccion de opciones:	");
			System.out.println("1- Ingresar numero");
			System.out.println("2- Numero aleatorio");
			System.out.print("Elegir:  ");
			System.out.println();
			Scanner seleccion = new Scanner(System.in);
			Proceso(seleccion);
			Scanner seguir = new Scanner(System.in);
			seguir.equals(seguir);
			System.out.println("Si desea continuar presione la letra S/s de lo contrario presione otra tecla");
			String seguirPrograma = seguir.nextLine();
			if (seguirPrograma.equalsIgnoreCase(valido)) {
				valido = "S";
			} else {
				valido = "N";
				System.out.println("FIN DEL PROGRAMA");
			}
			System.out.println("------------------------------------");

		}
	}

	// Según la opcion elegida, realiza el proceso correspondiente

	public static void Proceso(Scanner seleccion) {
		String elegida = seleccion.nextLine();
		if (ValidarNumero(elegida)) {
			int seleccionado = Integer.parseInt(elegida);
			if (seleccionado == 1) {
				IngresarNumero();
			} else if (seleccionado == 2) {
				double aleatorio = (double) Math.random() * 500;
				int random = (int) aleatorio;
				System.out.println("El valor seleccionado de forma aleatoria es:  " + random);
				ClaseDeNumero(random);
			} else {
				System.out.println("Seleccion no valida");
			}
		} else {
			System.out.println("Seleccion no valida");
		}

	}

	// Pide un número al usuario

	public static void IngresarNumero() {
		Scanner numeroIngresado = new Scanner(System.in);
		ValidarNumeroPositivo(numeroIngresado);
	}

	// Detecta si el valor ingresado es mayor a 0

	public static void ValidarNumeroPositivo(Scanner numeroIngresado) {
		int inicializar = 0, numeroDefinitivo;
		while (inicializar == 0) {
			System.out.println("Ingresar numero:	");
			String numero = numeroIngresado.nextLine();
			if (ValidarNumero(numero)) {
				numeroDefinitivo = Integer.parseInt(numero);
				if (numeroDefinitivo <= 0) {
					System.out.println("Numero invalido, ingresar nuevamente");
					inicializar = 0;
				} else {
					inicializar = 1;
					ClaseDeNumero(numeroDefinitivo);
				}
			} else {
				System.out.println("El valor ingresado no es un numero");
				inicializar = 0;

			}
		}
	}

	// Detecta si lo ingresado es un número o no
	
	public static boolean ValidarNumero(String numero) {
		int numInicializar = 0;
		if (numInicializar == 0) {
			try {
				numInicializar = Integer.parseInt(numero);
				return true;
			} catch (Exception e) {
				return false;
			}
		} else {
			return true;
		}
	}
	
	// Determina si el número ingresado es un numero Perfecto, Abundante o
	// Deficiente

	public static void ClaseDeNumero(int numeroDefinitivo) {
		int sumadorDeDivisores = 0;
		for (int i = 1; i < numeroDefinitivo; i++) {
			int div = numeroDefinitivo % i;
			if (div == 0) {
				sumadorDeDivisores = sumadorDeDivisores + i;
			}
		}
		if (sumadorDeDivisores == numeroDefinitivo) {
			System.out.println("El valor ingresado es un numero Perfecto");
		} else if (sumadorDeDivisores > numeroDefinitivo) {
			System.out.println("El valor ingresado es un numero Abundante");
		} else {
			System.out.println("El valor ingresado es un numero Deficiente");
		}
	}
}
