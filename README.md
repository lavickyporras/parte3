#include <iostream>
using namespace std;

void solicitarContrasena(string clave){
	string palabra;

	cout << "Quiero comer crustaceos... " << endl;
	cin >> palabra;
	while (clave != palabra){
		cout << "Eres tonto yo lo que quiero es comer crustaceos " <<endl;
		cin >> palabra;
	}
}

	/* OTRA FORMA DE HACERLO
	cout << "Quiero crustaceos";
	cin>> palabra;
	fro (int i = 0; clve != palabra && i< 3 ; i++){
	cout << "deberas que quiero crustaceos.." ;
	cin >> palabar;
	}
*/

int aBase8 (int numero){
	int decenas;
	int unidades;
	if (numero > 64){ cout << "no estamos preparados para trabajar la recurrencia todavia...";
	}
	else{
		unidades = numero%8;
		decenas = numero/8;
		numero = decenas*10 + unidades;
	}
	return numero ;
}

void imprimirLista(string lista[], int tama){
	for (int i= 0 ; i<tama; i++){
		cout << lista[i] << endl;
	}
}

void pasarLista(string lista[], int tama, char listaFaltas[]){
	string respuesta;
	for (int i= 0 ; i<tama; i++){
		cout << "esta "<< lista[i]<< " en clase " <<endl;
		cin >> respuesta;
		if (respuesta == "si") listaFaltas[i] = 'V';
		else listaFaltas[i] = 'F';
	}
}




int main(){
	string contrasena = "crustaceos";
	int numero;
	int numeroBase8;
	int tamaLista= 5;
	string listaPulpos[] = {"a", "b","c","d", "e"};
	char listaFaltas[tamaLista];

cout << "vicky" << endl;

solicitarContrasena(contrasena);

cout << "introduce un numero" << endl;
cin >> numero;
numeroBase8 = aBase8(numero);
cout << numeroBase8<< endl ;
imprimirLista(listaPulpos, tamaLista);
cout << endl;
pasarLista(listaPulpos, tamaLista, listaFaltas);
cout << endl;



	return 0;
}
