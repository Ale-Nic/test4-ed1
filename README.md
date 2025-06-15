# Test4 ED1 - Examen Tipo Test: Estructuras de Datos I

1. **¿Cuál de las siguientes afirmaciones sobre las funciones genéricas en C++ es verdadera según el tema 5?**  
A) Una función genérica no puede ser sobrecargada.  
B) Las plantillas de funciones siempre requieren especialización.  
C) Las plantillas permiten definir un conjunto infinito de funciones aplicables a distintos tipos.  
D) No se puede utilizar el operador < dentro de funciones genéricas.  

2. **¿Qué resultado imprime este fragmento de código?**
```cpp
template <class T>
T mayor(T a, T b) {
    return (a < b) ? b : a;
}

int main() {
    int x = 3, y = 9;
    std::cout << mayor(x, y);
}
```
A) 3  
B) 9  
C) Error de compilación  
D) Resultado indeterminado  

3. **(Múltiple) ¿Qué errores pueden derivarse del siguiente fragmento de código?**
```cpp
void insertarInicio(TNodo* Lista, float valor) {
    TNodo* NodoNuevo = new TNodo;
    NodoNuevo->Datos = valor;
    NodoNuevo->Siguiente = Lista;
    Lista = NodoNuevo;
}
```
A) Fuga de memoria  
B) El nodo no se inserta correctamente en la lista  
C) Falta liberar el puntero al final  
D) No se modifica la lista original fuera de la función  

4. **¿Cuál de las siguientes opciones describe mejor el propósito de seekp en C++?**  
A) Cambiar el tamaño de un fichero  
B) Posicionar el puntero de lectura  
C) Mover el puntero de escritura en un archivo  
D) Leer un bloque binario desde un archivo  

5. **(Múltiple) Analiza el siguiente código. ¿Qué problemas puede presentar?**
```cpp
void destruirLista(TNodo* lista) {
    while (lista != NULL) {
        delete lista;
        lista = lista->Siguiente;
    }
}
```
A) Acceso a puntero colgante  
B) Posible pérdida de acceso a nodos intermedios  
C) No se libera memoria correctamente  
D) lista->Siguiente debería guardarse antes de hacer delete  

6. **¿Qué se imprime por pantalla?**
```cpp
int tabla[] = {1, 2, 3};
int* p = tabla;
p++;
std::cout << *p;
```
A) 1  
B) 2  
C) 3  
D) Dirección de memoria  

7. **¿Qué representa este código?**
```cpp
ofstream fichero("datos.txt", ios::app || ios::binary);
```
A) Abre un archivo de texto para lectura  
B) Abre un archivo binario y sobreescribe su contenido  
C) Abre un archivo binario y añade datos al final  
D) Abre un archivo para lectura secuencial en binario  

8. **¿Cuál es el resultado de ejecutar este código?**
```cpp
int a = 5;
int* p = &a;
*p = *p + 10;
std::cout << a;
```
A) 5  
B) 10  
C) 15  
D) Dirección de p  

9. **El uso de typename en una plantilla de C++ sirve para:**
A) Declarar funciones constantes  
B) Definir el tipo de retorno de una función  
C) Especificar un tipo genérico en plantillas  
D) Crear nuevos tipos a partir de estructuras  

10. **¿Qué hace el operador -> en este código?**
```cpp
cliente* c = new cliente();
c->nombre = "Pedro";
```
A) Libera memoria  
B) Crea un puntero a función  
C) Accede al miembro de un objeto apuntado  
D) Ejecuta un constructor por defecto  

11. **¿Qué fragmento es más eficiente para insertar un valor al principio de una lista enlazada?**  
A)
```cpp
Nodo* nuevo = new Nodo;
nuevo->dato = x;
nuevo->siguiente = lista;
lista = nuevo;
```
B)  
```cpp
Nodo* nuevo = new Nodo[x];
lista = nuevo;
```
C)
```cpp
Nodo nuevo;
nuevo.dato = x;
nuevo.siguiente = lista;
lista = &nuevo;
```
D)
```cpp
lista = new Nodo;
lista->dato = x;
lista->siguiente = NULL;
```

12. **En la especificación algebraica de listas, ¿cuál es el rol de +izq?**  
A) Eliminar el primer elemento  
B) Añadir un elemento a la derecha  
C) Añadir un elemento a la izquierda  
D) Concatenar dos listas  

13. **¿Qué se debe hacer después de utilizar new en una estructura dinámica?**  
A) Nada, el sistema lo libera  
B) Usar malloc  
C) Invocar delete para evitar fugas  
D) Llamar a free obligatoriamente  

14. **¿Cuál es el riesgo de pasar una lista enlazada por puntero sin doble indirecto?**  
A) El puntero se inicializa automáticamente  
B) Los cambios en la estructura no afectan a la lista original  
C) Se pierde el acceso al nodo siguiente  
D) Se modifica el tamaño del array subyacente  

15. **¿Qué resultado imprime este fragmento?**
```cpp
char s1[] = "hola";
char s2[] = "mundo";
std::cout << mayor(s1, s2);
```
(Usando la especialización char* mayor(char*, char*) del tema 5)  
A) hola  
B) mundo  
C) Error en tiempo de ejecución  
D) El que tenga mayor orden lexicográfico  

16. **¿Qué fragmento permite liberar correctamente los nodos de una lista dinámica?**  
A)
```cpp
delete lista;
```
B)
```cpp
while (lista != NULL) {
    TNodo* aux = lista->Siguiente;
    delete lista;
    lista = aux;
}
```
C)
```cpp
while (!lista) delete lista;
```
D)
```cpp
free(lista);
```

17. **¿Cuál es el efecto de seekg(0, ios::end); en un ifstream?**  
A) Borra el contenido del archivo  
B) Cierra el flujo actual  
C) Sitúa el puntero de lectura al final del archivo  
D) Muestra el número total de líneas del archivo  

18. **¿Qué patrón arquitectónico se sugiere cuando se necesita ocultar la implementación de estructuras dinámicas al usuario?**  
A) Singleton  
B) Iterator  
C) Pimpl (Pointer to Implementation)  
D) MVC  

19. **¿Qué representa gcount() tras una lectura binaria?**  
A) Número de registros del archivo  
B) Número de bytes leídos realmente  
C) Posición del puntero de escritura  
D) Tamaño total del archivo  

20. **(Múltiple) ¿Cuáles de los siguientes fragmentos pueden provocar memory leaks?**  
A) int* x = new int(5);  
B) float* p = new float[10];  
C) delete[] p;  
D) char* c = (char*)malloc(20);  

21. **¿Cuál es la complejidad de insertar un elemento al principio de una lista simplemente enlazada?**  
A) O(1)  
B) O(n)  
C) O(log n)  
D) Depende del tipo de dato  

22. **El siguiente código genera un error sutil. ¿Cuál?**
```cpp
void eliminarPrimero(TNodo* lista) {
    delete lista;
    lista = lista->Siguiente;
}
```
A) No se elimina el nodo  
B) Se produce acceso inválido a memoria  
C) El puntero lista no se modifica fuera de la función  
D) delete no se puede usar con punteros  

23. **¿Qué estructura es más adecuada si se requiere acceso rápido a elementos por posición y tamaño variable?**  
A) Lista simplemente enlazada  
B) Tabla dinámica (array redimensionable)  
C) Lista doblemente enlazada  
D) Cola circular  

