#include <stdio.h>
#include<stdlib.h>

int main() {

  int i, *N, *aux, v=0, v1=19;
  N=(int*)malloc(20*sizeof(int));
  aux=(int*)malloc(sizeof(int));

  for(i=0;i<20;i++){
      scanf("%i",&N[i]);
  }
  while(v<v1){
      *aux=*(N+v);
      *(N+v)=*(N+v1);
      *(N+v1)=*aux;
      v+=1;
      v1-=1;
  }
  for(i=0;i<20;i++){
      printf("N[%i] = %i\n",i,*(N+i));
  }
    return 0;
}
