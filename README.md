Program in 8051 to generate a 200 µs delay using Timer 0 in Mode 1 and toggle Port 0.1
NAME: PREETHI S
REG NO: 212224060195
AIM

To write program in 8051 to generate a 200 µs delay using Timer 0 in Mode 1 and toggle Port 0.1

APPARATUS REQUIRED

Personal Computer

Keil µVision Software

PROGRAM:

     ORG 0000H

    MAIN:   MOV TMOD, #01H      
    AGAIN:  MOV TH0, #0FFH      
        MOV TL0, #038H    
        SETB TR0        
    WAIT:   JNB TF0, WAIT        
        CLR TR0         
        CLR TF0              
        CPL P0.1             
        SJMP AGAIN      

    END


OUTPUT:

<img width="1280" height="720" alt="Untitled design (1)" src="https://github.com/user-attachments/assets/133a3a60-ffa7-4b0a-9e68-f7e6fe612f58" />



RESULT:

Thus the 200 µs delay using Timer 0 in Mode 1 and toggle Port 0.1 is obtained