24. **¿Qué valor imprime este código?**
```cpp
int a = 3, b = 4;
int* p = &a;
*p = b;
std::cout << a;
```
A) 3  
B) 4  
C) Dirección de memoria  
D) Error en compilación  

25. **(Múltiple) ¿Qué errores puede generar este código?**
```cpp
float* valores = new float[5];
valores[6] = 3.2;
delete[] valores;
```
A) Escritura fuera de los límites del array  
B) Fuga de memoria  
C) Comportamiento indefinido  
D) Acceso correcto si el compilador lo permite  

26. **¿Qué hace seekg(0, ios::beg)?**  
A) Borra el contenido de un archivo  
B) Sitúa el puntero de lectura al inicio del archivo  
C) Lee los primeros 0 bytes  
D) Cambia el archivo a modo binario  

27. **¿Qué se necesita para recorrer una lista circular?**  
A) Dos punteros auxiliares  
B) La lista debe terminar en NULL  
C) Condición de parada que detecte el retorno al nodo inicial  
D) No puede recorrerse  

28. **¿Qué patrón de diseño representa mejor el uso de iteradores sobre TADs?**  
A) Decorator  
B) Builder  
C) Iterator  
D) Proxy  

29. **¿Cuál es el resultado?**
```cpp
int v[] = {10, 20, 30};
int* p = v;
std::cout << *(p + 2);
```
A) 10  
B) 20  
C) 30  
D) Error de ejecución  

30. **(Múltiple) ¿Cuáles de los siguientes errores pueden ocurrir al no inicializar un puntero?**  
A) Fugas de memoria  
B) Acceso a memoria no válida  
C) Errores de segmentación  
D) Desreferenciación de puntero salvaje  

31. **¿Qué hace este fragmento?**
```cpp
ifstream f("datos.bin", ios::binary);
f.seekg(0, ios::end);
int tam = f.tellg();
```
A) Lee un byte  
B) Calcula el tamaño total en bytes del archivo  
C) Sitúa el puntero al inicio  
D) Muestra la cantidad de registros  

32. **¿Qué representa el siguiente fragmento?**
```cpp
template <class T>
TLista<T>::~TLista() {
    while (elementos != NULL) {
        TNodo_Datos<T>* sig = elementos->Siguiente;
        delete elementos;
        elementos = sig;
    }
}
```
A) Constructor  
B) Destructor que libera todos los nodos  
C) Constructor que reserva nodos  
D) Fuga de memoria por punteros duplicados  

33. **¿Qué operador se emplea para obtener la dirección de una variable?**  
A) *  
B) ->  
C) &  
D) %  

34. **¿Cuál es la mejor opción para implementar una pila LIFO con eficiencia?**  
A) Lista doblemente enlazada  
B) Array estático  
C) Lista simplemente enlazada  
D) Tabla hash  

35. **¿Qué implica el uso de template <class T> al definir una clase?**  
A) Que solo puede almacenar tipos básicos  
B) Que el tipo de los datos es definido dinámicamente  
C) Que se genera una versión específica para cada tipo usado  
D) Que hereda de una clase base  

36. **¿Qué se imprime?**
```cpp
int* p = new int(7);
delete p;
std::cout << *p;
```
A) 7  
B) 0  
C) Valor indefinido o error  
D) NULL  

37. **¿Qué permite el operador delete[]?**  
A) Borrar una clase  
B) Liberar un array dinámico completo  
C) Borrar el primer elemento de una tabla  
D) Liberar un fichero  

38. **¿Cuál es una ventaja de las listas con nodo cabecera?**  
A) Ocupan menos memoria  
B) Simplifican las operaciones de inserción y eliminación en extremos  
C) Permiten acceso aleatorio directo  
D) No requieren punteros  

39. **(Múltiple) ¿Qué ventajas ofrece el uso de plantillas en estructuras de datos?**  
A) Reutilización de código  
B) Evitan duplicación de funciones  
C) Permiten trabajar con tipos desconocidos en tiempo de compilación  
D) Reducen el tamaño del binario ejecutable  

40. **¿Qué hace el siguiente código?**
```cpp
cola c;
c.desencolar();
```
(Suponiendo que la cola c está vacía)  
A) Devuelve el primer elemento  
B) Inserta un elemento  
C) Puede causar un comportamiento indefinido si no se comprueba vacía  
D) Llama al constructor por defecto  

41. **¿Qué hace este fragmento de código?**
```cpp
fichero.write((char*) &objeto, sizeof(objeto));
```
A) Lee un objeto binario del archivo  
B) Escribe un objeto binario en el archivo  
C) Convierte un objeto a texto  
D) Inicializa una estructura con ceros  

42. **¿Qué indica el método .fail() en flujos C++?**  
A) Que no se ha cerrado el archivo  
B) Que se ha producido un error en la última operación  
C) Que el archivo está lleno  
D) Que la lectura ha terminado correctamente  

43. **¿Qué fragmento previene correctamente una fuga de memoria tras usar new?**  
A)
```cpp
int* p = new int;
```
B)
```cpp
int* p = new int;
p = NULL;
```
C)
```cpp
int* p = new int;
delete p;
```
D)
```cpp
int* p = NULL;
delete p;
```

44. **¿Qué significa este constructor?**
```cpp
lista::lista(float e) {
    elementos = new float[INCREMENTO];
    elementos[0] = e;
    n = 1;
}
```
A) Crea una lista vacía  
B) Crea una lista con un solo elemento  
C) Crea una lista con incremento dinámico  
D) Crea una pila  

45. **¿Qué salida genera este código?**
```cpp
int a = 10;
int* p = &a;
std::cout << *(p + 0);
```
A) Error de compilación  
B) Dirección de a  
C) 10  
D) 0  

46. **(Múltiple) ¿Qué afirmaciones sobre el uso de new en C++ son correctas?**  
A) Permite la creación de memoria dinámica  
B) Ejecuta el constructor de un objeto si lo hay  
C) Es equivalente a malloc  
D) Puede fallar y devolver NULL  

47. **¿Qué fragmento es más eficiente para buscar un valor en una lista enlazada?**  
A)
```cpp
while (lista != NULL && lista->dato != x)
    lista = lista->siguiente;
```
B)
```cpp
for (int i = 0; i < lista.size(); i++) { /*...*/ }
```
C)
```cpp
lista.find(x);
```
D)
```cpp
lista[x];
```

48. **¿Qué ocurre si no se libera memoria dinámica antes de que finalice el programa?**  
A) Se optimiza el uso de RAM  
B) El sistema operativo la libera automáticamente en todos los casos  
C) Puede producirse una fuga de memoria  
D) Se destruyen automáticamente todos los objetos  

49. **¿Qué representa typename en la definición de plantillas?**  
A) Un tipo constante  
B) Un sinónimo de clase  
C) Un tipo genérico  
D) Una estructura anónima  

51. **¿Qué ocurre si delete[] se usa sobre un puntero no creado con new[]?**  
A) Comportamiento indefinido  
B) El programa sigue correctamente  
C) Se libera solo el primer elemento  
D) Se lanza una excepción  

52. **¿Qué tipo de acceso permite leer un bloque completo de un archivo en una única operación?**  
A) Secuencial  
B) Directo con read()  
C) getline()  
D) >> con ifstream  

