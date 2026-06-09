# quiz_Correccion
================================================================
   QUIZ — FUNCIONES EN C++
   Universidad San Francisco de Quito — USFQ
   Curso: Programación Avanzada en C++

   Nombre: _Thiago Yumbla________________________________
   Fecha:  _8/06/2026________________________________
   Nota:   _______ / 100

   Instrucciones:
   - Duración: 50 minutos
   - Resuelve TODO en este documento o en papel
   - No se permite computadora ni calculadora
   - Escribe con letra legible
   - Si no sabes una respuesta, deja espacio y continúa
================================================================


╔══════════════════════════════════════════════════════════════╗
║   SECCIÓN A — CONCEPTUAL  (15 puntos / 5 pts c/u)          ║
║   Responde con tus propias palabras. Sé específico.        ║
╚══════════════════════════════════════════════════════════════╝

A1. (5 pts)
Explica la diferencia entre PARÁMETRO y ARGUMENTO.
Escribe un ejemplo propio de una función donde señales
claramente cuál es el parámetro y cuál es el argumento.

Respuesta:
_Parámetro: variable que aparece en la definición de la función.
Argumento: valor que se envía al llamar la función.__________________________________________________________
_______________________________________________________________
_______________________________________________________________
______________________________________________________________


A2. (5 pts)
¿Cuándo usarías paso por VALOR y cuándo paso por REFERENCIA?
Da un ejemplo concreto para cada caso que justifique tu elección.

Respuesta:
_______________________________________________________________
Referencia → modificar variable original.
Valor → trabajar con copia.____________________________________________________________
_______________________________________________________________
_______________________________________________________________
_______________________________________________________________
_______________________________________________________________


A3. (5 pts)
¿Qué es una función recursiva?
Nombra sus DOS partes obligatorias y explica qué ocurre
si falta alguna de ellas.

Respuesta:
_______________________________________________________________
_la función se llama a sí misma,  partes obligatorias:
Caso base, Caso recursivo__________________________________________________________
_______________________________________________________________
_______________________________________________________________
_______________________________________________________________
_______________________________________________________________


╔══════════════════════════════════════════════════════════════╗
║   SECCIÓN B — SELECCIÓN MÚLTIPLE Y V/F  (20 puntos)        ║
║   Encierra la letra correcta o escribe V o F               ║
╚══════════════════════════════════════════════════════════════╝

B1. (2 pts) Una variable declarada dentro de una función:
   a) Es accesible desde cualquier parte del programa
   b) Solo existe mientras la función se está ejecutando
   c) Mantiene su valor entre llamadas a la función
   d) Es igual a una variable global

   Respuesta: _____


B2. (2 pts) ¿Cuál de las siguientes sobrecargas es INVÁLIDA en C++?

   a) int f(int a, int b)   y   int f(int a, int b, int c)
   b) int f(int a)          y   double f(int a)
   c) int f(int a)          y   int f(double a)
   d) int f(int a)          y   int f(int b)

   Respuesta: _b____


B3. (2 pts) ¿Qué ocurre cuando se ejecuta return; (sin valor)
   dentro de una función void?

   a) Error de compilación
   b) La función termina de inmediato y devuelve el control
      al código que la llamó
   c) La función ignora el return y sigue ejecutando
   d) El programa termina completamente

   Respuesta: _b____


B4. (2 pts) V o F: Cuando se usa paso por valor, modificar
   el parámetro dentro de la función cambia también el valor
   de la variable original en el código que hizo la llamada.

   Respuesta: _f____


B5. (2 pts) V o F: El siguiente prototipo es válido en C++:
   void calcular(int a, double b = 3.5, int c);

   Respuesta: __f___


B6. (2 pts) ¿Cuál es el propósito del CASO BASE en una
   función recursiva?

   a) Hacer que la función sea más rápida
   b) Detener la recursión para que no sea infinita
   c) Definir cuántos parámetros recibe la función
   d) Retornar siempre el valor cero

   Respuesta: __b___


B7. (2 pts) Sobre parámetros con valor por defecto,
   ¿cuál afirmación es CORRECTA?

   a) Pueden ir en cualquier posición de la lista de parámetros
   b) Solo puede haber un parámetro con valor por defecto
   c) Deben ir al FINAL de la lista de parámetros
   d) No pueden usarse junto con otros parámetros normales

   Respuesta: _c____


B8. (2 pts) ¿Qué es la sobrecarga de funciones?
   a) Definir una función dentro de otra función
   b) Tener varias funciones con el mismo nombre pero
      diferente cantidad o tipo de parámetros
   c) Llamar a una función más de una vez en el programa
   d) Usar el mismo parámetro en distintas funciones

   Respuesta: __b___


B9. (2 pts) ¿Qué imprime el siguiente código?

   int doble(int x) { return x * 2; }

   int main() {
       int a = 5;
       int b = doble(doble(a));
       cout << b;
   }

   a) 5
   b) 10
   c) 20
   d) 40

   Respuesta: __c___


