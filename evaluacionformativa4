turistas = {
"001": ["John Doe", "Estados Unidos", "12-01-2024"],
"002": ["Emily Smith", "Estados Unidos", "23-03-2024"],
"012": ["Julian Martinez", "Argentina", "19-09-2023"],
"014": ["Agustin Morales", "Argentina", "28-03-2024"],
"005": ["Carlos Garcia", "Mexico", "10-05-2024"],
"006": ["Maria Lopez", "Mexico", "08-12-2023"],
"007": ["Joao Silva", "Brasil", "20-06-2024"],
"003": ["Michael Brown", "Estados Unidos", "05-07-2023"],
"004": ["Jessica Davis", "Estados Unidos", "15-11-2024"],
"008": ["Ana Santos", "Brasil", "03-10-2023"],
"010": ["Martin Fernandez", "Argentina", "13-02-2023"],
"011": ["Sofia Gomez", "Argentina", "07-04-2024"],
}

def ingresar_turista():
   nombre = input("Ingrese el nombre del turista: ")
   pais = input("Ingrese el país del turista: ")
   fecha = input("Ingrese la fecha de ingreso (dd-mm-aaaa): ")

   nuevo_id = str(max([int(k) for k in 
turistas.keys()]) + 1).zfill(3)
   turistas[nuevo_id] = [nombre, pais, fecha]
   print(f"Turista {nombre} agregado con ID {nuevo_id} a {pais}.\n")

def mostrar_turistas():
   pais = input("Ingrese el país para buscar turistas: ")
   encontrados = False
   print(f"Turistas en {pais}:")
   for id, datos in turistas.items():
      if datos[1].lower() == pais.lower():
         print(f"- {datos[0]} (ID: {id}, Fecha: {datos[2]})")
         encontrados = True
   if not encontrados:
      print("No hay turistas registrados en ese país.\n")

def eliminar_turista():
   id_turista = input("Ingrese el ID del turista que desea eliminar: ")
   if id_turista in turistas:
      nombre = turistas[id_turista][0]
      del turistas[id_turista]
      print(f"Turista {nombre} eliminado con éxito.\n")
   else:
      print("No se encontró un turista con ese ID.\n")

def menu():
   while True:
      print("\nMENU PRINCIPAL")
      print("1. Ingresar turista")
      print("2. Mostrar turistas por país")
      print("3. Eliminar turista")
      print("4. Salir")
      opcion = input("Ingrese opción: ")

      if opcion == "1":
         ingresar_turista()
      elif opcion == "2":
         mostrar_turistas()
      elif opcion == "3":
         eliminar_turista()
      elif opcion == "4":
         print("Programa terminado.")
         break
      else:
         print("Opción no válida. Intente nuevamente.")
menu()