53. **¿Qué salida produce?**
```cpp
float valores[3] = {1.2, 3.4, 5.6};
float* p = valores;
p++;
std::cout << *p;
```
A) 1.2  
B) 3.4  
C) 5.6  
D) Error de compilación  

53. **¿Qué ocurre si se escribe más allá del límite en una tabla dinámica?**  
A) Se redimensiona automáticamente  
B) El programa genera un error controlado  
C) Se accede a posiciones no asignadas → comportamiento indefinido  
D) Se lanza una excepción C++  

54. **¿Qué técnica se sugiere para evitar pérdida de punteros al eliminar nodos?**  
A) Liberar todos los punteros  
B) Guardar el puntero al siguiente nodo antes de eliminar  
C) Usar estructuras temporales  
D) Reservar punteros duplicados  

55. **¿Cuál es el riesgo al devolver un puntero a una variable local?**  
A) Ninguno  
B) Puede provocar una condición de carrera  
C) Se devuelve un puntero a memoria ya liberada  
D) Duplica la variable en el heap  

56. **¿Qué permite Anterior(int i) en una lista enlazada?**  
A) Obtener el último nodo  
B) Obtener el nodo anterior al índice i  
C) Insertar un nodo al final  
D) Eliminar un nodo por índice  

57. **¿Qué diferencia principal existe entre una cola circular y una cola normal?**  
A) La circular nunca se llena  
B) El puntero de inicio vuelve a cero al llegar al final físico  
C) Solo la circular permite encolar datos  
D) La cola circular no necesita punteros  

58. **¿Qué representa esta clase?**
```cpp
template <class T>
class TLista {
   // ...
};
```
A) Clase derivada  
B) Clase abstracta  
C) Clase genérica basada en plantillas  
D) Clase recursiva  

59. **¿Cuál es el comportamiento correcto de cima() en una pila?**  
A) Devuelve NULL si la pila está vacía  
B) Devuelve el elemento en el tope sin eliminarlo  
C) Desapila el último elemento  
D) Borra todos los elementos  

60. **(Múltiple) ¿Qué características definen a una especificación algebraica de TAD?**  
A) Define operaciones y tipos sin implementación  
B) Es dependiente del lenguaje de programación  
C) Se basa en términos bien formados y ecuaciones  
D) Se orienta a la representación en memoria  

## Preguntas 61-80
61. **¿Cuál de estas funciones modifica correctamente una lista enlazada desde una función externa?**  
A)
```cpp
void insertar(TNodo* lista, float valor);
```
B)
```cpp
void insertar(TNodo*& lista, float valor);
```
C)
```cpp
void insertar(const TNodo* lista, float valor);
```
D)
```cpp
void insertar(TNodo lista, float valor);
```

62. **¿Cuál es el comportamiento de una lista simplemente enlazada si no se actualiza el puntero elementos tras insertar el primer nodo?**  
A) Se produce un error de compilación  
B) La lista se inicializa vacía  
C) El nuevo nodo no queda enlazado correctamente  
D) Se elimina el último nodo  

63. **¿Qué salida produce este fragmento?**
```cpp
int v[3] = {1, 2, 3};
int* p = v;
std::cout << *(p + 1);
```
A) 1  
B) 2  
C) 3  
D) Dirección de v[1]  

64. **¿Qué problema puede producir el siguiente código?**
```cpp
TLista lista;
MostrarLista(lista);
```
(Considerando que el destructor se ejecuta tras pasar la lista por copia)  
A) Nada, se comporta correctamente  
B) La lista se borra parcialmente  
C) La lista original queda inválida por acción del destructor  
D) Solo afecta si la lista es vacía  

65. **¿Qué ventaja ofrece el uso de template <class T> en listas?**  
A) El compilador comprueba los tipos en tiempo de ejecución  
B) Se genera una versión optimizada del código para cada tipo  
C) Reduce el uso de punteros  
D) Limita la estructura a tipos básicos  

66. **¿Qué hace este código?**
```cpp
cola c;
if (!c.esvacia()) {
    Persona p = c.primero();
}
```
A) Accede al último elemento  
B) Lee el primer elemento sin extraerlo  
C) Inserta un nuevo elemento  
D) Borra la cola  

67. **¿Qué estructura se representa si un nodo contiene punteros a anterior y siguiente?**  
A) Lista circular  
B) Lista doblemente enlazada  
C) Árbol binario  
D) Cola de prioridad  

68. **¿Qué implica llamar a delete sin haber usado new?**  
A) No ocurre nada  
B) Error de compilación  
C) Comportamiento indefinido  
D) Se libera el stack  

69. **¿Qué condición define una cola como vacía?**  
A) fin == inicio  
B) inicio == -1  
C) ne == 0  
D) capacidad == 0  

70. **(Múltiple) ¿Qué ventajas ofrece el uso de listas dinámicas respecto a las estáticas?**  
A) No hay límite fijo de tamaño  
B) Uso más eficiente de memoria  
C) Requieren menos código  
D) Permiten inserciones sin desplazamientos  

71. **¿Qué instrucción mueve el puntero de escritura en un fichero binario?**  
A) seekp  
B) seekg  
C) tellp  
D) write  

72. **¿Qué operación puede provocar pérdida de datos en una tabla dinámica?**  
A) insertar sin verificación  
B) modificar  
C) eliminar sin copiar los elementos correctamente  
D) esvacia  

73. **¿Qué define INCREMENTO en la implementación de listas y pilas dinámicas?**  
A) Tamaño máximo del vector  
B) Número de elementos nuevos al ampliar capacidad  
C) Dirección del último nodo  
D) Número de elementos actuales  

74. **¿Qué error contiene este código?**
```cpp
TNodo* nodo = new TNodo;
nodo->siguiente->dato = 3;
```
A) nodo no existe  
B) dato es privado  
C) siguiente no está inicializado  
D) Falta el operador new  

75. **¿Cuál es el uso correcto de delete[]?**  
A) Eliminar una variable entera  
B) Liberar una tabla dinámica creada con new[]  
C) Eliminar un archivo  
D) Destruir un objeto  

76. **¿Qué es necesario para guardar una estructura en un archivo binario?**  
A) Convertirla a string  
B) Serializarla manualmente con write  
C) Usar fprintf  
D) Hacer cout << estructura  

77. **¿Cuál es la causa principal de una race condition en estructuras dinámicas compartidas?**  
A) Punteros no inicializados  
B) Acceso concurrente sin sincronización  
C) Declaración incorrecta de clases  
D) Uso de malloc en lugar de new  

78. **¿Qué operación afecta a los punteros al desencolar?**  
A) inicio++ o inicio = inicio->siguiente  
B) fin--  
C) ne = 0  
D) insertar  

79. **¿Qué requiere un acceso aleatorio eficiente?**  
A) Punteros a cada elemento  
B) Estructura de tabla o array  
C) Recorrido de nodos  
D) Estructura de árbol binario  

80. **(Múltiple) ¿Qué condiciones debe cumplir un TAD para considerarse correctamente especificado algebraicamente?**  
A) Todos los términos bien formados deben tener un valor único  
B) Las operaciones deben definirse mediante ecuaciones   
C) Los tipos deben implementarse en C++  
D) La semántica debe estar determinada mediante axiomas  


