#include <iostream>

using namespace std;

int sommaArray(int[], int [], int*, int);
void stampaArray(int[], int);
int cercaIndice(int[], int, int);

int main(){
	const int MAX=5;
	int A1[MAX];
	int A2[MAX];
	int A3[MAX];
	int m=0;
	int indice=0;
	int riempimento=0;
	
	cout<<"Inserisci array A1, "<<MAX<<" numeri divisi da uno spazio: ";
	for(int i=0;i<MAX;i++)
		cin>>A1[i];
	cout<<"\nInserisci array A2, "<<MAX<<" numeri divisi da uno spazio: ";
	for(int i=0;i<MAX;i++)
		cin>>A2[i];

	cout<<"Inserisci l'intero m: ";
	cin>>m;
	
	riempimento=sommaArray(A1, A2,  &A3[0], MAX);
	cout<<"Array A3: ";
	stampaArray(A3, riempimento);
	cout<<endl<<"Il riempimento di A3 e' pari a: "<<riempimento<<endl;
	indice=cercaIndice(A3, riempimento, m);
	if(indice==-1)
		cout<<"Nessun valore di A3 e' maggiore di "<<m<<endl;
	else
		cout<<"il valore in posizione: "<<indice<<" e' maggiore di: "<<m<<endl;
	return 0;
}

int sommaArray(int a1[], int a2[], int* a3, int max){
	int tmpCont=0, cont=0;
	for(int i=0;i<max;i++)
		if(a1[i]%2!=0 && a2[i]%2!=0)
			tmpCont++;

	for(int i=0;i<max;i++)
		if(a1[i]%2!=0 && a2[i]%2!=0)
			a3[cont++]=a1[i]+a2[i];

	return tmpCont;
}

void stampaArray(int a[], int max){
	for(int i=0; i<max;i++)
		cout<<a[i]<<" ";
}

int cercaIndice(int a[], int max, int m){
	int ret=-1;
	for(int i=0;i<max;i++)
		if(a[i]>m){
			ret=i;
			break;
		}
	return ret;
}