B10. (2 pts) V o F: Una función puede tener más de un
    enunciado return dentro de su cuerpo.

   Respuesta: ___V__


╔══════════════════════════════════════════════════════════════╗
║   SECCIÓN C — ANÁLISIS DE CÓDIGO  (18 puntos / 6 pts c/u)  ║
║   Lee el código y responde las preguntas.                   ║
╚══════════════════════════════════════════════════════════════╝

C1. (6 pts) Lee este fragmento:

   void duplicar(int x) {
       x = x * 2;
       cout << "Dentro: " << x << endl;
   }

   int main() {
       int a = 8;
       cout << "Antes: " << a << endl;
       duplicar(a);
       cout << "Despues: " << a << endl;
       return 0;
   }

   a) ¿Qué imprime el programa completo? (2 pts)
   ______Antes:8_
        Dentro:16________________________________________________________
   ______Antes:8_______________________________________________________
   _______________________________________________________________

   b) ¿Por qué el valor de 'a' en main no cambia
      después de llamar a duplicar? (2 pts)
   ______Por que no se guarda el valor._________________________________________________________
   _______________________________________________________________

   c) Escribe SOLO la primera línea de la función (la que
      tiene su nombre y parámetros) modificada para que 'a'
      SÍ cambie. No modifiques el cuerpo de la función.
      Esa primera línea se llama FIRMA de la función. (2 pts)

  Firma original:  void duplicar(int x)
  Firma corregida: _void duplicar(int &x)___________________________________


C2. (6 pts) Lee este fragmento:

   void mostrar(int n) {
       cout << "entero: " << n << endl;
   }
   void mostrar(double d) {
       cout << "double: " << d << endl;
   }
   void mostrar(int a, int b) {
       cout << "suma: " << a + b << endl;
   }

   int main() {
       mostrar(5);
       mostrar(3.14);
       mostrar(2, 7);
       mostrar('A');
       return 0;
   }

   a) ¿Qué versión de mostrar se llama en cada línea? (4 pts)
      Escribe la firma exacta de la versión que se ejecuta
      y justifica por qué.

  mostrar(5)    → ___mostrar(int)_____________________________________
  mostrar(3.14) → ___mostrar(double)________________________________________
  mostrar(2, 7) → ___mostrar(int a, int b)________________________________________
  mostrar('A')  → ___mostrar(int)________________________________________

   b) ¿Qué imprime mostrar('A')? Explica por qué el
      compilador elige esa versión si no existe una
      versión para char. (2 pts)
   ______Entero:65______El valor de A___________________________________________________
   _______________________________________________________________


C3. (6 pts) Lee este fragmento:

   int misterio(int n) {
       if (n == 0) return 0;
       return n + misterio(n - 1);
   }

   int main() {
       cout << misterio(4) << endl;
       return 0;
   }

   a) ¿Qué calcula esta función? Escríbelo en una oración. (2 pts)
   _______4+3+2+1+0 = 10________________________________________________________

   b) Identifica el caso base y el caso recursivo: (2 pts)
      Caso base (la línea que detiene la recursión):
      ___if(n==0) return0;____________________________________________________________
      Caso recursivo (la línea que se llama a sí misma):
      ____return n+misterio(n-1);___________________________________________________________

   c) Sigue la ejecución paso a paso para misterio(4).
      Escribe cada llamada en una línea, luego la resolución
      de vuelta. Usa este formato: (2 pts)

   misterio(4) = 4 + misterio(3)
      misterio(3) = 3+misterio(2)
      misterio(2) = ...
      misterio(1) = ...
      misterio(0) = 0   ← caso base
      ─────────────────── (resuelve de vuelta)
      misterio(1) = 1+0
      misterio(2) = 2+misterio(1)
      misterio(3) = 3+misterio(2)
      misterio(4) = 4+misterio(3)
      Resultado: ___


╔══════════════════════════════════════════════════════════════╗
║   SECCIÓN D — IDENTIFICAR Y CORREGIR ERRORES (18 pts)      ║
║   Cada fragmento tiene exactamente UN error.               ║
║   Identifícalo, explica por qué es un error y corrígelo.  ║
╚══════════════════════════════════════════════════════════════╝

D1. (6 pts)

   int mayor(int a, int b) {
       if (a > b) {
           return a;
       }
   }

   int main() {
       cout << mayor(3, 7) << endl;
       return 0;
   }

   Error: __Falta retornar algo cuando a <= b______________________________________________________
   _______________________________________________________________

   ¿Por qué es un error?
   ____Por que el valor de a es mayor que el de b y contradice la funcion.___________________________________________________________
   _______________________________________________________________

   Código corregido (escribe la función completa):
   ___int mayor(int a, int b){
   If (a>b){
   Return a;
   }else {
   Return b;}
   }______________________________________________________________
   _______________________________________________________________
   _______________________________________________________________
   _______________________________________________________________