81. **¿Qué error sutil contiene este fragmento?**
```cpp
void eliminarLista(TNodo* lista) {
    while (lista != NULL) {
        TNodo* aux = lista;
        delete lista;
        lista = lista->Siguiente;
    }
}
```
A) La lista no se libera completamente  
B) lista se apunta a sí misma  
C) Se produce una pérdida de acceso a los nodos  
D) El orden de operaciones es incorrecto  

82. **¿Cuál es la mejor forma de insertar un nodo al final de una lista circular simple?**  
A) Insertar antes del nodo cabecera  
B) Recorrer hasta encontrar el nodo cuyo siguiente apunta al primero  
C) Reemplazar el primer nodo  
D) Insertar y borrar el último nodo  

83. **¿Qué valor se imprime?**
```cpp
int a = 5;
int* p = &a;
*p = *p + 2;
std::cout << a;
```
A) 2  
B) 5  
C) 7  
D) Dirección de a  

84. **¿Qué ocurre al ejecutar cola::desencolar() si la cola está vacía?**  
A) Se lanza una excepción automáticamente  
B) Se produce un acceso inválido si no se comprueba la condición  
C) El puntero Inicio se inicializa a NULL  
D) El compilador lo detecta y lo corrige  

85. **(Múltiple) ¿Qué errores conceptuales presenta este código?**
```cpp
TLista<T>::TLista(TLista<T> otra) {
    elementos = otra.elementos;
}
```
A) No se copia cada nodo, solo el puntero  
B) Se produce un aliasing peligroso  
C) Se realiza una copia profunda  
D) El destructor de uno afecta al otro  

86. **¿Cuál es el resultado de la siguiente operación?**
```cpp
float x = 3.5;
float* p = &x;
std::cout << *p + 2;
```
A) 3.5  
B) 2.0  
C) 5.5  
D) Dirección de x  

87. **¿Qué fragmento genera una lista genérica válida?**  
A)
```cpp
TLista<int> l;
```
B)
```cpp
TLista<T> l;
```
C)
```cpp
Lista l;
```
D)
```cpp
Lista<int> l;
```

88. **¿Qué patrón de diseño encaja mejor con cola y pila como estructuras de acceso controlado?**  
A) Strategy  
B) Factory  
C) Adapter  
D) Abstract Data Type (ADT)  

89. **¿Qué función muestra la cantidad real de bytes leídos tras read()?**  
A) eof()  
B) fail()  
C) gcount()  
D) seekg()  

90. **¿Qué instrucción garantiza que el objeto apilado está en la cima?**
```cpp
pila.apilar("dato");
```
A) pila.cima() == "dato"  
B) pila.esvacia()  
C) pila.longitud() == 0  
D) pila.desapilar()  

91. **¿Qué sucede si se hace delete[] sobre un puntero simple?**  
A) Elimina solo el primer byte  
B) Comportamiento indefinido  
C) Error en tiempo de compilación  
D) Libera correctamente la memoria  

92. **¿Qué representa este bloque?**
```cpp
template <class T>
T mayor(T a, T b) {
    return (a > b) ? a : b;
}
```
A) Sobrecarga de operadores  
B) Función especializada  
C) Plantilla genérica de función  
D) Herencia múltiple  

93. **¿Qué valor contiene a?**
```cpp
int a = 5;
int* p = &a;
int** pp = &p;
**pp = 10;
```
A) 5  
B) 10  
C) Dirección de p  
D) Error en compilación  

94. **¿Qué función accede al último nodo de una lista simple?**  
A) Anterior(n)  
B) while (nodo->Siguiente != NULL)  
C) modificar(n, valor)  
D) eliminar(1)  

95. **¿Qué operación es costosa en una tabla dinámica?**  
A) observar(i)  
B) modificar(i, e)  
C) insertar(i, e) cuando n == Tama  
D) esvacia()  

96. **¿Qué representa esta definición?**
```cpp
struct TNodo_Cola {
   Cadena Datos;
   TNodo_Cola* Siguiente;
};
```
A) Nodo de una lista simple  
B) Nodo de una pila  
C) Nodo de una cola dinámica  
D) Nodo binario  

97. **¿Qué implicación tiene ifstream f("datos", ios::binary);?**  
A) Lee datos interpretando caracteres especiales  
B) Lectura de archivo sin conversión de formato  
C) Lectura de líneas de texto  
D) Escritura en binario  

98. **¿Qué error produce este código?**
```cpp
void mostrarLista(lista l) {
    // uso de destructor tras copia
}
```
A) Fuga de memoria  
B) Sobrescritura de datos  
C) Se destruye la lista original si no se copia profundamente  
D) No hay error si lista no tiene punteros  

99. **¿Qué indica return Inicio == NULL; en una cola dinámica?**  
A) Que la cola está llena  
B) Que la cola está vacía  
C) Que la cola está corrupta  
D) Que el inicio ha sido liberado  

100. **(Múltiple) ¿Qué errores pueden surgir si se olvida liberar memoria dinámica?**  
A) Fugas de memoria  
B) Caídas progresivas de rendimiento  
C) Errores de compilación  
D) Uso de memoria no válida por el sistema operativo  

## Preguntas 101-120
101. **¿Qué resultado imprime este código?**
```cpp
char texto[] = "hola";
std::cout << texto[2];
```
A) h  
B) o  
C) l  
D) a  

102. **¿Qué riesgo existe en este código?**
```cpp
ifstream f("datos.txt");
f >> nombre;
f.close();
```
(Suponiendo que nombre es un array de char sin reserva de memoria)  
A) Error de compilación  
B) Fuga de memoria  
C) Escritura en una dirección inválida  
D) El archivo no se cierra correctamente  

103. **¿Qué estructura es más adecuada para implementar una cola de impresión?**  
A) Pila  
B) Lista doblemente enlazada  
C) Cola circular  
D) Árbol AVL  

104. **¿Cuál es el propósito de la operación seekg(0, ios::end)?**  
A) Escribir desde el final del archivo  
B) Leer la primera línea  
C) Mover el puntero de lectura al final del archivo  
D) Borrar el contenido del archivo  

105. **¿Qué error lógico presenta esta función?**
```cpp
void modificar(int i, float e) {
    elementos[i] = e;
}
```
A) No existe elementos  
B) No comprueba si el índice es válido  
C) No modifica el valor  
D) Devuelve un valor sin retorno  

106. **¿Qué patrón de diseño representa mejor una jerarquía de estructuras de datos con implementación oculta?**  
A) Factory  
B) Singleton  
C) Pimpl (Pointer to Implementation)  
D) Observer  

107. **¿Qué hace template <class T> al definir una función?**  
A) Genera múltiples versiones para cada tipo usado  
B) Permite herencia múltiple  
C) Crea una función abstracta  
D) Limita el uso a tipos básicos  

109. **¿Qué valor imprime este fragmento?**
```cpp
int* p = new int(42);
delete p;
std::cout << *p;
```
A) 42  
B) Error de compilación  
C) Valor indefinido  
D) NULL  

109. **¿Qué hace esvacia() en una pila implementada con nodos enlazados?**  
A) Devuelve el número de elementos  
B) Elimina el último nodo  
C) Verifica si el puntero elementos es NULL  
D) Borra todos los nodos  

110. **(Múltiple) ¿Qué errores pueden surgir al recorrer una lista circular sin condición de parada adecuada?**  
A) Bucle infinito  
B) Fuga de memoria  
C) Acceso fuera de la lista  
D) Bloqueo del programa  

