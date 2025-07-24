# AULAS---240725
CODIGOS C NO DEVC ++
//BOLETIM ESCOLAR 

#include <stdio.h>
#include <string.h>
int main(){
	char nome [50]; // vetor 
	float n1,n2; // variaveis
	
	printf("===================================\n");
	printf( "Dados dos Alunos -IBC\n");
    printf("===================================\n");
	printf("Digite seu nome. (Ex : Ana Julia Barros):");
	fgets(nome, sizeof(nome),stdin); // leitura de uma string acima com espaços 
	nome [strcspn(nome,"\n")]='\0'; // tirar quebra de linha 
	printf ("Digite a primeira nota. (Ex: 9.2): "); // para o usuario inserir suas informacoes
	scanf("%f",&n1); //guarda a variavel digitada 
	getchar(); //captura o enter apos o usuario digitar 
	printf("Digite a segunda nota.(Ex: 7.8): ");
	scanf("%f",&n2);
	getchar();
	
	 float media = (n1+n2)/2;
	
	printf("\n----BOLETIM----");
	if (media>=7){
		 printf("\nAluno: %s",nome);
		 printf("\nStatus:APROVADO");
		 printf("\Media:%.1f",media);
	}else if (media>=5){
		printf("\nAluno: %s", nome);
		printf("\nStatus: RECUPERACAO");
		printf("\nMedia: %.1f", media);
	}else{
	      printf("\nAluno: %s", nome);
		  printf("\nStatus: REPROVADO");
		  printf("\nMedia: %.1f", media);
	}
	return 0;	
	} 
	
