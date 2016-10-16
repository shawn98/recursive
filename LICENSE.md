#include<stdio.h>
int Multiple(int a,int b){
	if(b==0) return 0;
	if(b==1) return a;
	if(b%2==0) return 2*Multiple(a,b/2); 
	else return 2*Multiple(a,b/2)+a; 
}
/*------------------------------------------*/
int Power(int a,int b){
	if(b==0) return 0;
	if(b==1) return a;
	if(b%2==0) return Power(Multiple(a,a),b/2);
	else return Multiple(a,Power(a,b-1));
} 
/*---------------------------------------------*/
int main(){
	printf("%d\n",Multiple(7,6));
	printf("%d\n",Power(3,2));
	return 0;
}