111. **¿Qué representa el siguiente código?**
```cpp
ofstream salida("fichero.txt", ios::app);
```
A) Lectura binaria  
B) Escritura al principio del fichero  
C) Escritura al final del fichero (sin truncar)  
D) Apertura en modo lectura/escritura  

112. **¿Qué representa este fragmento?**
```cpp
class TLista {
   TNodo_Datos<T>* elementos;
};
```
A) Lista estática  
B) Pila  
C) Lista genérica dinámica  
D) Árbol  

113. **¿Qué valor tiene la variable n tras eliminar el último nodo?**
```cpp
void eliminar(int i) {
   ...
   n--;
}
```
(Suponiendo que n era 1)  
A) 1  
B) 0  
C) -1  
D) Error en tiempo de ejecución  

114. **¿Qué condición se comprueba para que una cola circular esté llena?**  
A) inicio == fin  
B) (fin + 1) % Tama == inicio  
C) ne == 0  
D) Tama == 0  

115. **¿Qué salida genera este código?**
```cpp
int a = 1, b = 2;
std::cout << mayor(a, b);
```
(Siendo mayor una plantilla que devuelve el mayor de dos valores)  
A) 1  
B) 2  
C) a  
D) Error en compilación  

116. **¿Qué ocurre si no se libera la memoria de los nodos al destruir una lista?**  
A) El compilador lo corrige automáticamente  
B) El sistema operativo la libera al instante  
C) Se produce una fuga de memoria  
D) Se produce un error en tiempo de compilación  

117. **¿Qué función mueve el puntero de entrada en un flujo?**  
A) tellp()  
B) clear()  
C) seekg()  
D) write()  

118. **¿Qué ocurre si se utiliza un puntero sin inicializar?**  
A) Se inicializa a NULL automáticamente  
B) Se genera un error de compilación  
C) Puede acceder a zonas de memoria aleatorias → comportamiento indefinido  
D) Se apunta al valor 0  

119. **¿Qué condición se cumple en una lista simplemente enlazada vacía?**  
A) elementos != NULL  
B) elementos == NULL  
C) n == -1  
D) Siguiente == elementos  

120. **(Múltiple) ¿Qué ventajas ofrece el uso de archivos binarios en estructuras de datos?**  
A) Mayor eficiencia en lectura/escritura  
B) Almacenamiento compacto  
C) Legibilidad directa por humanos  
D) Permite guardar estructuras sin conversión a texto  


121. **¿Qué valor se imprime?**
```cpp
int x = 2;
int y = 5;
std::cout << mayor(x, y);
```
(Siendo mayor una función plantilla que devuelve el mayor)  
A) 2  
B) 5  
C) y  
D) Error en compilación  

122. **¿Qué produce este fragmento?**
```cpp
TNodo* nodo = NULL;
nodo->dato = 5;
```
A) Asigna correctamente el valor  
B) Compila pero da error en ejecución  
C) Error en compilación  
D) Crea un nodo nuevo  

123. **¿Qué operación permite recorrer nodos sucesivos en una lista simple?**  
A) elementos->Anterior  
B) elementos->Siguiente  
C) elementos->Fin  
D) elementos->Cabeza  

124. **¿Cuál es el principal inconveniente de una tabla estática?**  
A) No se puede acceder por posición  
B) No se puede ordenar  
C) Tiene tamaño fijo y poco flexible  
D) No permite modificación  

125. **¿Qué implica este fragmento?**
```cpp
int* p = NULL;
if (!p) std::cout << "nulo";
```
A) Acceso inválido  
B) Muestra "nulo"  
C) Error de compilación  
D) Inicialización con valor por defecto  

126. **¿Qué hace este código en un archivo binario?**
```cpp
entrada.read((char *) fichas, 3*sizeof(ficha));
```
A) Escribe 3 fichas en un archivo  
B) Lee 3 fichas completas desde archivo  
C) Borra el archivo  
D) Lee el nombre de una sola ficha  

127. **¿Qué ocurre si nodo->Siguiente apunta a sí mismo?**  
A) Nada anormal  
B) Se forma una lista circular de un solo nodo  
C) Se genera una condición de carrera  
D) Se borra el nodo  

128. **¿Qué representa Cadena en esta declaración?**
```cpp
Cadena Datos;
```
A) Tipo definido con typedef  
B) Clase estándar de C++  
C) Campo privado  
D) Enumeración  

129. **¿Qué estructura necesita dos punteros (Inicio, Fin)?**  
A) Lista simplemente enlazada  
B) Pila  
C) Cola dinámica  
D) Lista doblemente enlazada  

130. **(Múltiple) ¿Qué errores de rendimiento puede causar el uso indebido de new?**  
A) Fragmentación de memoria  
B) Fugas por olvidar delete  
C) Redimensionado costoso  
D) Acceso concurrente mal sincronizado  

131. **¿Qué código copia el contenido de una lista en otra?**  
A) lista2 = lista1;  
B) lista2.insertar(1, lista1);  
C) Recorrer lista1 y clonar nodos uno a uno  
D) lista2 = &lista1;  

132. **¿Qué implica template <class T, class U>?**  
A) Se definen dos tipos genéricos  
B) T y U son sinónimos  
C) Solo se permite un tipo básico  
D) No se puede usar en métodos  

133. **¿Qué ventaja ofrece usar un nodo cabecera en listas?**  
A) Evita duplicación de nodos  
B) Facilita las inserciones y eliminaciones en extremos  
C) Aumenta la eficiencia de búsqueda  
D) Reduce el tamaño del código  

134. **¿Qué función devuelve el valor del primer nodo de una lista?**  
A) observarIzq()  
B) eliminarIzq()  
C) posicion(1)  
D) esvacia()  

135. **¿Qué comportamiento tiene esta instrucción?**
```cpp
delete [] elementos;
```
A) Libera solo el primer elemento  
B) Libera todo el array dinámico  
C) Elimina una clase  
D) Da error si el puntero está NULL  

136. **¿Cuál es el propósito de Anterior(int i)?**  
A) Buscar un valor por índice  
B) Insertar un nodo  
C) Devolver el nodo anterior al i-ésimo  
D) Obtener el último nodo  

137. **¿Qué salida genera?**
```cpp
char cad[] = "chat";
std::cout << cad[0];
```
A) c  
B) h  
C) a  
D) t  

138. **¿Qué función modifica el valor de un nodo existente?**  
A) insertar(i, e)  
B) eliminar(i)  
C) modificar(i, e)  
D) observar(i)  

139. **¿Qué sucede si el puntero de una pila dinámica es NULL?**  
A) El tope apunta a un valor no válido  
B) El método cima() devuelve el último elemento  
C) La pila está vacía  
D) Se produce una excepción  

140. **(Múltiple) ¿Qué aspectos se deben considerar al definir una estructura dinámica?**  
A) Gestión explícita de memoria  
B) Comprobación de punteros  
C) Reducción de complejidad temporal  
D) Acceso directo a elementos intermedios sin recorrer  


141. **¿Qué hace este código?**
```cpp
if (fichero.fail()) {
   std::cout << "Error al abrir";
}
```
A) Comprueba si el archivo ha llegado al final  
B) Verifica si hubo error al abrir el archivo  
C) Escribe contenido en el archivo  
D) Inicializa el archivo en binario  

