# SudoYourNano

#include<stdio.h>
#include<wiringPi.h>

int ShowMainMenu();
int ShowFATMenu();
int ShowFATSubMenu();
int ShowFATModuleMenu();
int ShowFATModuleSubMenu();
 
void PrintHotswap();
void PrintACS();
void PrintRack();
void PrintDoor();
void PrintLIFT();
void PrintADS();
void PrintLEDTesting();

void PrintWakeUp();
void PrintFAT2();
void PrintFAT3();
 
int main(void)
{
   int 
      nChoice = 0;
 
   do
   {
      nChoice = ShowMainMenu ();
      switch (nChoice)
      {
         case 1:
         {
            ShowFATMenu ();            
         }
         break;
 
         case 2: 
         {
            ShowFATModuleMenu ();
         }
         break;
 
         case 3: 
         {
            printf ("*********User ended the session*********\n\n");
         }
         break;
      }
   }
   while (nChoice != 3);
   return 0;
} 
 
/* ************************************************** ******************* */
 
int ShowMainMenu ()
{
   int 
      nSelected = 0;
 
   do
   {
      printf ("*********MENU*********\n");

      printf ("(1) FAT\n(2) FAT Module\n(3) Quit\n\n");
 
      printf ("Enter a number of your choice > ");
      scanf ("%d", &nSelected);
      printf("\n");
 
      if (( nSelected < 1 ) || ( nSelected > 3))
      {
         printf("You have entered an invalid choice. Please try again\n\n\n");
      }
   }
   while (( nSelected < 1) || ( nSelected > 3));
 
   return nSelected;
}
 
/* ************************************************** ************************** */
int ShowFATMenu ()
{   
   int 
      nChoice = 0;   
   do
   {
      nChoice = ShowFATSubMenu();
      switch (nChoice)
      {
 
         case 1:
         {
            PrintWakeUp ();
         }
         break;
 
         case 2: 
         {
            PrintFAT2 ();
         }
         break;
 
         case 3: 
         {
            PrintFAT3 ();
         }
         break;
 
         case 4: 
         {
            printf (">>>>>>>>>Back to Menu<<<<<<<<<\n\n");
         }
         break;
      }
   }
   while (nChoice != 4);
 
   return nChoice;
}
 
/* ************************************************** ******************* */
int ShowFATSubMenu() 
{
   int 
      nSelected = 0;
 
   do
   {
 
      printf ("(1) WakeUp\n(2) FAT2\n(3) FAT3\n(4) Quit\n\n");
 
      printf ("Enter a number that corresponds to your choice > ");
      scanf ("%d", &nSelected);
      printf("\n");
 
      if (( nSelected < 1 ) || ( nSelected > 4))
      {
         printf("You have entered an invalid choice. Please try again\n\n\n");
      }
   }
   while (( nSelected < 1) || ( nSelected > 4));
 
   return nSelected;
}
 
/* ************************************************** ************************** */
int ShowFATModuleMenu ()
{
   int 
      nChoice = 0;
 
   do
   {
      nChoice = ShowFATModuleSubMenu ();
      switch (nChoice)
      {
         case 1:
         { 
            PrintHotswap ();
         }
         break;
 
         case 2:
         { 
            PrintACS ();
         }
         break;
 
         case 3:          
         {             
            PrintRack ();
         }
         break;

         case 4:          
         {             
            PrintDoor ();
         }
         break;

         case 5:          
         {             
            PrintLIFT ();
         }
         break;

         case 6:          
         {             
            PrintADS ();
         }
         break;
 
         case 7:
         { 
            PrintLEDTesting ();       
         }
         break;

         case 8:
         { 
            printf (">>>>>>>>>Back to Menu<<<<<<<<<\n\n");
         }
         break;
      }
   }
   while (nChoice != 8);
 
   return nChoice;
}
 
/* ************************************************** ******************* */
int ShowFATModuleSubMenu ()
{
   int 
      nSelected = 0;
 
   do
   {
 
      printf ("(1) Hotswap\n(2) ACS\n(3) Rack\n(4) Door\n(5) LIFT\n(6) ADS\n(7) LEDTesting\n(8) Quit\n\n");
 
      printf ("Enter a number that corresponds to your choice > ");
      scanf ("%d", &nSelected);
      printf("\n");
 
      if (( nSelected < 1 ) || ( nSelected > 8))
      {
         printf("You have entered an invalid choice. Please try again\n\n\n");
      }
   }
   while (( nSelected < 1) || ( nSelected > 8));
 
   return nSelected;
}
 
/* ************************************************** ************************** */
void PrintWakeUp ()
{
   printf("Run WakeUp Program\n\n");
}
 
/* ************************************************** ************************** */
void PrintFAT2 ()
{
   printf("Run FAT2 Program\n\n");
}
 
/* ************************************************** ************************** */
void PrintFAT3 ()
{
   printf("Run FAT3 Program\n\n");
}
 
/* ************************************************** ************************** */
void PrintHotswap ()
{
   printf("Run Hotswap Program\n\n");
}
 
/* ************************************************** ************************** */
void PrintACS ()
{
   printf("Run ACS Program\n\n");
}
/* ************************************************** ************************** */
 
void PrintRack ()
{
   printf("Run Rack Program\n\n");
}
/* ************************************************** ************************** */
void PrintDoor ()
{
   printf("Run Door Program\n\n");
}
 
/* ************************************************** ************************** */
void PrintLIFT ()
{
   printf("Run LIFT Program\n\n");
}
/* ************************************************** ************************** */
 
void PrintADS ()
{
   printf("Run ADS Program\n\n");
}
/* ************************************************** ************************** */
void PrintLEDTesting ()
{

}
