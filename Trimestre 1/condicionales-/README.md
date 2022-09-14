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
 
 
 sub sumar
 
 
   a = inputbox ("por favor escribe un numero")
   
   b = inputbox (" por favor escribe otro numero")
   
   C = int (a) + int (b)
   
     msgbox " el resultado es: " & c
     
 end sub   
 
 
 -------------------------------------------------
 
 sub sumar 
 
 a = int (inputbox (" por favor escribe un numero")
 
 b = inputbox (" por favor escribe otro numero")
 
   c= a + int (b)
  
  msgbox "el resultado es: " & c
  
  end sub
   
   
Sub formulario()
    ID = True
    fila = 1
    
    cedula = Int(InputBox("Digite el número de cédula: "))
    While ID
        If cedula = lista.Cells(fila, 1) Then
            nombre = lista.Cells(fila, 2)
            
            ID = False
            MsgBox "su nombre es: " & nombre
        End If
    Wend
    
End Sub

 
