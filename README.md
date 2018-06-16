# ICC-SmartClass
def menu():

    print("=============================")
    print("==     1. Crear            ==")
    print("==     2. Buscar           ==")
    print("==     3. Editar           ==")
    print("==     4. Eliminar         ==")
    print("==     5. Mensaje          ==")
    print("==     6. Ver historial    ==")
    print("==     7. Salir            ==")
    print("=============================")
    print("Seleccione una opción del 1 al 6: ")
    opcion=int(input())

    return opcion



def crear(lista):

    #Agregar un algoritmo que permita crear una lista solicitando los siguientes datos:
    # 1. Nombres
    # 2. Apellido Paterno
    # 3. Edad
    # 4. Teléfono
    # 5. ID_Registro --> Este código se va a generar automáticamente de manera correlativa y será el identificador para manipular el registro en la lista.
    lista_modificada = lista
    return lista_modificada


def buscar(lista_donde_se_buscara_el_valor, valor_a_buscar):

    #Agregar un algoritmo que permita buscar los registros en la lista_donde_se_buscara_el_valor que cumplan con el valor_a_buscar.
    #Deberá mostrar los registros que coincidan.

    print("Funcionalidad de buscar")

    return



def editar(lista, ID_Registro):

    #Agregar un algoritmo que permita modificar el registro especifico de una lista
    #Los datos que se podrán modificar son:
    # 1. Nombres
    # 2. Apellido Paterno
    # 3. Edad
    # 4. Teléfono

    lista_modificada = lista

    print("Funcionalidad de editar")

    return lista_modificada



def eliminar(lista, ID_Registro):

    lista_modificada = lista

    print("Funcionalidad de eliminar")

    return lista_modificada



def mensaje(emisor, receptor, mensaje, lista_de_mensajes):

    #Agregar un algoritmo que permita agregar mensajes a una lista_de_mensajes con la siguiente estructura:
    # ID_Registro_del_emisor
    # ID_Registro_del_receptor
    # Contenido del Mensaje
    # Fecha y hora del mensaje --> Este valor debe generarse automÃ¡ticamente

    print("Funcionalidad de mensaje")

    return lista_de_mensajes



def ver_historial(lista_de_mensaje):

    #Agregar un algoritmo para mostrar el historial de los mensajes en orden cronológico con la siguient estructura:
    # Nombres y apellido del emisor |  Nombres y apellido del receptor  |  Fecha y hora del mensaje  |  Contenido del Mensaje
    # El historial debe mostrarse ordenado por Emisor , Receptor y Fecha y hora del mensaje

    print("Funcionalidad de ver historial")


    return



lista_de_alumnos = []
lista_de_mensajes = []

opcion = 0
while not(opcion == 7):

    opcion = menu()

    if opcion == 1:
        print("Seleccionó la opción Crear")
        lista_de_alumnos = crear(lista_de_alumnos)

    elif opcion == 2:
        print("Seleccionó la opción Buscar")
        valor_a_buscar = input("Ingrese el valor a buscar: ")
        buscar(lista_de_alumnos, valor_a_buscar)

    elif opcion == 3:
        print("Seleccionó la opción Editar")
        codigo_de_alumno = int(input("Ingrese el ID de registro de alumno a MODIFICAR: "))
        lista_de_alumnos = editar(lista_de_alumnos, codigo_de_alumno)

    elif opcion == 4:
        print("Seleccionó la opción Eliminar")
        codigo_de_alumno = int(input("Ingrese el ID de registro de alumnoa ELIMINAR: "))
        lista_de_alumnos = eliminar(lista_de_alumnos, codigo_de_alumno)

    elif opcion == 5:
        print("Seleccionó la opción Mensaje")
        ID_registro_EMISOR   = int(input("Ingrese el ID de registro del EMISOR: "))
        ID_registro_RECEPTOR = int(input("Ingrese el ID de registro del RECEPTOR: "))
        contenido_del_mensaje = input("Ingrese el mensaje: ")
        lista_de_mensajes = mensaje(ID_registro_EMISOR, ID_registro_RECEPTOR, contenido_del_mensaje, lista_de_mensajes)

    elif opcion == 6:
        print("Seleccionó la opción Ver Historial")
        ver_historial(lista_de_mensajes)

    elif opcion == 7:
        print("Finalizó el programa")
