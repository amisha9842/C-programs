# C-programs
#include <stdio.h>
//define 10;
int array[10];  //outside main function
int top=-1;
void push()
{
  int x,j;
  for(j=0;j<=4;j++)
    {
  printf("enter data to insert");
  scanf("%d",&x); 
  if(top==4)
  {
    printf("overflow");
  }
  else
  {
    top++;
    array[top]=x;
  }
      }
}

void pop()
{
  if(top==-1)
  {
    printf("stack underflow\n");
  }
  else
  {
    int temp;
    temp=array[top];
    top--;
    printf("the popped element is %d \n",temp);
  }
  
}
void peep()
{
  if(top==-1)
  {
    printf("stack is empty\n");
  }
  else
  {
  int temp;
  temp=array[top];
  printf("the peeped element is %d \n ",temp);
  }
}
void display()
{
  int i;
  for(i=top;i>=0;i--)
    {
      printf("%d \n",array[i]);
    }
} 

int main(void)
{
  push();
  printf("after inserting the data,the stack is:\n");
  display();
  pop();
  printf("after deletion the stack is\n");
  display();
  peep();
}
