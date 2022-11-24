## Funciones de manejo de cadenas para caracteres

### Actividad 1

Crear una tabla con 20 nombres y al accionar un botón se va generar una lista de los sus ultimos 2 caracteres.

**Codigo en VBA**

```
Sub prueba()
    For m = 2 To 21
        bres = nombres.Cells(m, 1)
        iden = Int(Len(bres)) - 1
        nombres.Cells(m, 2) = Mid(bres, iden, 2)
    Next m
End Sub
```

### Actividad 2

Crear una tabla con 20 nombres con sus respectivas ciudades y municipios. Al accionar un botón se va generar un lista de codigo creado con los siguentes caracteres:

1. Los dos primeros caracteres del año.
2. Los dos ultimos caracteres del municipio.
3. Los dos primeros caracteres del nombre.

**Codigo en VBA**

```
Sub referencia()
    For m = 2 To 21
        nombres = codigo.Cells(m, 1)
        anho = codigo.Cells(m, 2)
        municipio = codigo.Cells(m, 3)
        idenNom = 1
        idenAnho = 1
        idenMuni = Len(municipio) - 1
        codigo.Cells(m, 4) = Mid(anho, idenAnho, 2) & Mid(municipio, idenMuni, 2) & Mid(nombres, idenNom, 2)
    Next m
End Sub
```
