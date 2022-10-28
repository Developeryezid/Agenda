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
## DART - Estructura de Objetos

```
void main() {
  Operacion operacion = new Operacion();
  operacion.num1 = 2.0;
  operacion.num2 = 4.0;
  print ('El resultado de la suma es: ${operacion.sumar()}');
  operacion.restar();
  print ('El resultado de la suma es: ${operacion.multiplicar()}');
}

class Operacion{
  double? num1;
  double? num2;
  
  double sumar(){
    double s = num1! + num2!;
    return s;
  }
  void restar(){
    double r = num1! - num2!;
    print ('La resta es $r');
  }
  double multiplicar(){
    double m = num1! * num2!;
    return m;
  }
}
```
## Metodos y constructor Dart
```
void main(){
  
  Person person =  Person(nomb: "Git", sex:"Hombre");
  
  person. apellido = "Copilot";
  person. edad = 24;
  print("El nombre es: ${person.nombre}");
  print("El apellido es: ${person.apellido}");
  print("El sexo es: ${person.sexo}");
  print("El nombre completo es: ${person.nombrecompleto()}");
  print("La edad es: ${person.edad}");
  person.edadmas(20);
  }
  
  class Person{
    
    String? nombre, sexo, apellido;
    int? edad;
    String? nombrecompleto(){
      
    String? nombrecompleto = nombre! + apellido!;
    return nombrecompleto;
    }
void edadmas(int num1){
    
    int a = edad! + num1;
      print("La edad sumada es: $a");
  }
    Person({String? nomb, String? sex}){
    nombre = nomb;
    sexo = sex;     
  }  
 }
```
## Jerarquia de Herencia Dart
```
void main() {
  String titulo = 'Clasificación de animales';
  Conejo conejo = new Conejo();
  conejo.nombre = 'Conejo';
  conejo.nombreCientifico = 'Oryctolagus cuniculus';
  conejo.tipo = 'Herbivoro';
  conejo.alimento = <String>['zanahorias', 'heno', 'hojas vegetales', 'pellets'];
  conejo.edadPromedio = 9;
  Leon leon = new Leon();
  leon.nombre = 'Leon';
  leon.nombreCientifico = ('Panthera leo');
  leon.alimento = <String>['ñúes','impalas', 'antílopes', 'cebras', 'jirafas', 'búfalos', 'carroña'];
  leon.edadPromedio = 15;
  
  Hiena hiena = new Hiena();
  hiena.nombre = 'Hiena';
  hiena.nombreCientifico = 'Hyaenidae';
  hiena.alimento = <String> ['aves', 'lagartos', 'serpientes']; 
  hiena.edadPromedio = 12;
  
  Hombre hombre = new Hombre();
  hombre.nombre = "Humano";
  hombre.nombreCientifico = 'Homo sapiens';
  hombre.alimento = <String> ['carnes', 'verduras', 'frutas'];
  hombre.edadPromedio = 77;
  
  print("""
  $titulo
  Los animales están dividido en 3 clasificaciones: Herviboro, carnivoro y omnivoro.
  Ejemplos:
    Animal 1:
        ${conejo.nombre}
          Nombre cientifico: ${conejo.nombreCientifico}
          Es clasificado como ${conejo.tipo}.
          Se alimenta de ${conejo.alimento}.
          Su edad de vida es de ${conejo.edadPromedio} años.
    Animal 2:
        ${leon.nombre}
          Nombre cientifico: ${leon.nombreCientifico}
          Es clasificado como ${leon.tipo}.
          Se alimenta de ${leon.alimento}.
          Su edad de vida es de ${leon.edadPromedio} años.
    Animal 3:
        ${hiena.nombre}
          Nombre cientifico: ${hiena.nombreCientifico}
          Es clasificado como ${hiena.tipo}.
          Se alimenta de ${hiena.alimento}.
          Su edad de vida es de ${hiena.edadPromedio} años.
    Animal 4:
        ${hombre.nombre}
          Nombre cientifico: ${hombre.nombreCientifico}
          Es clasificado como ${hombre.tipo}.
          Se alimenta de ${hombre.alimento}.
          Su edad de vida es de ${hombre.edadPromedio} años.
  """);
}
class Animal {
  String? nombre, nombreCientifico;
  List? alimento;
  int? edadPromedio;
}
class Herbivoro extends Animal {
  String tipo = 'herbivoro';
}
class Conejo extends Herbivoro {}
class Carnivoro extends Animal {
  String tipo = 'carnivoro';
}
class Leon extends Carnivoro {}
class Hiena extends Carnivoro {}
class Omnivoro extends Animal {
  String tipo = 'omnivoro';
}
class Hombre extends Omnivoro {}
```
## Herencia empresa Dart
```
void main(){ 
  List listaPais = ['Canada','Noruega','Colombia','Brazil'];
  List listaCodigo = [45342, 093434, 199634, 202345, 230445];
  List listaOficina = ['IBM', 'Overflow', 'Pragmat', 'Baire'];
  for (int i = 0; i < 3; i++){
    Empresa empresa = Empresa(pais:listaPais[i],oficina:listaOficina[i],codigo:listaCodigo[i]);
    print ('El codigo de la empresa es ${empresa.generarCodigo()}');
    
    empresa.cantCaracteres();
  }
  
}
class Empresa{ 
  String? pais, oficina; 
  int? codigo;
  
  Empresa ({this.pais, this.oficina, this.codigo});
  String generarCodigo(){
    int caractoficina = oficina!.length - 3;
    return pais!.substring(0,3) + codigo.toString().substring(0,3) + oficina!.substring(caractoficina, oficina!.length);
  }
  void cantCaracteres(){
    
    int cantTotal = pais!.length + oficina!.length + codigo!.toString().length;
    print ("""
  
    La cantidad de caracteres de ciudad: ${pais!.length}
    La cantidad de caracteres de oficina: ${oficina!.length}
    La cantidad de caracteres de numero: ${codigo!.toString().length}
    Cantidad total: $cantTotal
    """);
  }
}
```
## Clase abstract y Estatic Dart
```
void main(){
  
  Gato gato = Gato();
  gato.emitirsonido();
  
  Vaca vaca = Vaca();
  vaca.emitirsonido();
  
  Perro perro = Perro();
  perro.emitirsonido();
  perro.nombre = 'Hela';
  print (perro.nombre);
  Carnivoro.imc(35, 10);    
}

abstract class Animal {
  void emitirsonido (); 
}

class Gato implements Animal{
 @override
  void emitirsonido(){
    print ('Gato miauu');
  } 
} 
class Vaca implements Animal{
 @override
  void emitirsonido(){
    print ('Vaca Muuu');
  }
}

class Carnivoro {
  String? nombre;
  
  static void imc(int altura, int peso){
    int calcularimc = peso * altura;
  print ('imc es igual a $calcularimc');
  }
}
class Perro extends Carnivoro implements Animal{
  @override
 void emitirsonido() {
   print ('Perro Guaau');
 }
}
```
