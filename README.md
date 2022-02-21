#include <stdio.h>
#include <stdlib.h>

/* run this program using the console pauser or add your own getch, system("pause") or input loop */

int main()
{



int tam = 10; // ORDEM DA MATRIZ
int linha, coluna, x,y; // CONTROLE DE NAVEGAÇÃO
int mat[tam][tam]; // DEFINE MATRIZ



srand(time(0)); // SEMENTE GERADORA


// POPULAR A MATRIZ
for(linha = 0; linha < tam; linha++){
	for(coluna = 0; coluna < tam; coluna++){
		mat[linha][coluna] = rand()%100;
	}
}



// EXIBE A MATRIZ
for(linha = 0; linha < tam; linha++){
	for(coluna = 0; coluna < tam; coluna++){
		printf("%3d", mat[linha][coluna]);
	}
	printf("\\n");
}


// EXIBE DIAGONAL PRINCIPAL
printf("\\n");
for(x=0; x < tam; x++){
	printf("%3d", mat[x][x]);
}

// EXIBE DIAGONAL SECUNDARIA
    printf("\\n");
	for(y=0; y < tam; y++){
		printf("%3d", mat[y][tam-1-y]);

	}
return 0;
