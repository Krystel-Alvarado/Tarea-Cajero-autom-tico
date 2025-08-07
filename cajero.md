## Mi Pseudocódigo

```pseudocodigo

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

<!-- Codigo Mermaid -->
---
config:
  theme: redux-dark
---
flowchart TD
    A(["Start"]) --> C["Definir monto como entero"]
    C --> n1["Definir saldo como entero"]
    n1 --> n2["saldo &lt;- 550"]
    n2 --> paraId[/"Ingrese cuánto desea retirar"/]
    paraId --> n3[/"monto"/]
    n3 --> decisionId{"¿El monto es mayor que el saldo?"}
    decisionId -- No --> n4["Restar el monto al saldo"]
    decisionId -- Si --> n5[/"Fondos insuficientes"/]
    n4 --> n6[/"Retire su dinero"/]
    n6 --> n7[/"Saldo restante"/]
    n7 --> n8(["End"])
    n5 --> n8
    n1@{ shape: rect}
    n2@{ shape: rect}
    n4@{ shape: rect}
