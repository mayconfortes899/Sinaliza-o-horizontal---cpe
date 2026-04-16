# Sinaliza-o-horizontal---cpe

#include <iostream>
#include <stdio.h>
#include <vector>
#include <iomanip>
 
  using namespace std;
  struct compras {
   string tipotinta;
   string 
  };
  struct pessoa{
      string celular;
      string email;
      string senha;
      string datanasc;
      string cpf;
      string nome;
  };

   int main (){
      int  contador=0;
      vector<pessoa>lista;
    string N;
    int opcoes;
    while(true){ 
      system ("cls");
   //menu
     cout<<"\t**********************\t"<<endl;
     cout<< " \t SEJA BEM-VINDO AO NOSSO SERVICO\t"<<endl;
     cout<<" O que deseja fazer hoje ? "<<endl;
     cout<<"1-Cadastrar"<<endl;
     cout<<"2-Entrar"<<endl;
     cout<<"3-sair"<<endl;

      cin>>opcoes;
     switch(opcoes){
        case 1:
         
        pessoa novapessoa;
             system("cls");
         cout<<"*****Preenchimento de Cadastro*****"<<endl;
         cout<<"Primeiro nome: "<<endl;
          cin>>novapessoa.nome;
         cout<<"\nNumero de telefone: \n";
         cin>> novapessoa.celular;
         cout<<"E-mail: "<<endl;
         cin>>novapessoa.email;
         cout<<"Senha: "<<endl;
         cin>>novapessoa.senha;
            lista.push_back(novapessoa); // adiciona a pessoa no final da fila
            cout<<"Sucesso! Cadastro realizado com sucesso."<<endl;
       break;
      }
       case 2:
         system("cls");
           if(lista.empty()){
            cout<<"Desculpe, nenhum usuario cadastrado."<<endl;
            break;
           } else{
            string emailLogin, senhaLogin;
               cout<<"\n ----- LOGIN -----";
              cout<<"Digite seu E-mail: ";
              cin>>emailLogin;

              cin>>senhaLogin;
               vector<pessoa>::iterator it;
               bool logado=false;
                for(it=lista.begin(); it!=lista.end();it++){ 
                   if(it->email == emailLogin && it->senha == senhaLogin){
                    logado=true;
                    break;
                   } if(logado){ // a partir deste momento, o iterador(ponteiro) estará apenas apontando 
                    cout<<"Seja Bem vindo, "<<it->nome <<endl;
                    cout<< "\t --------- MENU DE COMPRAS --------- \t"<<endl;
                    cout<<

                    break;
                   }
              
           }
        case 3:
          cout<<"Ate mais!"<<endl;
        return 0;
          break;
       
     }
       





  

    
    return  0;
  }
