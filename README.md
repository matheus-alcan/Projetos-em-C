#include <stdio.h>
#include <stdlib.h>
 
void main(){
	int p, e, y, f, i;
	float v=0 ,v1=0 ,v2=0 ,v3=0 ,d=0 ,d1=0 ,d2=0 ,d3=0 ,soma=0 ,c=0,r=0,b=0;
	
	printf("\nInforme o valor do primeiro produto:");
	scanf("%f",&v1);
 
	printf("\nInforme o valor do segundo produto:");
	scanf("%f",&v2);
	printf("\nInforme o valor do terceiro produto:");
	scanf("%f",&v3);
	
	v = v1+v2+v3;
	
	printf("\nValor: R$%.2f\n",v);
	printf("\nInforme o valor do primeiro produto:");
	scanf("%f",&d1);
	printf("\nInforme o valor do segundo produto:");
	scanf("%f",&d2);
	printf("\nInforme o valor do terceiro produto:");
	scanf("%f",&d3);
	
	d = (d1+d2+d3)*5.46;
	
	printf("\nValor convertido em reais: R$%.2f\n",d);
	printf("\nMenu:");
	printf("\n1 - Geladeira - R$2500");
	printf("\n2 - Cama - R$1500");
	printf("\n3 - Sofa - R$2000");
	printf("\nInforme o produto escolhido:");
	scanf("%i",&p);
	
	if(p == 1){
		y=2500;
		printf("\nValor da compra: R$ %d\n",y);
	}else if(p == 2){
		y=1500;
		printf("\nValor da compra: R$ %d\n",y);
	}else if(p == 3){
		y=2000;
		printf("\nValor da compra: R$ %d\n",y);
	}else{
		printf("\nOpcao Invalida");
	}
	
	printf("\nMenu:");
	printf("\n1 - Iphone - 1500 dolares");
	printf("\n2 - Xiaomi - 1000 dolares");
	printf("\n3 - Hoverboard - 5000 dolares\n");
	printf("\nInforme o produto importado escolhido:");
	scanf("%c",&e);
	
	switch(e){
		case '1' :
			r=1500*5.46;
			printf("Valor da compra em reais: R$%.2f\n",r);
			break;
		case '2' :
			r=1000*5.46;
			printf("Valor da compra em reais: R$%.2f\n",r);
			break;
		case '3' :
			r=5000*5.46;
			printf("Valor da compra em reais: R$%.2f\n",r);
			break;
	}
	
	getchar();
	soma = r + v + d + y;
	
	printf("\nValor da soma dos subtotais: R$%.2f\n",soma);
	printf("\nMenu de formas de pagamento:");
	printf("\n1 - Pagamento a vista - desconto de 12%%");
	printf("\n2 - Pagamento a prazo - acrescimo de 15%%");
	printf("\n3 - Parcela em 6x - acrescimo de 19%%");
	printf("\nInforme a forma de pagamento escolhida:");
	scanf("%i",&f);
	
	switch(f){
		case 1 :
			b=soma*0.88;
			break;
		case 2 :
			b=soma*1.15;
			break;
		case 3 :
			b=(soma/6)*1.19;
			break;
	}
	getchar();
	
	printf("\nValor do pedido: R$%.2f\n",b);
	printf("\nMenu de entrega:");
	printf("\n1 - Entrega Expressa - taxa de 11%%");
	printf("\n2 - Entrega convencional - taxa de 5%%");
	printf("\n3 - Retirar a compra na empresa - taxa de 0%%");
	printf("\nInforme a forma de entrega escolhida:");
	scanf("%i",&i);
	
	if(i == 1){
		c=b*1.11;
		printf("\nValor a pagar: R$%.2f\n",c);
	}else if("i == 2"){
		c=b*1.05;
		printf("\nValor a pagar: R$%.2f\n",c);
	}else if("i == 3"){
		c=b;
		printf("\nValor a pagar: R$%.2f\n",c);
	}else{
		printf("\nOpcao Invalida");
	}
	getchar();
}