142. **¿Qué propiedad tiene una pila respecto al orden de acceso?**  
A) FIFO  
B) FILO  
C) LIFO  
D) LILO  

143. **¿Cuál es el propósito de la función tellg()?**  
A) Mueve el puntero de lectura  
B) Retorna el número de líneas de un archivo  
C) Indica la posición actual de lectura en el archivo  
D) Cierra el archivo  

144. **¿Qué indica que Inicio == NULL en una cola dinámica?**  
A) Cola llena  
B) Cola vacía  
C) Se ha borrado un nodo  
D) El archivo está cerrado  

145. **¿Qué representa typedef char cadena[30];?**  
A) Define una constante  
B) Declara una función  
C) Crea un nuevo tipo llamado cadena  
D) Establece una cadena dinámica  

146. **¿Qué acción realiza delete p; cuando p es un puntero a objeto?**  
A) Elimina la clase  
B) Libera la memoria y llama al destructor  
C) Borra solo la primera variable  
D) No tiene efecto si no se usa new  

147. **¿Qué valor se imprime?**
```cpp
int tabla[3] = {3, 6, 9};
int* p = tabla;
p += 2;
std::cout << *p;
```
A) 3  
B) 6  
C) 9  
D) Error en compilación  

148. **¿Qué función sirve para obtener la posición de un elemento?**  
A) modificar(e)  
B) insertar(i,e)  
C) posicion(e)  
D) observar(i)  

149. **¿Qué representa el operador -> en C++?**  
A) Paso por referencia  
B) Acceso a puntero a función  
C) Acceso a miembro de un objeto apuntado  
D) Comparación de punteros  

150. **(Múltiple) ¿Qué condiciones deben cumplirse al liberar una lista enlazada?**  
A) Eliminar nodo a nodo con delete  
B) No perder el puntero al siguiente nodo  
C) Llamar al destructor del nodo  
D) Inicializar el puntero principal a NULL  

151. **¿Qué sucede si se aplica seekp(0, ios::end) a un fichero?**  
A) Lee el archivo desde el principio  
B) Posiciona el puntero de escritura al final  
C) Elimina el contenido  
D) Lee un bloque binario  

152. **¿Qué sucede si se inserta un nodo sin redimensionar una tabla dinámica llena?**  
A) Se redimensiona automáticamente  
B) El nodo se pierde  
C) Error o acceso a memoria no reservada  
D) El último valor se sobreescribe  

153. **¿Qué representa p->dato si p es un puntero a TNodo?**  
A) Accede a la dirección de dato  
B) Copia dato a p  
C) Accede al campo dato del nodo apuntado por p  
D) Borra el valor dato  

154. **¿Cuál es el valor de a?**
```cpp
int a = 1;
int* p = &a;
*p = 4;
```
A) 1  
B) 4  
C) Dirección de a  
D) Valor indefinido  

155. **¿Qué método se usa para escribir datos binarios?**  
A) <<  
B) fprintf()  
C) write()  
D) putline()  

156. **¿Qué ocurre si delete se llama más de una vez sobre el mismo puntero?**  
A) Error en compilación  
B) Comportamiento indefinido  
C) Se ignora la segunda llamada  
D) Se reinicia el valor del puntero  

157. **¿Qué devuelve longitud() en una lista?**  
A) El número de bytes  
B) La capacidad máxima  
C) La cantidad de nodos actuales  
D) El índice del último elemento  

158. **¿Qué condición provoca redimensionado de una tabla dinámica?**  
A) Tama == 0  
B) n == Tama  
C) Tama > n  
D) n == 1  

159. **¿Qué efecto tiene declarar delete [] tabla;?**  
A) Libera una sola celda  
B) Libera el objeto tabla  
C) Libera una tabla dinámica completa creada con new[]  
D) Da error si la tabla es estática  

160. **(Múltiple) ¿Qué implicaciones tiene recorrer una lista dinámica con puntero auxiliar?**  
A) Permite no perder la referencia original  
B) Evita modificar la cabeza de la lista  
C) Facilita la destrucción segura de nodos  
D) Disminuye el uso de memoria  


161. **¿Qué hace el siguiente fragmento?**
```cpp
ifstream f("datos.bin", ios::binary);
f.seekg(0, ios::end);
int tam = f.tellg();
```
A) Lee el primer carácter del archivo  
B) Indica cuántos bytes tiene el archivo  
C) Borrar el archivo  
D) Devuelve el índice del último registro lógico  

162. **¿Qué estructura permite acceso O(1) por índice?**  
A) Lista simplemente enlazada  
B) Árbol binario  
C) Tabla dinámica  
D) Pila  

163. **¿Qué error presenta este código?**
```cpp
void eliminarIzq() {
    elementos = elementos->Siguiente;
}
```
A) Fuga de memoria  
B) No se elimina el primer nodo  
C) Se elimina el último nodo  
D) Asigna NULL directamente  

164. **¿Qué función garantiza el acceso sin modificación al nodo i?**  
A) observar(i)  
B) modificar(i, x)  
C) eliminar(i)  
D) insertar(i, x)  

165. **¿Qué representa typename?**  
A) Declara una constante de tipo clase  
B) Es un alias para int  
C) Indica un parámetro de tipo en plantillas  
D) Se usa en estructuras anidadas  

166. **¿Qué hace seekp(0, ios::beg)?**  
A) Mueve el puntero de lectura al principio  
B) Mueve el puntero de escritura al principio  
C) Lee un carácter del principio  
D) Borra el archivo  

167. **¿Qué condición define el final de una lista simple?**  
A) Siguiente == NULL  
B) elementos == NULL  
C) posicion == longitud()  
D) modificar == false  

168. **(Múltiple) ¿Qué riesgos implica el uso de estructuras dinámicas?**  
A) Fugas de memoria  
B) Acceso a punteros no válidos  
C) Fragmentación del heap  
D) Control completo sobre el recolector de basura  

169. **¿Cuál es el resultado?**
```cpp
float v[] = {2.5, 4.1, 6.0};
std::cout << *(v + 1);
```
A) 2.5  
B) 4.1  
C) 6.0  
D) Dirección de v[1]  

170. **¿Qué diferencia principal hay entre read() y >>?**  
A) Ninguna  
B) read() permite acceder a campos privados  
C) read() opera a nivel de bytes, >> a nivel de texto  
D) >> es binario, read() es textual  

171. **¿Qué hace este fragmento?**
```cpp
if (elementos == NULL)
   return true;
```
A) Comprueba si hay un solo nodo  
B) Verifica si la lista está vacía  
C) Devuelve la longitud  
D) Comprueba si el nodo actual es el final  

172. **¿Qué representa la función eliminar(i)?**  
A) Borra el nodo de la cabeza  
B) Borra el último nodo  
C) Elimina el nodo en la posición i  
D) Vacia toda la lista  

173. **¿Cuál es la causa más común de acceso inválido con punteros?**  
A) Declarar sin inicializar  
B) Uso de delete[]  
C) Crear estructuras grandes  
D) Recorrer listas con for  

174. **¿Qué debe hacerse tras liberar todos los nodos de una lista?**  
A) Cerrar el archivo  
B) Decrementar la variable global n  
C) Asignar elementos = NULL  
D) Insertar un nodo vacío  

175. **¿Qué ventaja aporta usar plantillas en listas?**  
A) Menor uso de memoria  
B) Compatibilidad con cualquier tipo  
C) No se necesita destructor  
D) Se evitan ciclos infinitos  

