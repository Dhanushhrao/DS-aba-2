#include<stdio.h>
#include<stdlib.h>
struct node
{
  int info;
  
  struct node*link;
};
typedef struct node*NODE;

NODE getnode()
{
  NODE x;
  x=(NODE)malloc(sizeof(struct node));
  
  if(x==NULL)
  {
    printf("Out of memory\n");
    exit(0);
  }
  return x;
}

NODE insert_rear(int item,NODE first)
{  NODE temp,cur;
  temp = getnode();
  temp->info=item;
  temp->link=NULL;
  if(first ==NULL)
   return temp;
  cur=first;
  while(cur->link!=NULL){
    cur=cur->link;
  }
  cur->link=temp;
  return first; 
}

void display(NODE first)
{
  NODE cur;
  if(first==NULL)
  {
    printf("List is empty\n");
    return;
  }
  printf("The contents of sigly linked list\n");

  cur=first;
  while(cur!=NULL)
  {
    printf("%d ",cur->info);
    cur=cur->link;
  }
  printf("\n");
}

NODE delete_front(NODE first)
{
  NODE temp;
  if(first==NULL)
  {
    printf("List is empty");
    return NULL;
  }
  temp=first;
  temp=temp->link;
  printf("Item deleted=%d\n",first->info);
  free(first);
  return temp;
 }
  

int main()
{
  NODE first;
  int choice,item,n,i;
  first=NULL;
   printf("1.Insert Front\n2.Delete Front\n3.Display\n4.Exit\n");
  for(;;)
  {
   printf("Enter your choice: ");
   scanf("%d",&choice);
   switch(choice)
   {
     case 1:
            printf("Enter the number of nodes\n");
            scanf("%d",&n);
            for(i=1;i<=n;i++)
            {
              printf("Enter the item to be inserted\n");
            scanf("%d",&item);
            first=insert_rear( item,first);
            }
            
            break;
    case 2:
             
            first=delete_front(first);
            break;
    case 3:
            
            display(first);
            break;
    default:
            exit(0);
   }
  }
}