D2. (6 pts)

   void agregarImpuesto(double precio, double porcentaje) {
       precio = precio + (precio * porcentaje / 100.0);
   }

   int main() {
       double p = 100.0;
       agregarImpuesto(p, 12.0);
       cout << "Precio con impuesto: " << p << endl;
       return 0;
   }

   Error: ____se usa paso por valor y no por referencia.____________________________________________________
   _______________________________________________________________

   ¿Por qué es un error?
   _____No se guarda o se modifica el valor__________________________________________________________
   _______________________________________________________________

   Código corregido (escribe la función completa):
   ___void agregarImpuesto(double &precio, double porcentaje) {
    precio = precio + (precio * porcentaje / 100.0);
}____________________________________________________________
   _______________________________________________________________
   _______________________________________________________________


D3. (6 pts)

   int sumar(int n) {
       return n + sumar(n - 1);
   }

   int main() {
       cout << sumar(5) << endl;
       return 0;
   }

   Error: ______falta caso base__________________________________________________
   _______________________________________________________________

   ¿Por qué es un error?
   _Por que no para el programa.______________________________________________________________
   _______________________________________________________________

   Código corregido (escribe la función completa):
   ____  Int sumar(int n){
   if(n==0) return 0;
   Return n + sumar(n-1);}____________________________________________________________
   _______________________________________________________________
   _______________________________________________________________


╔══════════════════════════════════════════════════════════════╗
║   SECCIÓN E — ESCRIBIR CÓDIGO  (29 puntos)                 ║
╚══════════════════════════════════════════════════════════════╝

E1. (12 pts)
Escribe ÚNICAMENTE el cuerpo de la función (no necesitas
escribir main). La firma ya está dada:

  void calcularEstadisticas(double a, double b, double c,
                            double &mayor, double &menor,
                            double &promedio)

  Los parámetros a, b, c se reciben por valor (el original
  no cambia). Los parámetros con & (mayor, menor, promedio)
  se reciben por referencia: la función debe asignarles
  el resultado directamente.

La función calcula:
  - mayor:    el más grande de a, b, c
  - menor:    el más pequeño de a, b, c
  - promedio: el promedio de los tres valores

NO uses funciones de la librería estándar (max, min, etc.).

Verificación: si la llamas con a=8.0, b=3.0, c=5.0,
debe asignar mayor=8.0, menor=3.0, promedio=5.33.

Tu solución:
_______________________________________________________________
_______________________________________________________________
___void calcularEstadisticas(double a, double b, double c,
                          double &mayor, double &menor,
                          double &promedio)
{
    // Mayor
    mayor = a;
    if (b > mayor)
        mayor = b;
    if (c > mayor)
        mayor = c;
    menor = a;
    if (b < menor)
        menor = b;
    if (c < menor)
        menor = c;
    promedio = (a + b + c) / 3.0;
}____________________________________________________________
_______________________________________________________________
_______________________________________________________________
_______________________________________________________________
_______________________________________________________________
_______________________________________________________________
_______________________________________________________________
_______________________________________________________________
_______________________________________________________________
_______________________________________________________________


E2. (17 pts)
Escribe la función recursiva y el main completo:
  int potencia(int base, int exponente)

La función calcula base elevado a exponente de forma RECURSIVA.
Puedes asumir que exponente >= 0.

Antes de escribir el código, responde estas preguntas
en el espacio de abajo — te ayudarán a estructurar la función:

  ¿Cuánto vale cualquier número elevado a la 0?  → _____
  Esa es tu CONDICIÓN DE PARADA (caso base).

  Si ya sabes calcular potencia(base, n-1),
  ¿cómo calculas potencia(base, n)?            → _____
  Esa es tu LLAMADA RECURSIVA.

El main debe:
  - Leer base y exponente del teclado
  - Llamar a la función
  - Imprimir el resultado

Entrada de ejemplo:  3   4
Salida esperada:
  3 elevado a la 4 = 81

IMPORTANTE: no uses pow() ni for ni while.

Tu solución:
_______________________________________________________________
_#include <iostream>
using namespace std;

int potencia(int base, int exponente)
{
    if (exponente == 0)
        return 1;
    return base * potencia(base, exponente - 1);
}

int main()
{
    int base, exponente;
    cout << "Ingrese la base: ";
    cin >> base;
    cout << "Ingrese el exponente: ";
    cin >> exponente;
    cout << base << " elevado a la "
         << exponente << " = "
         << potencia(base, exponente)
         << endl;
    return 0;
}______________________________________________________________
_______________________________________________________________
_______________________________________________________________
_______________________________________________________________
_______________________________________________________________
_______________________________________________________________



================================================================
FIN DEL QUIZ
================================================================