176. **¿Qué imprime este código?**
```cpp
char c[] = "abc";
std::cout << *(c + 2);
```
A) a  
B) b  
C) c  
D) Error en compilación  

177. **¿Qué pasa si no se actualiza el puntero Fin en una cola dinámica?**  
A) Se borra el primer nodo  
B) No se puede encolar correctamente  
C) Se recorre en orden inverso  
D) La cola se convierte en pila  

178. **¿Qué salida produce este código?**
```cpp
int w[] = {1, 2, 3};
int* p = w;
std::cout << *(p++);
```
A) 1  
B) 2  
C) 3  
D) Dirección de p  

179. **¿Qué tipo de implementación se describe con new, delete y punteros?**  
A) Estática  
B) Basada en arrays  
C) Dinámica  
D) Recursiva  

180. **(Múltiple) ¿Qué condiciones pueden causar comportamiento indefinido?**  
A) Acceder a memoria liberada  
B) Usar punteros sin inicializar  
C) Liberar punteros múltiples veces  
D) Usar seekp en modo lectura  


181. **¿Qué resultado imprime este fragmento?**
```cpp
int a = 3;
int b = 7;
std::cout << mayor(a, b);
```
(Siendo mayor una función plantilla que devuelve el mayor)  
A) 3  
B) 7  
C) b  
D) Error de compilación  

182. **¿Qué ventaja ofrece usar seekg y seekp en archivos binarios?**  
A) Posicionamiento preciso dentro del archivo  
B) Convertir texto a binario  
C) Borrar archivos  
D) Comprimir datos  

183. **¿Qué error contiene este código?**
```cpp
void destruirLista(TNodo* lista) {
   while (lista != NULL) {
      delete lista;
      lista = lista->Siguiente;
   }
}
```
A) Fuga de memoria  
B) Doble liberación  
C) El puntero siguiente se pierde antes del delete  
D) Error en compilación  

184. **¿Qué propiedad cumple una cola FIFO?**  
A) El último en entrar es el primero en salir  
B) El primero en entrar es el primero en salir  
C) Se eliminan los elementos por el final  
D) Se recorre siempre en sentido inverso  

185. **¿Qué se necesita para usar una plantilla con tipos personalizados?**  
A) Que tengan sobrecargado el operador =  
B) Que sean clases estáticas  
C) Que no usen new  
D) Que hereden de una clase base común  

186. **¿Qué instrucción produce redimensionamiento?**
```cpp
if (n == Tama)
   // ...
```
A) modificar()  
B) esvacia()  
C) insertar()  
D) concatenar()  

187. **¿Cuál es el uso de delete []?**  
A) Borra un solo elemento  
B) Libera una tabla dinámica creada con new[]  
C) Cierra un archivo  
D) Borra el nodo de una lista  

188. **(Múltiple) ¿Qué ventajas ofrece una implementación con nodos enlazados?**  
A) Flexibilidad en tamaño  
B) No requiere memoria contigua  
C) Inserción/eliminación eficiente  
D) Acceso directo por índice  

189. **¿Qué representa NULL en punteros?**  
A) Dirección de un objeto destruido  
B) Puntero a dirección 0  
C) Final de archivo  
D) Identificador de memoria dinámica  

190. **¿Qué hace el siguiente código?**
```cpp
TNodo* nodo = new TNodo;
nodo->Siguiente = NULL;
```
A) Inicializa un nodo sin conectar  
B) Borra el nodo  
C) Accede a un nodo inexistente  
D) Declara el nodo como constante  

191. **¿Qué pasa si elementos == NULL y se llama a elementos->Siguiente?**  
A) Devuelve NULL  
B) Causa error en tiempo de compilación  
C) Comportamiento indefinido (acceso inválido)  
D) El programa lo ignora  

192. **¿Qué hace este fragmento?**
```cpp
if (!entrada) {
   std::cout << "Error";
}
```
A) Comprueba si el archivo ha llegado a EOF  
B) Verifica si hubo error de apertura  
C) Borra el archivo  
D) Reinicia la entrada  

193. **¿Qué devuelve cima() en una pila?**  
A) El primer nodo  
B) El último nodo  
C) El nodo del tope  
D) Siempre NULL  

194. **¿Qué representa Inicio == Fin == NULL en una cola?**  
A) Cola vacía  
B) Cola llena  
C) Cola circular  
D) Nodo mal referenciado  

195. **¿Qué salida da?**
```cpp
char c[] = "hola";
std::cout << *(c + 1);
```
A) h  
B) o  
C) l  
D) a  

196. **¿Qué hace este constructor?**
```cpp
lista::lista(float e) {
   elementos = new float[INCREMENTO];
   n = 1;
   elementos[0] = e;
}
```
A) Crea una lista vacía  
B) Crea una lista con un elemento inicial  
C) Declara un array estático  
D) Borra la lista  

197. **¿Qué indica el operador * al acceder a punteros?**  
A) Multiplicación  
B) Dirección de memoria  
C) Desreferenciación  
D) Encapsulamiento  

198. **¿Qué hace seekg(0, ios::beg)?**  
A) Sitúa el puntero de escritura al principio  
B) Sitúa el puntero de lectura al principio  
C) Borra el archivo  
D) Reescribe los datos  

199. **(Múltiple) ¿Qué funciones deben implementarse correctamente para evitar fugas en listas?**  
A) Destructor  
B) Insertar  
C) Eliminar  
D) Modificar  

200. **¿Qué error lógico contiene este código?**
```cpp
void insertarInicio(TNodo* lista, float valor) {
   TNodo* nuevo = new TNodo;
   nuevo->dato = valor;
   nuevo->Siguiente = lista;
   lista = nuevo;
}
```
A) El nodo se inserta correctamente  
B) Se modifica una copia local del puntero  
C) Falta asignar a NULL  
D) El destructor se llama dos veces  

