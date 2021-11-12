#include<stdio.h>

#include<string.h>





int main()

{

  char name[23],father[100],mother[100],password1[10],password2[10];

  int age,ac=33354678,start,balance=0,choice,add=0,value;

  printf("enter 1 to create a new account:");

  scanf("%d",&start);

  if(start==1)

  {

  printf("enter your name\n");

  scanf("%s",name);

  printf("enter your age\n");

  scanf("%d",&age);

  printf("enter fathers name\n");

  scanf("%s",father);

  printf("enter mothers name\n");

  scanf("%s",mother);

  printf(" your account number is 33354678\n");

  printf("enter your password of 6 characters:");

  scanf("%s",password1);

  balance=0;

  printf("\n\n\n\n\n\t\twelcome to your bank\n\n");

  menu:

  printf("1.check your details \n");

  printf("2.add money \n ");

  printf("3.withdraw money \n");

  printf("4.check savings\n");

  printf("5.change password\n");

  printf("6.logout and exit\n\n\n");

   

  printf("enter your choice\n");

  scanf("%d",&choice);

  switch(choice)

  {

    case 1:

    printf("\n\n\n\n\n\nyour name is %s \n",name);

    printf("your age is %d \n",age);

    printf("your fathers name is %s \n",father);

    printf("your mothers name is %s \n",mother);

    printf("your account number is 33354678 \n");

    printf("your balance is %d \n",balance);

    break;

     

     

   

    case 2:

    printf("\n\n\n\n\n\n\nhow much money do you want to add?");

    scanf("%d",&add);

    balance=balance+add;

    printf("added %d rupees succesfully.\n your total balance is %d\n\n\n",add,balance);

    break;

     

    case 3:

    printf("\n\n\n\n\n\n\nhow much money do you want to withdraw?");

    scanf("%d",&add);

    balance=balance-add;

    printf("withdrew %d rupees succesfully.\n your total balance is %d\n\n\n",add,balance);

    break;

     

    case 4:

    printf("your balance is %d \n",balance);

    break;

     

    case 5:

    printf("enter your current 6 character password \n");

    passw:

    scanf("%s",password2);

    value=strcmp(password1,password2); 

    if(value==0)

    {

      printf("enter your new password of 6 characters\n");

      scanf("%s",password1);

      printf("succesfully changed password\n");

       

    }

    else

    {

      printf("incorrect password please retry \n");

      goto passw;

    }

    break;

    default : printf("invalid input \n"); 

  }

  }

  else 

  {

  printf("invalid input");

  }

   

  printf("\n\n\n\n\n\tenter 1 for menu \n \tenter 0 to logout and exit\n");

  scanf("%d",&choice);

  if(choice==1)

  {

    goto menu;

  }

  else

  {

    return 0;

  }

  return 0;

}
