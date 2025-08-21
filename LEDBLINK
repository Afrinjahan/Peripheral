ORG 00H 			; Assembly Starts from 0000H.
; Main Program
START:	MOV P1, #0XFF		; Move 11111111 to PORT1.
		CALL WAIT 	; Call WAIT 
		MOV A, P1 	; Move P1 value to ACC 
		CPL A 		; Complement ACC
		MOV P1, A 	; Move ACC value to P1
		CALL WAIT 	; Call WAIT
		SJMP START 	; Jump to START
WAIT:		MOV R2, #10 	; Load Register R2 with 10 (0x0A)
WAIT1:	MOV R3, #200 		; Load Register R3 with 10 (0xC8)
WAIT2:	MOV R4, #200 		; Load Register R4 with 10 (0xC8)
		DJNZ R4, $ 	; Decrement R4 till it is 0. Stay there if not 0.
		DJNZ R3, WAIT2 	; Decrement R3 till it is 0. Jump to WAIT2 if not 0.
		DJNZ R2, WAIT1 	; Decrement R2 till it is 0. Jump to WAIT1 if not 0.
		RET 		; Retu rn to Main Program
END  				; End Assembly
