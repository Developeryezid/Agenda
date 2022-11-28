# Apuntes en general
   + introduccion al algoritmo
   + diagramas de flujo
   + practicas diarias de programacion
   + analizar procesos de algoritmos




# ejemplos de algoritmos
 + condicionales dobles
 + algoritmos de datos y registros
 + Algoritmos de impuestos
 + algoritmos de estructuras de datos

 
 ----------------------------------------------
 ```
 
 sub sumar
 
 
   a = inputbox ("por favor escribe un numero")
   
   b = inputbox (" por favor escribe otro numero")
   
   C = int (a) + int (b)
   
     msgbox " el resultado es: " & c
     
 end sub   
 ```
 
 -------------------------------------------------
 ```
 sub sumar 
 
 a = int (inputbox (" por favor escribe un numero")
 
 b = inputbox (" por favor escribe otro numero")
 
   c= a + int (b)
  
  msgbox "el resultado es: " & c
  
  end sub
 ```
   ## VBA notas de estudiantes 24/08/2022
   ```
   Sub aprobo_estudiante()
   nom = InputBox("Escriba el nombre del alumno")
   par = Int(InputBox ("Escriba la nota del parcial"))
   exa = Int(InputBox ("Escriba nota del examen final"))
   pra = Int(InputBox ("Escriba promedio de practicas"))
   nota = ((exa * 2) + par + pra) / 3
   If nota = 6 Then
      MsgBox ("El nombre del alumno es: " & nom)
      MsgBox ("El alumno con nombre: " & nom & " aprobo con esta nota: " & nota)
   Else
      MsgBox ("No aprobo")
   End If 
End Sub
```
## VBA impuesto empresa usando if else
```
Sub impuesto_a_pagar_empresa()
    ingreso = InputBox("Isertar los ingresos anuales de la empresa")
        If ingreso >= 1001 And ingreso <= 10000 Then
            impuesto = ((ingreso * 5) / 100)
            MsgBox ("el  impuesto es: " & impuesto)
        Else
            If ingreso >= 10001 And ingreso <= 100000 Then
                impuesto = ((ingreso * 10) / 100)
                MsgBox ("el impuesto es: " & impuesto)
            End If
            If ingreso >= 100001 And ingreso <= 1000000 Then
                impuesto = ((ingreso * 15) / 100)
                MsgBox ("el impuesto es: " & impueto)
            End If
            If ingreso >= 1000001 And ingreso <= 10000000 Then
                impuesto = ((ingreso * 20) / 100)
                MsgBox ("el impuesto es: " & impuesto)
            End If
            If ingreso >= 10000001 Then
                impuesto = ((ingreso * 25) / 100)
                MsgBox ("el impuesto es: " & impuesto)
            End If
            If ingreso >= 1 And ingreso <= 1000 Then
                MsgBox ("el impuesto es: " & impuesto)
            End If
            If ingreso <= 0 Then
                MsgBox ("El impuesto es de: " & 0)
            End If
        End If
End Sub
```
## VBA Programa usando select case
```
Sub sena()
    ingreso = Int(InputBox("Escriba los ingresos anuales de la empresa"))
        Select Case ingreso
            Case 0 To 1000
                MsgBox ("El impuesto a pagar es: " & ingreso)
                Case 1001 To 10000
                    impuesto = ((ingreso * 5) / 100)
                    MsgBox ("El impuesto a pagar es: " & impuesto)
                Case 10001 To 100000
                    impuesto = ((ingreso * 10) / 100)
                    MsgBox ("El impuesto a pagar es: " & impuesto)
                Case 100001 To 1000000
                    impuesto = ((ingreso * 15) / 100)
                    MsgBox ("El impuesto a pagar es: " & impuesto)
                Case 1000001 To 10000000
                    impuesto = ((ingreso * 20) / 100)
                    MsgBox ("El impuesto a pagar es: " & impuesto)
                Case Else
                    impuesto = ((ingreso * 25) / 100)
                    MsgBox ("El impuesto a pagar es: " & impuesto)
        End Select
End Sub
```
## VBA Ciclo for
```
Sub prueba()
    For n = 1 To 15
        nom = InputBox("Digite su nombre")
        fila = nombres.Cells(2, 6)
        nombres.Cells(fila, 2) = nom
        nombres.Cells(2, 6) = fila + 1
    Next n
    MsgBox ("Nombres registrados")
End Sub
```
## VBA Funciones de cadenas de caracteres
```
Sub inicio()
    For a = 2 To 21
    nom = Hoja1.Cells(a, 1)
    ultimo = Len(nom) - 1
    Hoja1.Cells(a, 2) = Mid(nom, ultimo, 2)

    Next a
End Sub
```
## VBA Base de datos con while - if

```
Sub datos()
   y = 2
   cedula = Int(InputBox("digite cedula: "))
   sw = True
   While sw
      If cedula = Hoja1.Cells(y, 1) Then
         nombre = Hoja1.Cells(y, 2)
         sw = False
         MsgBox "su nombre es: " & nombre
      End If         
      If y = 20 Then
         MsgBox ("no valido")
         sw = False
      End If     
          y = y + 1        
   Wend
      
End Sub
```
## Ciclo For student
```
Sub estudiante()
    cont = 0
    acum = 0
    masde = 0
    cant = Int(InputBox("Ingrese la cantidad de estudiantes que aportaron de los 7500"))
        For i = 1 To cant
            aporto = Int(InputBox("Ingrese la cantidad que aporto el estudiante"))
            cont = cont + 1
            acum = acum + aporto
            noapor = 7500 - cant
            prom = acum / cont
                If aporto > 10000 Then
                    masde = masde + 1
                End If
        Next i
    MsgBox ("Cantidad de estudintes que aporto: " & cant)
    MsgBox ("total recaudado: " & acum)
    MsgBox ("El numero de estudiantes que no aporto: " & noapor)
    MsgBox ("Valor recaudo promedio: " & prom)
    MsgBox ("Los estudiantes que aportaron mas de 10.000 fueron: " & masde)
End Sub
```
## VBA Base de datos Recaudo con while

~~~
Sub presupuesto()
    abono = 0
    aporto = 0
    noaporto = 0
    masde = 0
    tot = 0
    While abono < 3000000
        aporto = Int(InputBox("cuanto dinero va aportar"))
        If aporto < 0 Then
            MsgBox ("no es valido")
        Else
            If aporto = 0 Then
                MsgBox ("el estudiante no aporto")
                noaporto = noaporto + 1
            End If
            If aporto > 0 Then
                abono = aporto + abono
                tot = tot + 1
            End If
            If aporto > 10000 Then
                tot = tot + 1
                masde = masde + 1
            End If
        End If     
    Wend
    promedio = abono / tot
    MsgBox ("el total aportado fue:" & "$" & abono)
    MsgBox ("estudiantes que aportaron :" & tot)
    MsgBox ("estudiantes que aportaron mas de $10.000: " & masde)
    MsgBox ("estudiantes que no aportaron: " & noaporto)
    MsgBox ("promedio de estudiantes que aportaron es de: " & "$" & promedio)
End Sub
~~~
