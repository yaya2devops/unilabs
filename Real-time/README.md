# [Laboratory 1](TP.pdf)
```C
#include <OSA.h>
#include <OSAcfg.h>

#pragma funcall main Thread1
#pragma funcall main Thread2
#pragma funcall main Thread3
#pragma funcall main Thread4


void InitTimer0(){
 T0CON = 0x88;
 TMR0H = 0xD1;
 TMR0L = 0x21;
 GIE_bit = 1;
 TMR0IE_bit = 1;
}


void Interrupt(){
 if (TMR0IF_bit){
 TMR0IF_bit = 0;
 TMR0H = 0xD1;
 TMR0L = 0x21;
 OS_Timer(); //Initialisation du timer pour le comptage des ticks
 }
}


void Thread1(void)
{   
 while(1)
 {
   PORTD.B1=1;
   OS_Delay(100)
 }
}


void Thread2(void)
{   
 while(1)
 {
   PORTD.B2=1;
   OS_Delay(100)
 }
}



void Thread3(void)
{   
 while(1)
 {
   PORTD.B3=1;
   OS_Delay(100)
 }
}


void Thread4(void)
{   
 while(1)
 {
   PORTD.B4=1;
   OS_Delay(100)
 }
}





void main() {
// Configuration du PORTD comme sortie
TRISD =0;

//mise à zéro du PORTD
PORTD =0;


 OS_Init(); //Initialisation de OS services
 OS_Task_Create(0,Thread1);
 OS_Task_Create(2,Thread2);
 OS_Task_Create(4,Thread3);
 OS_Task_Create(7,Thread4);
 InitTimer0()

 OS_Run(); // Appel à l’ordonnanceur
}


```
# [Laboratory 2](TP2.pdf)

``` C
#include <osa.h>
#include <OSAcfg.h>
#pragma funcall main Tache2
#pragma funcall main Tache1



void InitTimer0(){
 T0CON = 0x88;
 TMR0H = 0xD1;
 TMR0L = 0x21;
 GIE_bit = 1;
 TMR0IE_bit = 1;
}


void Interrupt(){
 if (TMR0IF_bit){
 TMR0IF_bit = 0;
 TMR0H = 0xD1;
 TMR0L = 0x21;
 OS_Timer(); 
 } 
}




void Tache1(void)
{
while(1) {
UART1_Write_Text("task1");
UART1_Write(13);
UART1_Write(10);

// changer l’état du bit1 du portd
PORTD.B1=1;

OS_Yield();
}
}



void Tache2(void)
{
while(1) {
UART1_Write_Text("task2");
UART1_Write(13);
UART1_Write(10);
// changer l’état du bit2 du portd


PORTD.B2=1;

OS_Yield();
}
}


void main() {


TRISD=0;
PORTD=0;


OSCCON = 0X70; // internal oscillator to 8MHz
ADCON1 = 0x0F; // Configurer AN pins
CMCON = 7; // désactiver le comparateur
UART1_Init(19200); // Init USART module


OS_Init();
OS_Task_Create(0,Tache2);
OS_Task_Create(0,Tache1);
InitTimer0();
OS_Run();

}

```

# [Laboratory 3 ](TP3.pd)

``` C
#include <osa.h>
#include <OSAcfg.h>
#pragma funcall main Tache2
#pragma funcall main Tache1
void InitTimer0(){
 T0CON = 0x88;
 TMR0H = 0xD1;
 TMR0L = 0x21;
 GIE_bit = 1;
 TMR0IE_bit = 1;
}
void Interrupt(){
 if (TMR0IF_bit){
 TMR0IF_bit = 0;
 TMR0H = 0xD1;
 TMR0L = 0x21;
 OS_Timer(); } // incrémentation du timer
}
 void Tache1(void)
{
 while(1) {
 OS_Bsem_Wait(BSEM_WRITE)
 UART1_Write_Text("task1");
 UART1_Write(13);
 UART1_Write_Text("Led allumé");
 UART1_Write(10);
 PORTD.B1=1;
 // changer l’état du bit1 du portd
 //OS_Yield();
 OS_Bsem_Set(BSEM_WRITE)
 }
}
 void Tache2(void)
{
 while(1) {
 OS_Bsem_Wait(BSEM_WRITE)
 UART1_Write_Text("task2");
 UART1_Write(13);
 UART1_Write_Text("Led allumé")  ;
 UART1_Write(10);
 PORTD.B2=1;
 // changer l’état du bit2 du portd               --
//OS_Yield();
OS_Bsem_Set(BSEM_WRITE)
 }
}
void main() {
 // configurer le portd en sortie
 //initialiser le portd avec zéro
 TRISD=0;
 PORTD=0;
 OSCCON = 0X70; // internal oscillator to 8MHz
 ADCON1 = 0x0F; // Configurer AN pins
//CMCON = 7; // désactiver le comparateur
 UART1_Init(19200); // Init USART module
 OS_Init();
 OS_Bsem_Set(BSEM_WRITE)
 OS_Task_Create(0,Tache2);
 OS_Task_Create(0,Tache1);
 InitTimer0();
 OS_Run();
  }

```


# Bonus, Exam
``` C
#include <osa.h>
#include <OSAcfg.h>
#pragma funcall tache1
#pragma funcall tache2

void tache1(void){
while(1){
PORTD.B0=1 ;
OS_Bsem_Wait(BSEM_WRITE);
Lcd_Cmd(_LCD_CLEAR);               // Clear display
Lcd_Cmd(_LCD_CURSOR_OFF);          // Cursor off
Lcd_Out(1,6,"led_allumee");
OS_Bsem_Set(BSEM_WRITE);                 // Write text in first row
}}

void tache2(void){
while(1){
PORTD.B0=0;
OS_Bsem_Wait(BSEM_WRITE);
Lcd_Cmd(_LCD_CLEAR);               // Clear display
Lcd_Cmd(_LCD_CURSOR_OFF);          // Cursor off
Lcd_Out(1,6,"led_eteint");
OS_Bsem_Set(BSEM_WRITE);               // Write text in first row
}}

sbit LCD_RS at RB4_bit;
sbit LCD_EN at RB5_bit;
sbit LCD_D4 at RB0_bit;
sbit LCD_D5 at RB1_bit;
sbit LCD_D6 at RB2_bit;
sbit LCD_D7 at RB3_bit;

sbit LCD_RS_Direction at TRISB4_bit;
sbit LCD_EN_Direction at TRISB5_bit;
sbit LCD_D4_Direction at TRISB0_bit;
sbit LCD_D5_Direction at TRISB1_bit;
sbit LCD_D6_Direction at TRISB2_bit;
sbit LCD_D7_Direction at TRISB3_bit;

void Config_LCD(){
OSCCON=0x70;
ADCON1=0x0F;
lcd_Init();}

void main() {
TRISD=0;
PORTD=0;
OS_Bsem_Set(BSEM_WRITE);
OS_Init();
OS_Task_Create(0,tache1);
OS_Task_Create(0,tache2);
OS_Run();
lcd_Cmd(_LCD_CLEAR);

}

```
