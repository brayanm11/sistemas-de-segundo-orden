# Sistemas de segundo orden

Los sistemas de segundo orden son fundamentales en la ingeniería de control, ya que modelan una amplia gama de sistemas físicos como oscilaciones mecánicas, circuitos eléctricos RLC, estructuras con amortiguamiento, y sistemas de temperatura o presión. La dinámica de estos sistemas está gobernada por ecuaciones diferenciales de segundo orden, que pueden analizarse eficientemente mediante su representación en el dominio de Laplace. Esta clase busca explorar detalladamente el comportamiento de estos sistemas, sus características temporales, sus respuestas típicas y cómo se interpretan en el plano complejo.


## 1. Subtítulos

1.1 Introducción a los sistemas de segundo orden

1.2 Función de transferencia estándar

1.3 Parámetros dinámicos: frecuencia natural y factor de amortiguamiento

1.4 Respuesta al escalón unitario

1.5 Clasificación según el amortiguamiento

1.6 Análisis en el planos

1.7 Cálculo del tiempo pico, sobre impulso, y tiempo de establecimiento

1.8 Sistemas con retardo (tiempo muerto)

## 2. Definiciones
🔑 Sistema de segundo orden: sistema cuya ecuación diferencial característica contiene una derivada de segundo orden, y su comportamiento se describe mediante una función de transferencia cuadrática.

🔑 Frecuencia natural ($\omega_n$): frecuencia en radianes por segundo a la que un sistema oscilaría si no existiera amortiguamiento.

🔑 Factor de amortiguamiento ($\zeta$): número adimensional que representa la cantidad de disipación de energía en el sistema.

🔑 Sobreimpulso ($M_p$): máxima desviación porcentual del valor final, causada por la oscilación de la respuesta.

🔑 Tiempo de establecimiento ($T_s$): tiempo requerido para que la respuesta permanezca dentro de un margen (generalmente 2%) alrededor del valor final.

🔑 Tiempo pico ($T_p$): instante en que la respuesta alcanza su valor máximo.

🔑 Tiempo muerto ($T_d$): retardo temporal entre la aplicación de la entrada y el inicio visible de la respuesta del sistema.

## 3. Subsecciones

### 3.1. Función de transferencia estándar
La forma canónica de un sistema de segundo orden es:

$$G(s)=\frac{w_{n}^{2}}{s^{2}+2\zeta w_{n}+w_{n}^{2}}$$

Esta expresión representa el cociente entre la salida y la entrada en el dominio de Laplace, bajo condiciones iniciales nulas.

### 3.2. Clasificación según $\zeta$
$\zeta > 1$: Sobreamortiguado (respuesta lenta, sin oscilaciones)

$\zeta = 1$: Críticamente amortiguado (tiempo mínimo sin oscilaciones)

$0 < \zeta < 1$: Subamortiguado (oscilación con atenuación)

$\zeta = 0$: No amortiguado (oscilación pura, sin atenuación)

### 3.3. Parámetros característicos de desempeño
Frecuencia natural ($\omega_n$): determina la rapidez del sistema.

Frecuencia amortiguada ($\omega_d$): $\omega_d = \omega_n \sqrt{1 - \zeta^2}$

Tiempo pico ($T_p$): $\frac{\pi}{\omega_d}$

Sobreimpulso ($M_p$): $100\cdot e^{\left(-\frac{\pi \zeta}{\sqrt{1 - \zeta^2}}\right)}%$

Tiempo de establecimiento ($T_s$): $\frac{4}{\zeta \omega_n}$

### 3.4. Tiempo muerto (retardo)
Un sistema con retardo se representa como:

$$G(s)=G_{0}(s).e^{-T\Delta s}$$

Donde $G_0(s)$ es la función de transferencia sin retardo y $T_d$ es el tiempo muerto.

## 4. Ejemplos
Si en algún caso pretende dar un ejemplo explicativo ya sea a través de texto o através de ecuaciones matemáticos, utilizar la palabra 'Ejemplo' seguido de una numeración consecutiva dentro de la clase. Utilice el emoji 💡 antecediendo la palabra.

## 5. Ecuaciones
Para la edición de ecuaciones debe utilizar la etiqueta '$$' al comienzo y final de la ecuación para que la ecuación quede centrada ocupando una línea. Si se quiere que la ecuación quede integrada en el texto debe utilizar la etiqueta '$' al comienzo y final de la ecuación. Las ecuaciones pueden ser editadas utilizando el código LATEX, en el siguiente enlace encuentran un editor de ecuaciones que les genera el código. http://www.alciro.org/tools/matematicas/editor-ecuaciones.jsp . Sin embargo hay muchas otras herramientas que pueden utilizar para esto.

