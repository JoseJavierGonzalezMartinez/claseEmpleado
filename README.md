# claseEmpleado
//jose javier gonzalez martinez, seminario estructura de datos, seccion D14
#include<iostream>
#include<stdlib.h>
using namespace std;


class materia{
    private:
        int claveClase;
        string nombre;
        string profesorTit;
        string libroTexto;
    public:
        materia (int clave,string nom,string prof,string libt);
        void imprime();
        void cambiaClave();
        void cambiaProfe();
};

materia::materia(int clave,string nom,string prof,string libt){
    claveClase =clave;
    nombre=nom;
    profesorTit=prof;
    libroTexto=libt;
}

void materia::imprime(){
    cout<<"clave: "<<claveClase<<" materia: "<<nombre<<" profesor: "<<profesorTit<<" libro: "<<libroTexto<<endl;
}

void materia::cambiaClave(){
    cout<<"cual es la nueva clave? "<<endl;
    cin>>claveClase;
}

void materia::cambiaProfe(){
    cout<<"cual es el nuevo profesor? "<<endl;
    getline(cin,profesorTit);
}

int main(){
    int opc,c=1;
    materia clase(42556,"programacion","Ortiz Pimentel, Belen Anabett","introduccion a los algoritmos");
    cout<<"que opcion desea realizar"<<endl;
    cout<<"1.- imprimir datos"<<endl<<"2.- cambiar clave de materia"<<endl<<"3.- cambiar nombre del profesor"<<endl;
    cout<<"4.- salir"<<endl;
    cin>>opc;
    while(c=1){
    switch(opc){
    case(1):
        system("cls");
        clase.imprime();
        break;
    case(2):
        system("cls");
        clase.cambiaClave();
        clase.imprime();
        break;
    case(3):
        system("cls");
        clase.cambiaProfe();
        clase.imprime();
        break;
    case(4):
        system("cls");
        c=0;
        break;
    default:
        cout<<"opcion no valida"<<endl;
        break;
    }
    break;
}
}
