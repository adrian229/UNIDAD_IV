#include <iostream>
 using namespace::std;

 enum { Tamano = 5};
 // Cambiar la variable Tamano para ordenar una
 // cantidad diferente de datos
 

 /*Prototipo de funcion Imprime */
 void Imprime( int A[]);

 /*prototipo de funcion Recibe */
 void Recibe ( int B[]);

 /*Prototipo de funcion Burbuja */
 void Burbuja( int C[]);
 

 int main()

 {           // Abre main

 int Arreglo[Tamano] = {0, 0};
 // El Arreglo se ha inicializado a 0
 
 cout <<"\nEste programa recibe una serie de de numeros enteros" << Tamano;
 cout <<" y los ordena por medio del algoritmo de ordenacion burbuja. "<< endl; 

 /*Se llena el arreglo mediante un llamado a la funcion Recibe*/
 Recibe(Arreglo);

 /*Se imprime el arreglo con las entradas en el orden original */
 cout <<"\nEsta es el orden en que se introdujeron los elementos: " <<endl;
 Imprime(Arreglo);

 /*Se ordena el arreglo mediante una llamada a la funcion Burbuja*/
 Burbuja(Arreglo);

 /*Se imprime el arreglo ordenado */
 cout <<"\nEste es el orden despues de el ordenamiento burbuja. " <<endl;
 Imprime(Arreglo);

 return 0;
 }           // Cierra main


 //////////////////////////////////////////////////
 //FUNCION IMPRIME 
 /////////////////////////////////////////////////
 
 void Imprime( int A[] )
 {     // Abre la funcion Imprime
 
 for ( int j = 0; j < Tamano; j++ )
 {      // Abre for
 cout << "\t" << A[j]; 

 if ( 0 == j + 1 % 10)
 cout <<endl <<endl;

 }      // Cierra for

 cout <<endl <<endl;
 }     // Cierra la funcion Imprime

 ////////////////////////////////////////////////////////////////////////////
 //FUNCION RECIBE
 //////////////////////////////////////////////////////////////////////////
 

 void Recibe( int B[] )
 {         // Abre funcion Recibe
 
 for ( int i = 0; i < Tamano; i++ )
 {      // Abre for
 cout << "\nIntroduzca el elemento " << i + 1 << " del arreglo: " << endl;
 cin >> B[i];
 }
 }         // Cierra funcion Recibe



 ///////////////////////////////////////////////
 //FUNCION BURBUJA
 /////////////////////////////////////////////////
 

  void Burbuja( int C[])
 {                 // Abre funcion Burbuja

 int temporal;

 for ( int m = 0; m < Tamano - 1; m++ )
 for ( int n = 0; n <= Tamano - 1; n++ )
 {    // Abre for
     
 if ( C[n] > C[n + 1] )
 {    // Abre if
 temporal = C[n]; 
 C[n] = C[n + 1];
 C[n + 1] = temporal;

 }    // Cierra if 
 }         //Cierra for
 }                 // Cierra funcion Burbuja



