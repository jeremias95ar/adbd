## Codigo en C++


#include <iostream>
#include <unordered_map>
using namespace std;

int main()
{
    unordered_map <string,long> umap;


    int str =9;
    int integer = 1;
    int lon =7;
    int doub = 1;
    int date = 1;
    umap["integer"] = 2*integer;
    umap["Long"] = 4*lon;
    umap["Double"] = 8* doub;
    umap["Date"] = 8*date;
    umap["String"] = 10*str;
    long sum =0;
    long registros= 50627392;
    long filas =35;
    cout<<"Valor en bytes de cada tipo"<<endl;
    for (auto x : umap){
        cout <<x.first<<" "<<x.second<< " bytes" <<endl;
        sum+=x.second;
    }
    cout<< "Fila: "<< sum<< endl;
    cout<< "Pagina: "<< filas*sum<<endl;
    cout<<"Total: "<<sum*registros*filas<< "bytes"<<endl;

    return 0;
}