## Soluciones
1. C. Las plantillas definen infinitas funciones aplicables a distintos tipos.
2. B. La función mayor devuelve el mayor entre 3 y 9.
3. A, B, D. No se modifica el puntero original por valor.
4. C. seekp mueve el puntero de escritura.
5. B, D. Falta guardar el siguiente nodo antes de liberar.
6. B. p++ apunta al segundo elemento: 2.
7. C. Apertura binaria con escritura al final.
8. C. Se modifica el valor de a directamente.
9. C. Especifica tipos genéricos.
10. C. -> accede al campo del objeto apuntado.
11. A. Inserta correctamente y actualiza el puntero.
12. C. +izq añade al principio.
13. C. delete es obligatorio para evitar fugas.
14. B. No se modifica el puntero original.
15. D. Compara con strcmp, devuelve mayor en orden lexicográfico.
16. B. Patrón correcto para liberar todos los nodos.
17. C. Posiciona el puntero al final.
18. C. Pimpl oculta la implementación.
19. B. Indica los bytes realmente leídos.
20. A, B, D. Solo C es correcta (libera).
21. A. Insertar al principio de una lista enlazada es O(1).
22. C. Se modifica una copia local del puntero.
23. B. Las tablas dinámicas permiten acceso directo y tamaño variable.
24. B. Se modifica a mediante su puntero.
25. A, C. Índice fuera de rango provoca comportamiento indefinido.
26. B. Sitúa el puntero de lectura al inicio.
27. C. La condición de parada es retornar al nodo inicial.
28. C. Permite recorrer estructuras sin exponer detalles.
29. C. *(p + 2) es 30.
30. B, C, D. Acceder a punteros no inicializados puede causar fallos graves.
31. B. tellg() en posición final indica el tamaño del archivo.
32. B. Destructor que elimina todos los nodos.
33. C. & devuelve la dirección de una variable.
34. C. Inserción/eliminación al principio en O(1).
35. C. El compilador genera instancias por tipo.
36. C. Acceder a memoria liberada genera valor indefinido.
37. B. Libera memoria de arrays dinámicos creados con new[].
38. B. Evita código especial para inserciones al inicio.
39. A, B, C. Las plantillas aumentan flexibilidad y reutilización.
40. C. Desencolar sin comprobar puede causar errores.
41. B. Escribe un objeto binario en el fichero.
42. B. .fail() indica un error en la operación anterior.
43. C. Solo delete p; evita la fuga.
44. B. Crea una lista con un solo valor.
45. C. *(p + 0) es equivalente a *p.
46. A, B, D. new ejecuta constructor y puede fallar.
47. A. Recorre la lista hasta encontrar el valor.
48. C. Puede haber fuga si no se libera memoria.
49. C. Define tipos genéricos en plantillas.
50. A. Comportamiento indefinido.
51. B. read() permite lectura directa por bloques.
52. B. p++ avanza al segundo elemento.
53. C. El acceso fuera de rango es indefinido.
54. B. Guardar antes el Siguiente.
55. C. Variable local se destruye al salir de la función.
56. B. Devuelve el nodo anterior al i.
57. B. El índice se recicla en circular.
58. C. Clase genérica basada en plantillas.
59. B. cima() observa sin modificar.
60. A, C. Independencia del lenguaje y uso de ecuaciones.
61. B. El paso por referencia permite modificar la lista original.
62. C. El nuevo nodo queda sin enlace.
63. B. *(p + 1) vale 2.
64. C. El destructor afecta al original.
65. B. Se genera una versión por tipo usado.
66. B. Lee el primer elemento sin extraerlo.
67. B. Lista doblemente enlazada.
68. C. Comportamiento indefinido.
69. C. ne == 0 indica vacío.
70. A, B, D. Sin límite y sin desplazamientos.
71. A. seekp mueve el puntero de escritura.
72. C. Eliminar sin copiar puede perder datos.
73. B. INCREMENTO define la ampliación.
74. C. siguiente no está inicializado.
75. B. Liberar una tabla dinámica.
76. B. Serializar con write.
77. B. Acceso concurrente sin sincronización.
78. A. Avanzar inicio.
79. B. Requiere array para acceso aleatorio.
80. A, B, D. Definición matemática sin implementación.
81. D. delete debe ir tras guardar Siguiente.
82. B. Se inserta recorriendo hasta el último nodo.
83. C. a toma el valor 7.
84. B. Acceso inválido si no se comprueba.
85. A, B, D. Copia superficial y destructor compartido.
86. C. 5.5.
87. A. TLista<int> l.
88. D. ADT.
89. C. gcount().
90. A. cima() == "dato".
91. B. Comportamiento indefinido con delete[].
92. C. Plantilla genérica de función.
93. B. a vale 10.
94. B. Recorre hasta Siguiente == NULL.
95. C. Insertar con n == Tama.
96. C. Nodo de cola dinámica.
97. B. Lectura sin conversión en binario.
98. C. Se destruye la lista original.
99. B. Indica cola vacía.
100. A, B, D. Fugas y degradación.
101. C. texto[2] es 'l'.
102. C. Riesgo de escritura inválida.
103. C. Cola circular.
104. C. Mueve el puntero al final del archivo.
105. B. No comprueba el índice.
106. C. Pimpl.
107. A. Genera versiones por tipo.
108. C. Valor indefinido tras delete.
109. C. Verifica puntero NULL.
110. A, D. Bucle infinito o bloqueo.
111. C. Escritura al final.
112. C. Lista genérica dinámica.
113. B. n pasa a 0.
114. B. (fin + 1) % Tama == inicio.
115. B. Devuelve 2.
116. C. Fuga de memoria.
117. C. seekg().
118. C. Acceso a memoria aleatoria.
119. B. elementos == NULL.
120. A, B, D. Binario eficiente y directo.
121. B. 5.
122. B. Error en ejecución por NULL.
123. B. elementos->Siguiente.
124. C. Tamaño fijo.
125. B. Muestra "nulo".
126. B. Lee 3 fichas.
127. B. Lista circular de un nodo.
128. A. Tipo typedef.
129. C. Cola dinámica.
130. A, B, D. Fragmentación y fugas.
131. C. Copiar nodo a nodo.
132. A. Dos tipos genéricos.
133. B. Facilita inserciones en extremos.
134. A. observarIzq().
135. B. Libera todo el array.
136. C. Nodo anterior al i.
137. A. 'c'.
138. C. modificar(i, e).
139. C. La pila está vacía.
140. A, B, C. Gestión de memoria y punteros.
141. B. Verifica error al abrir.
142. C. LIFO.
143. C. Indica posición de lectura.
144. B. Cola vacía.
145. C. Nuevo tipo cadena.
146. B. Libera y llama al destructor.
147. C. 9.
148. C. posicion(e).
149. C. Acceso a miembro del objeto apuntado.
150. A, B, D. Liberar nodo a nodo y anular puntero.
151. B. Puntero de escritura al final.
152. C. Error o acceso fuera de rango.
153. C. Accede al campo dato.
154. B. a vale 4.
155. C. write().
156. B. Comportamiento indefinido.
157. C. Cantidad de nodos.
158. B. n == Tama.
159. C. Libera tabla dinámica.
160. A, B, C. Mantiene referencia, evita modificar cabeza y permite liberar.
161. B. Indica tamaño en bytes.
162. C. Tabla dinámica.
163. A. Fuga de memoria.
164. A. observar(i).
165. C. Parámetro de tipo.
166. B. Mueve el puntero de escritura al principio.
167. A. Siguiente == NULL.
168. A, B, C. Fugas, punteros inválidos y fragmentación.
169. B. 4.1.
170. C. read es binario; >> es textual.
171. B. Verifica lista vacía.
172. C. Elimina el nodo en i.
173. A. Punteros sin inicializar.
174. C. Asignar elementos = NULL.
175. B. Compatibilidad con cualquier tipo.
176. C. 'c'.
177. B. No se puede encolar correctamente.
178. A. 1.
179. C. Implementación dinámica.
180. A, B, C. Todas generan indefinido.
181. B. 7.
182. A. Posicionamiento preciso.
183. C. Se pierde Siguiente antes del delete.
184. B. FIFO.
185. A. Deben soportar asignación.
186. C. insertar() para redimensionar.
187. B. Liberar arrays new[].
188. A, B, C. Tamaño flexible y eficientes.
189. B. Dirección 0.
190. A. Crea nodo sin conexiones.
191. C. Acceso inválido.
192. B. Detecta error de apertura.
193. C. Valor en el tope.
194. A. Cola vacía.
195. B. 'o'.
196. B. Lista con elemento inicial.
197. C. Desreferenciación.
198. B. Puntero de lectura al inicio.
199. A, B, C. Destructor, insertar y eliminar.
200. B. Se modifica una copia local.
