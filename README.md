/******************************************************************************
    Autor....:Israel Salles de Oliveira
    Data.....:17/07/2025
    Objetivo.:holerite
*******************************************************************************/
#include <stdio.h>
#include <stdlib.h>

int main(void) 
{ 
	 //declarando variaveis

    	char nome[50];   
    	int idade; 
    	char cargo[50];  
    	float gratificacao;    
    	float salario_bruto;    
    	float salario_com_desconto;  
    	float salario_liquido;  
    	float reajuste;
        int opcao;
	 //leitura de dados
   
        	printf("   Digite seu nome..........: ");
        	fgets(nome, sizeof(nome),stdin);
            printf ("   Jovem Aprendiz?\n   [1] - sim \n   [2] - nao \n   ");
            scanf("%d",&opcao);
            if (opcao==1)
            {
             salario_bruto= 956.00;
            }
            else
            {
                printf("   Digite seu salario bruto....: ");
                scanf("%f", &salario_bruto);
            }
    // Limpar buffer de entrada para evitar problemas com fgets depois do scanf
            int c;
            for (c = getchar(); c != '\n' && c != EOF; c = getchar());

        	printf("   Digite seu cargo.........: ");
        	fgets(cargo, sizeof(cargo),stdin);
        	printf("   Digite sua idade.........: ");
        	scanf("%d", &idade);
            if ( opcao==1 )
			{
                if (idade>=14)
                {
                if (idade<=21)
                {
                }else
                {
                    printf("	ACESSO NEGADO !\n"); 
                    return 0;
                }
                
                
                }
                else
                {
                    printf("	ACESSO NEGADO !\n"); 
				return 0;
                }
                
                
			}
			else
			{
			}
	 //contas

        reajuste =  (salario_bruto * 38 ) / 100 + salario_bruto;      
        gratificacao = (reajuste * 20 ) / 100 ;       
        salario_com_desconto = ((reajuste + gratificacao) * 15) / 100 ;       
        salario_liquido = (reajuste + gratificacao) - salario_com_desconto ;
	
     //imprimir
 
        printf("                                        \n");
    	printf("\tNome...........................: %s ", nome);
    	printf("\tCargo..........................: %s ", cargo);
    	printf("\tIdade..........................: %d anos \n",idade);
    	printf("\tSalario bruto anterior.........: R$ %.2f \n", salario_bruto);
    	printf("\tSeu reajuste e igual...........: R$ %.2f \n", reajuste);
    	printf("\tSua gratificacao e igual.......: R$ %.2f \n", gratificacao);
    	printf("\tSera descontado de seu salario.: R$ %.2f \n", salario_com_desconto);
    	printf("\tSeu salario liquido e igual....: R$ %.2f \n", salario_liquido);
      
	return 0;

}
