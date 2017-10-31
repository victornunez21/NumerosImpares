# NumerosImpares

import asyncio
import random

def impares():
    yield "Impares"

def generar_secuencia():
    numero = 1
    while True:
        yield numero
        numero = numero + 2

if __name__ == "__main__":
    generador = impares()
    print(next(generador))

    numeros = generar_secuencia()
    for n in numeros:
        print(n)
        if n > 50:
            break
