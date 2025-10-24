Program in 8051 to generate a 200 µs delay using Timer 0 in Mode 1 and toggle Port 0.1

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

<img width="1222" height="712" alt="image" src="https://github.com/user-attachments/assets/aa0bb1a6-8041-4b11-bb07-67d8991f0e00" />


RESULT:

Thus the 200 µs delay using Timer 0 in Mode 1 and toggle Port 0.1 is obtained
