#Aun falta solucionar algunas fallas con respecto al complemento, no muestra lo que deberia mostrar, tambien podria seguir validando en el meno de opciones para que solo que puedan ingresar los numeros disponibles en las opciones.
def es_natural(numero):
    try:
        int(numero)
        if int(numero) > 0:
            return True
        else:
            return False
    except ValueError:
        return False

while True:
    try:
        a = int(input("Ingrese el inicio de su conjunto: "))
        if es_natural(a):
            break
        else:
            print("El número debe ser un número natural.")
    except ValueError:
        print("El número debe ser un número natural.")

while True:
    try:
        b = int(input("Ingrese el final de su conjunto: "))
        if es_natural(b):
            if b < a:
                print("El número para el final de su conjunto debe ser mayor al inicial.")
            else:
                break
        else:
            print("El número debe ser un número natural.")
    except ValueError:
        print("El número debe ser un número natural.")

conjunto = set()
for i in range(a, b):
    resultado = 2 * i ** 2 - 1
    conjunto.add(resultado)
print(f"El conjunto universal es: {conjunto}\n")
aconjunto = set (input('Ingrese los valores para su conjunto "a" separando cada elemento con una coma: ').split(","))
bconjunto = set (input('Ingrese los valores para su conjunto "b" separando cada elemento con una coma: ').split(","))
print (f'su conjunto "a" es:{aconjunto}')
print (f'su conjunto "b" es:{bconjunto}\n')
opcion = int(
    input(
        "\n      MENU DE OPCIONES\n\t"     
            +"1. Mostrar la Union de los conjuntos\n"
            +"2. Mostrar la intercepcion de los conjuntos\n"
            +"3. Mostrar la igualdad de los conjuntos\n"
            +"4. Mostrar la diferencia de los conjuntos A-B\n"
            +"5. Mostrar la diferencia de los conjuntos B-A\n"
            +"6. Mostrar el complemento de A\n" 
            +"7. Mostrar el complemento de B\n" 
            +"8. Salir\n\n\t"
        + "Por favor ingrese una opcion:  ",
        
    )
)
while opcion != 8:
    if opcion == 1:
        print(f"\nla union de los conjuntos es: {aconjunto.union(bconjunto)}")
    elif opcion == 2:
        print(f"\n la intercepcion de los conjuntos es: {aconjunto.intersection(bconjunto)}")
    elif opcion == 3:
        print(f"\n la igualdad de los conjuntos es: {aconjunto == bconjunto}")
    elif opcion == 4:
        print(f"\n la diferencia de los conjuntos A-B es:{aconjunto.difference(bconjunto)}")
    elif opcion == 5:
        print(f"\n la diferencia de los conjuntos A-B es: {bconjunto.difference(aconjunto)}")
    elif opcion==6:
        print(f"\n el complemento de A es:  {conjunto.difference(aconjunto)}")
    elif opcion==7:
        print (f"\n el complemento del conjunto B es: {conjunto.difference(bconjunto)}")
    elif opcion==8:
        break
    else:
        print("\n Por favor ingrese una opcion valida")
    opcion = int(
        input(
            "\n   MENU DE OPCIONES\n\t"
            
            + "1. Mostrar la Union de los conjuntos\n"
            +"2. Mostrar la intercepcion de los conjuntos\n"
            +"3. Mostrar la igualdad de los conjuntos\n"
            + "4. mostrar la diferencia de los conjuntos A-B\n"
            +"5. mostrar la diferencia de los conjuntos B-A\n"
            +"6. mostrar el complemento de A\n"
            +"7. mostrar el complemento de B\n" 
            + "8. Salir\n\n\t"
            + "Por favor ingrese una opcion:"
        )
    )
