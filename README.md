# Matriz con nombre y horas trabajadas
recursos = [
    
    ["Ana","1", 8, 8, 9, 8, 8,],   
    ["Carlos","2", 10, 9, 8, 9, 10,],
    ["Luisa","3", 7, 8, 7, 8, 7,],
    ["Pedro","4", 8, 8, 8, 8, 8,]
]
# Función para calcular horas y clasificación
def calcular_horas(horas):
    total = sum(horas)

    if total > 40:
        clasificacion = "Sobretiempo"
    else:
        clasificacion = "Horario Estándar"
    return total, clasificacion

# Recorrer la matriz
for recurso in recursos:
    nombre = recurso[0]
    id = recurso[1]
    horas = recurso[2:]

    total, clasificacion = calcular_horas(horas)

    print("Recurso:", id)
    print("Nombre:", nombre)
    print("Total de horas:", total)
    print("Clasificación:", clasificacion)
    print("---------------------------")