💡**Ejemplo 1:** si se va a representar la ecuación de la ley de Ohm se puede mostrar así $R=\frac{V}{I}$ o también,

$$R=\frac{V}{I}$$

$${
\begin{pmatrix*}[r]
63 & 71 & 2\\
6 & 829 & 12\\
599 & 9 & 361
\end{pmatrix*}
}={\begin{pmatrix*}[r]
63 & 71 & 2\\
6 & 829 & 12\\
599 & 9 & 361
\end{pmatrix*}}$$


## 6. Figuras
Todas las figuras que incluya deben ser generadas por ustedes, **no utilizar las figuras de las presentaciones**. Para incluir figuras puede seguir los siguientes pasos:
* Primero escribimos ![]().
* Después escribimos, dentro de los corchetes, el texto alternativo. Este es opcional y solo entra en acción cuando no se puede cargar la imagen correctamente.
* Después escribimos, dentro de los paréntesis, la ubicación del archivo (ya sea una url o una ubicación dentro de algun folder local). Se recomienda poner las imágenes en una carpeta que se llame imágenes dentro del repositorio github para que no tengan problemas al cargar las imágenes.

💡**Ejemplo 2:**

![Figura de prueba](images/plantilla/Captura2.PNG)

Figura 1. Figura de prueba

Incluya la respectiva etiqueta a modo de descripción de la figura y mantenga numeración consecutiva para todas las figuras de la clase.

## 7. Tablas
En caso de necesitar la inclusión de tablas para organizar información se recomienda el uso de la herramienta del siguiente enlace https://www.tablesgenerator.com/markdown_tables , la cual permite organizar la información dentro de la tabla y genera el código markdown automáticamente:

💡**Ejemplo 3:** 

| **Resultado** | **x = número de intentos hasta primer éxito** |
|---------------|-----------------------------------------------|
|       S       |                       1                       |
|       FS      |                       2                       |
|      FFS      |                       3                       |
|      ...      |                      ...                      |
|    FFFFFFS    |                       7                       |
|      ...      |                      ...                      |

Tabla 1. Tabla de ejemplo

Cada tabla debe llevar la etiqueta que describa su contenido y numeración consecutiva para todas las tablas

## 8. Código
Teniendo en cuenta que el curso requiere del desarrollo de código matlab, c, c++ u otro. Si requiere incluir pequeños segmentos de código en los apuntes hágalos de la siguiente manera:

💡**Ejemplo 4:**
```
var sumar2 = function(numero) {
  return numero + 2;
}
```

## 9. Ejercicios
Deben agregar 2 ejercicios con su respectiva solución, referentes a los temas tratados en cada una de las clases. Para agregar estos, utilice la etiqueta #, es decir como un nuevo título dentro de la clase con la palabra 'Ejercicios'. Cada uno de los ejercicios debe estar numerado y con su respectiva solución inmediatamente despues del enunciado. Antes del subtitulo de cada ejercicio incluya el emoji 📚

## Rúbrica
| 0-1                                                                                   | 1-2                                                                                  | 2-3                                                                                                                                                                               | 3-4                                                                                                                                                                       | 4-5                                                                                                                                                                               |
|---------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Presenta menos del 10% de los temas o no presenta por  el medio y formato  solicitado | Presenta menos del 40% de los temas solicitados, y  cumple parcialmente la plantilla | Presenta menos del 60% de los temas solicitados (con descripciones, gráficos tablas, etc), y cumple  parcialmente la plantilla. No presenta la totalidad  de ejercicios resueltos | Presenta menos del 80% de los temas solicitados (con descripciones, gráficos, tablas, etc) y cumple con  la plantilla. No presenta  la totalidad de ejercicios  resueltos | Presenta el 100% de los temas vistos en clase (con descripciones, gráficos, tablas, etc), siguiendo totalmente la plantilla. presenta la  totalidad de los ejercicios solicitados |

## 10. Conclusiones
Agregue unas breves conclusiones sobre los temas trabajados en cada clase, puede ser a modo de resumen de lo trabajado o a indicando lo aprendido en cada clase

## 11. Referencias
Agregue un subtítulo al final donde pueda poner todas las referencias consultadas incluyendo el origen o fuente de los ejercicios planteados. Tambien dentro del texto referencie los textos o artículos consultados y las figuras y tablas dentro de la explicación de las mismas.
