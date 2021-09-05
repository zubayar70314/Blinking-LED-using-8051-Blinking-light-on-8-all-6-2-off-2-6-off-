# Blinking-LED-using-8051-Blinking-light-on-8-all-6-2-off-2-6-off-
Blinking LED using 8051 Blinking 8 LED using 8051 This is the first project regarding 8051 and of course one of the simplest, blinking LED using 8051.







;sakif
;led blinking asm file
;8,6,2 position light on

ORG 0000H
REPEAT: CLR P1.0
	CLR P1.1
	CLR P1.2
	CLR P1.3
	CLR P1.4
	CLR P1.5
	CLR P1.6
	CLR P1.7
LCALL DELAY

SETB 	P1.0
	CLR P1.1
	CLR P1.2
	CLR P1.3
	CLR P1.4
	CLR P1.5
	CLR P1.6
   SETB P1.7   
LCALL DELAY

SETB P1.0
SETB P1.1
SETB P1.2
	
	CLR P1.3
	CLR P1.4
	CLR P1.5
 SETB P1.6  
 SETB P1.7  
LCALL DELAY

        SETB 	P1.0
        SETB 	P1.1
        SETB	P1.2
CLR	P1.3
CLR 	P1.4
        SETB    P1.5   
        SETB    P1.6	
        SETB    P1.7	
LCALL DELAY

CLR P1.0
CLR P1.1
CLR P1.2
CLR P1.3
CLR P1.4
CLR P1.5
CLR P1.6
CLR P1.7
LCALL DELAY
SJMP REPEAT
ORG 100H
DELAY:   MOV R1, #4D
WAIT1:   MOV R0, #50D
WAIT:    DJNZ R0, WAIT
DJNZ R1, WAIT1
RET
END
