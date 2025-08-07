//Mi pseudocódigo//

Proceso cajero_automatico_ka
    Definir monto Como Entero
    Definir saldo Como Entero
	
    saldo <- 550
	
    Escribir "Ingrese cuánto desea retirar:"
    Leer monto
	
    Si monto > saldo Entonces
        Escribir "Fondos insuficientes"
    Sino
        saldo <- saldo - monto
        Escribir "Retire su dinero"
        Escribir "Saldo restante: ", saldo
    FinSi
FinProceso
