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
## Encapsulamient0 Java

```
public class Main {
    public static void main(String args[]) {
   
       Person person = new Person("Lebrom");
       person.nombre = "James";
   
    System.out.println("El nombre es: " +person.nombre);
        System.out.println("El apellido es: " +person.getapellido());
       
        System.out.println(Person.imc(1.90, 85.8));
   }
}
class Person {
public String nombre;
    private String apellido;
    private String genero;
   
    Person(String apellido){
    this.apellido = apellido;
    }

    public String getapellido(){
    return this.apellido;    
   }
   
   public void setgenero(String g){
    this.genero = g;
        g = ("Masculino");
   }
   
   public static double imc(double altura, double peso){
    return (peso / (altura * altura));  
  }
}
```