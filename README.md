# C
#include <stdio.h>
#include <locale.h>

int main(){
    setlocale(LC_ALL, "Portuguese");
   //varivais
   int menu=1,estsuco,estrefri,estsal,estsalass,estdoce,comprar=1,comprarsuco=0,comprarrefri=0,comprarsal=0,comprarsalass=0,comprardoce=0,
   qtdsucovend=0,qtdrefrivend=0,qtdsalvend=0,qtdsalassvend=0,qtddocevend=0,repor=1,qtdsucorepor=0,qtdrefrirepor=0,qtdsalrepor=0,qtdsalassrepor=0,qtddocerepor=0,
   cadastrarsuco=0,cadastrarrefri=0,cadastrarsal=0,cadastrarsalass=0,cadastrardoce=0;
   float valsuco,valrefri,valsal,valsalass,valdoce,totalparcial=0,totalcompra=0;
   
   //inicializaçao do programa para pedir informação da quantidade do estoque de cada produto
   printf("\n-------------INFORME O ESTOQUE DOS PRODUTOS-------------------\n");
   while(cadastrarsuco <=0){//nao vai sair do while ate que recebar 1
     printf("Quantidade do produto 01 - suco(garrafa 500 ml):\n");
     scanf("%d",&estsuco);
     printf("valor do produto 01 - suco(garrafa 500 ml)R$:\n");
     scanf("%f",&valsuco);
     printf("-----------------------------------------------\n");
     if(estsuco <=0 || valsuco <=0){//vai verificar se o estoque esta com o valor maior que zero
         printf("\ninforme um valor maior que zero para o estoque e valor\n");
         getch();
         system("cls");
         printf("\n---------------------------INFORME O ESTOQUE DOS PRODUTOS-------------------\n");
     }
     else //se o estoque for maior que zero então o cadastro de suco vai receber 1 e sair do laço
     cadastrarsuco=1;
     
   }
   while(cadastrarrefri <=0){//nao vai sair do while ate que recebar 1
     printf("\nQuantidade do produto 02 - refrigerante(lata):\n");
     scanf("%d",&estrefri);
     printf("\nvalor do produto 02 - refrigerante(lata)R$:\n");
     scanf("%f",&valrefri);
     printf("-----------------------------------------------\n");
     if(estrefri <=0 || valrefri <=0){//vai verificar se o estoque esta com o valor maior que zero
         printf("\ninforme um valor maior que zero para o estoque e valor\n");
         getch();
       //  system("cls");
         printf("\n---------------------------INFORME O ESTOQUE DOS PRODUTOS-------------------\n");
     }
     else //se o estoque for maior que zero então o cadastro de suco vai receber 1 e sair do laço
     cadastrarrefri=1;
     
   }
   while(cadastrarsal <=0){//nao vai sair do while ate que recebar 1
     printf("\nQuantidade do produto 03 - salgadinho frito:\n");
     scanf("%d",&estsal);
     printf("\nvalor do produto 03 - salgadinho frito R$:\n");
     scanf("%f",&valsal);
     printf("\n-----------------------------------------------\n");
     if(estsal <=0 || valsal <=0){//vai verificar se o estoque esta com o valor maior que zero
         printf("\ninforme um valor maior que zero para o estoque e valor\n");
         getch();
        // system("cls");
         printf("\n---------------------------INFORME O ESTOQUE DOS PRODUTOS-------------------\n");
     }
     else //se o estoque for maior que zero então o cadastro de suco vai receber 1 e sair do laço
     cadastrarsal=1;
     
   }
     while(cadastrarsalass <=0){//nao vai sair do while ate que recebar 1
     printf("\nQuantidade do produto 04 - salgadinho assado:\n");
     scanf("%d",&estsalass);
     printf("\nvalor do produto 04 - salgadinho assado R$:\n");
     scanf("%f",&valsalass);
     printf("\n-----------------------------------------------\n");
     if(estsalass <=0 || valsalass <=0){//vai verificar se o estoque esta com o valor maior que zero
         printf("\ninforme um valor maior que zero para o estoque e valor\n");
         getch();
         system("cls");
         printf("\n---------------------------INFORME O ESTOQUE DOS PRODUTOS-------------------\n");
     }
     else //se o estoque for maior que zero então o cadastro de suco vai receber 1 e sair do laço
     cadastrarsalass=1;
     
   }
   while(cadastrardoce <=0){//nao vai sair do while ate que recebar 1
     printf("\nQuantidade do produto 05 - doce:\n");
     scanf("%d",&estdoce);
     printf("\nvalor do produto 05 - doce R$:\n");
     scanf("%f",&valdoce);
     printf("\n-----------------------------------------------\n");
     if(estdoce <=0 || valdoce <=0){//vai verificar se o estoque esta com o valor maior que zero
         printf("\ninforme um valor maior que zero para o estoque e valor\n");
         getch();
        // system("cls");
         printf("\n---------------------------INFORME O ESTOQUE DOS PRODUTOS-------------------\n");
     }
     else //se o estoque for maior que zero então o cadastro de suco vai receber 1 e sair do laço
     cadastrardoce=1;
     
   }
   while(menu != 0){
      // system("cls");
       printf("\n====================BEM-VINDO AO MENU DA CANTINA===================\n");
       printf("\n 1-Vender\n 2-Consular estoque\n 3-Consular lucro\n 4-Repor estoque\n 0-Sair\n");
       scanf("%d",&menu);
       switch(menu){
           case 1: 
           while(comprar !=0){
              // system("cls");
               printf("\n====================QUAL PRODUTO QUE DESEJA COMPRAR==============\n");
               printf("\nProduto                      Preço\n");
               printf("\n---------------------------------\n");
               printf("\n 1-Suco(garrafa 500 ml) R$: %.2f\n"
                      "\n 2-Refrigerante(lata) R$: %.2f\n"
                      "\n 3-Salgadinho Frito R$: %.2f\n"
                      "\n 4-Salgadinho Assado R$: %.2f\n"
                      "\n 5-Doce R$: %.2f\n"
                      "\n 0-Encerrar Compra\n",
                      valsuco,valrefri,valsal,valsalass,valdoce);
                      scanf("%d",&comprar);
                     // system("cls");
                      switch(comprar){
                          case 1:
                          if(estsuco >0){
                              while(comprarsuco<=0){
                                 // system("cls");
                                  printf("\n Produto              Preço\n");
                                  printf("\n--------------------------\n");
                                  printf("\n Suco (garrafa 500 ml) R$: %2.f\n",valsuco);
                                  printf("\n-----------------------------------------\n");
                                  printf("\n Quantas garrafas de suco deseja compra:\n");
                                  scanf("%d",&comprarsuco);
                                  if(comprarsuco <= estsuco && comprarsuco > 0){
                                      qtdsucovend+=comprarsuco;
                                      estsuco = estsuco - comprarsuco;
                                      totalparcial += comprarsuco * valsuco;
                                      printf("\n o valor ficou em R$: %.2f\n",comprarsuco*valsuco);
                                  }
                                  else if(comprarsuco <=0){
                                      printf("\n informe um valor maior que zero\n");
                                      printf("\n-----------------------------------\n");
                                      getch();
                                  }
                                  else
                                  printf("\nDesculpe mais o estoque e insuficiente para o seu pedido.\n");
                                  
                              }
                              comprarsuco=0;
                          }
                          else
                          printf("\nDesculpe mais o estoque esta vazio!\n");
                          getch();
                          break;
                          
                          case 2:
                          if(estrefri >0){
                              while(comprarrefri<=0){
                               //   system("cls");
                                  printf("\nProduto              Preço\n");
                                  printf("\n--------------------------\n");
                                  printf("\n refrigerante em lata R$: %2.f\n",valrefri);
                                  printf("\n-----------------------------------------");
                                  printf("\n Quantas refrigerante deseja compra:\n");
                                  scanf("%d",&comprarrefri);
                                  if(comprarrefri <= estrefri && comprarrefri > 0){
                                      qtdrefrivend+=comprarrefri;
                                      estrefri = estrefri - comprarrefri;
                                      totalparcial += comprarrefri * valrefri;
                                      printf("\n o valor ficou em R$: %.2f\n",comprarrefri*valrefri);
                                  }
                                  else if(comprarrefri <=0){
                                      printf("\n informe um valor maior que zero\n");
                                      printf("\n-----------------------------------");
                                      getch();
                                  }
                                  else
                                  printf("\nDesculpe mais o estoque e insuficiente para o seu pedido.\n");
                                  
                              }
                              comprarrefri=0;
                          }
                          else
                          printf("\nDesculpe mais o estoque esta vazio!\n");
                          getch();
                          break;
                          
                          case 3:
                          if(estsal >0){
                              while(comprarsal<=0){
                                //  system("cls");
                                  printf("\nProduto              Preço\n");
                                  printf("\n--------------------------\n");
                                  printf("\n Salgadinho Frito  R$: %2.f\n",valsal);
                                  printf("\n-----------------------------------------\n");
                                  printf("\n Quantas Salgadinho Frito deseja compra:\n");
                                  scanf("%d",&comprarsal);
                                  if(comprarsal <= estsal && comprarsal > 0){
                                      qtdsalvend+=comprarsal;
                                      estsal = estsal - comprarsal;
                                      totalparcial += comprarsal * valsal;
                                      printf("\n o valor ficou em R$: %.2f\n",comprarsal*valsal);
                                  }
                                  else if(comprarsal <=0){
                                      printf("\n informe um valor maior que zero\n");
                                      printf("\n-----------------------------------");
                                      getch();
                                  }
                                  else
                                  printf("\nDesculpe mais o estoque e insuficiente para o seu pedido.\n");
                                  
                              }
                              comprarsal=0;
                          }
                          else
                          printf("\nDesculpe mais o estoque esta vazio!\n");
                          getch();
                          break;
                          
                          case 4:
                          if(estsalass >0){
                              while(comprarsalass<=0){
                                  system("cls");
                                  printf("\nProduto              Preço\n");
                                  printf("\n--------------------------\n");
                                  printf("\n Salgadinho Assado R$: %2.f\n",valsalass);
                                  printf("\n-----------------------------------------\n");
                                  printf("\n Quantas Salgadinho Assado deseja compra:\n");
                                  scanf("%d",&comprarsalass);
                                  if(comprarsalass<= estsalass && comprarsalass > 0){
                                      qtdsalassvend+=comprarsalass;
                                      estsalass = estsalass - comprarsalass;
                                      totalparcial += comprarsalass * valsalass;
                                      printf("\n o valor ficou em R$: %.2f\n",comprarsalass*valsalass);
                                  }
                                  else if(comprarsalass <=0){
                                      printf("\n informe um valor maior que zero\n");
                                      printf("\n-----------------------------------\n");
                                      getch();
                                  }
                                  else
                                  printf("\nDesculpe mais o estoque e insuficiente para o seu pedido.\n");
                                  
                              }
                              comprarsalass=0;
                          }
                          else
                          printf("\nDesculpe mais o estoque esta vazio!\n");
                          getch();
                          break;
                          case 5:
                          if(estdoce >0){
                              while(comprardoce<=0){
                                  system("cls");
                                  printf("\nProduto              Preço\n");
                                  printf("\n--------------------------\n");
                                  printf("\n Doce R$: %2.f\n",valdoce);
                                  printf("\n-----------------------------------------\n");
                                  printf("\n Quantas Doces deseja compra:\n");
                                  scanf("%d",&comprardoce);
                                  if(comprardoce <= estdoce && comprardoce > 0){
                                      qtddocevend+=comprardoce;
                                      estdoce = estdoce - comprardoce;
                                      totalparcial += comprardoce * valdoce;
                                      printf("\n o valor ficou em R$: %.2f\n",comprardoce*valdoce);
                                  }
                                  else if(comprardoce <=0){
                                      printf("\n informe um valor maior que zero\n");
                                      printf("\n-----------------------------------\n");
                                      getch();
                                  }
                                  else
                                  printf("\nDesculpe mais o estoque e insuficiente para o seu pedido.\n");
                                  
                              }
                              comprardoce=0;
                          }
                          else
                          printf("\nDesculpe mais o estoque esta vazio!\n");
                          getch();
                          break;
                          
                          case 0:
                          printf("\nObrigador por realizar a comprar na nossa cantina..\n");
                            printf("\n------------------------------------\n");
                            printf("\n A sua comprar ficou em R$: %.2f\n",totalparcial);
                            break;
                            default:
                            printf("\nDesculpa mais o codigo não encotrado \n Aperte qualquer tecla para continuar...");
                            getch();
                            break;
                      }
           }
           comprar=1;
           totalcompra += totalparcial;
           totalparcial=0;
           break;
           
           case 2:
         //  system("cls");
           printf("\n===================Bem-vindo ao Estoque Da Catina================\n");
           printf("\nProduto || Qantidade em estoque valor do produto || Valor do Estoque\n ");
           printf("---------------------------------------------------------------------\n");
           printf(" Suco             %d garrafas 500 ml R$: %.2f             R$: %.2f\n",estsuco,valsuco,estsuco*valsuco);
           printf(" Refrigerante     %d lata R$: %.2f                        R$: %.2f\n",estrefri,valrefri,estrefri*valrefri);
           printf(" Salgadinho FR    %d salgadinho R$: %.2f                  R$: %.2f\n",estsal,valsal,estsal*valsal);
           printf(" Salgadinho AS    %d salgadinho assado R$: %.2f           R$: %.2f\n",estsalass,valsalass,estsalass*valsalass);
           printf(" Doce             %d doce R$: %.2f                        R$: %.2f\n",estdoce,valdoce,estdoce*valdoce);
           printf("\n------------------------------------------------------------------------------------------------------\n");
           printf("\n O valor total do estoque R$: %.2f",(estsuco*valsuco)+(estrefri*valrefri)+(estsal*valsal)+(estsalass*valsalass)+(estdoce*valdoce));
           break;
           
           case 3:
         //  system("cls");
           printf("\n===================Total de Vendas da Cantina========================\n");
           printf("\nProduto  ||  Quantidade vendido valor da venda\n ");
           printf("Suco                %d garrafas 500 ml R$: %.2f \n",qtdsucovend,qtdsucovend*valsuco);
           printf("Refrigerante        %d lata R$: %.2f \n",qtdrefrivend,qtdrefrivend*valrefri);
           printf("salgadinho FR       %d salgadinho R$: %.2f \n",qtdsalvend,qtdsalvend*valsal);
           printf("salgadinho AS       %d salgadinho assado R$: %.2f \n",qtdsalassvend,qtdsalassvend*valsalass);
           printf("Doce                %d doce R$: %.2f \n",qtddocevend,qtddocevend*valdoce);
           printf("Total R$: %.2f",(qtdsucovend*valsuco)+(qtdrefrivend*valrefri)+(qtdsalvend*valsal)+(qtdsalassvend*valsalass)+(qtddocevend*valdoce));
           break;
           
           case 4:
           while(repor !=0){
            //   system("cls");
               printf("\n===================Repor estoque da Cantina====================\n");
               printf("Informe qual produto que deseja repor no estoque\n");
               printf("\n----------------------------------------------\n");
               printf("\n Produto || Quantidade no estoque");
               printf("\n 1- Suco (garrafas 500 ml) %d garrafas\n"
                      "\n 2- Refrigerante (lata) %d lata\n"
                      "\n 3- Salgadinho Frito %d unidade\n"
                      "\n 4- Salgadinho Assado %d unidade\n"
                      "\n 5- Doce %d unidade\n"
                      "\n 0- Encerrar \n",estsuco,estrefri,estsal,estsalass,estdoce);
                      scanf("%d",&repor);
                      switch(repor){
                          case 1:
                         // system("cls");
                          while(qtdsucorepor <=0){
                              printf("\nProduto || Quantidade\n");
                              printf("\n----------------------------\n");
                              printf("\n Suco (garrafas 500 ml) %d\n",estsuco);
                              printf("\n----------------------------------");
                              printf("\n Informe a quantidade de garrafas de suco\n");
                              scanf("%d",&qtdsucorepor);
                              if(qtdsucorepor>0){
                                  estsuco+=qtdsucorepor;
                                  printf("\n O novo estoque de suco é: %d\n",estsuco);
                              }
                              else
                              printf("\n Informe uma quantidade maior que zero\n");
                              getch();
                            //  system("cls");
                          }
                          qtdsucorepor=0;
                          break;
                          
                          case 2:
                         // system("cls");
                          while(qtdrefrirepor <=0){
                              printf("\nProduto || Quantidade\n");
                              printf("\n----------------------------\n");
                              printf("\n Refrigerante em lata %d\n",estrefri);
                              printf("\n----------------------------------");
                              printf("\n Informe a quantidade de latas de refrigerante\n");
                              scanf("%d",&qtdrefrirepor);
                              if(qtdrefrirepor>0){
                                  estrefri+=qtdrefrirepor;
                                  printf("\n O novo estoque de refrigerante é: %d\n",estrefri);
                              }
                              else
                              printf("\n Informe uma quantidade maior que zero\n");
                              getch();
                            //  system("cls");
                          }
                          qtdrefrirepor=0;
                          break;
                          
                          case 3:
                        //  system("cls");
                          while(qtdsalrepor <=0){
                              printf("\nProduto || Quantidade\n");
                              printf("\n----------------------------\n");
                              printf("\n Salgadinho Frito %d\n",estsal);
                              printf("\n----------------------------------\n");
                              printf("\n Informe a quantidade de salgadinho frito\n");
                              scanf("%d",&qtdsalrepor);
                              if(qtdsalrepor>0){
                                  estsal+=qtdsalrepor;
                                  printf("\n O novo estoque de salgadinho frito é: %d\n",estsal);
                              }
                              else
                              printf("\n Informe uma quantidade maior que zero\n");
                              getch();
                            //  system("cls");
                          }
                          qtdsalrepor=0;
                          break;
                          
                          case 4:
                         // system("cls");
                          while(qtdsalassrepor <=0){
                              printf("\nProduto || Quantidade\n");
                              printf("\n----------------------------\n");
                              printf("\n Salgadinho Assado %d\n",estsalass);
                              printf("\n----------------------------------\n");
                              printf("\n Informe a quantidade de salgadinho assado\n");
                              scanf("%d",&qtdsalassrepor);
                              if(qtdsalassrepor>0){
                                  estsalass+=qtdsalassrepor;
                                  printf("\n O novo estoque de salgadinho assado é: %d\n",estsalass);
                              }
                              else
                              printf("\n Informe uma quantidade maior que zero\n");
                              getch();
                              //system("cls");
                          }
                          qtdsalassrepor=0;
                          break;
                          
                          case 5:
                         // system("cls");
                          while(qtddocerepor <=0){
                              printf("\nProduto || Quantidade\n");
                              printf("\n----------------------------\n");
                              printf("\n Doce %d\n",estdoce);
                              printf("\n----------------------------------");
                              printf("\n Informe a quantidade de doce\n");
                              scanf("%d",&qtddocerepor);
                              if(qtddocerepor>0){
                                  estdoce+=qtddocerepor;
                                  printf("\n O novo estoque de doce é: %d\n",estdoce);
                              }
                              else
                              printf("\n Informe uma quantidade maior que zero\n");
                              getch();
                             // system("cls");
                          }
                          qtddocerepor=0;
                          break;
                          
                          case 0:
                          printf("\nEstoque reposto com sucesso.\n ");
                          break;
                          
                          default:
                          printf("\nCodigo não encotrado! \n Aperte qualquer tecla para continuar... ");
                          break;
                      }
           }
           repor=1;
           break;
           case 0:
           // system("cls");
            printf("\n===================Relatorio Final do Dia da Cantina====================\n");
            printf("\nProduto   ||  Quantidade Vendido no Estq. Valor do Prod   ||   Valor do Estq\n ");
            printf("--------------------------------------------------------------------------\n");
            printf(" Suco               %d garrafas 500 ml R$: %.2f                       R$: %.2f\n",qtdsucovend,estsuco,valsuco,estsuco*valsuco);
            printf(" Refrigerante       %d lata R$: %.2f                                  R$: %.2f\n",qtdrefrivend,estrefri,valrefri,estrefri*valrefri);
            printf(" Salgadinho FR      %d salgadinho fr R$: %.2f                         R$: %.2f\n",qtdsalvend,estsal,valsal,estsal*valsal);
            printf(" Salgadinho AS      %d salgadinho as R$: %.2f                         R$: %.2f\n",qtdsalassvend,estsalass,valsalass,estsalass*valsalass);
            printf(" Doce               %d doce R$: %.2f                                  R$: %.2f\n",qtddocevend,estdoce,valdoce,estdoce*valdoce);
            printf("--------------------------------------------------------------------------------------------------\n");
            //printf("\nQuantidade de vendas efetuadas: %d\n",qtdsucovend,qtdrefrivend,qtdsalvend,qtdsalassvend,qtddocevend);
            printf("--------------------------------------------------------------------------------------------------\n");
            printf("\n O lucro total do dia R$: %.2f",(qtdsucovend*valsuco)+(qtdrefrivend*valrefri)+(qtdsalvend*valsal)+(qtdsalassvend*valsalass)+(qtddocevend*valdoce));
            break;
            
            default:
            printf("\nCodigo não encontrado!\n");
            break;
           }
           getch();
          // system("cls");
   }
   
    return 0;
}
