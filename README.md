# DSA-
#include<stdio.h>
#include<conio.h>
#include<stdlib.h>
typedef struct lklist
{
int data;
struct lklist*next;
}node;

void linklistTraverse(node *start)
{
  while(start != NULL)
   {
     printf("%d/n",start->data);
     start=start->next;
   }

}

int main()
{
//clrscr();
node *head;
node *second;
node *third;
node *fourth;

head = (node*)malloc(sizeof(node));
second = (node*)malloc(sizeof(node));
third = (node*)malloc(sizeof(node));
fourth = (node*)malloc(sizeof(node));

head->data=2;
head->next=second;

second->data=4;
second->next=third;

third->data=6;
third->next=fourth;

fourth->data=8;
fourth->next=NULL;

linklistTraverse(head);

getch();
return 0;
}
