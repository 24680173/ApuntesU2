# ApuntesU2
---
## TransformaciÓn bidimensional
Las transformaciones nos permiten alterar de una forma uniforme toda la imagen. Es un hecho que a veces es más fácil modificar toda la imagen que una porción de ella. Esto supone un complemento muy útil para las técnicas de dibujo manual, donde es normalmente más fácil modificar una pequeña porción del dibujo que crear un dibujo completamente nuevo.
La composición de transformaciones bidimensionales consiste en la mezcla de las transformaciones bidimensionales básicas como son traslación, sesgado y escalado.
Notemos que no mencionamos la rotación como una transformación básica, esta es en realidad la combinación de escalado y sesgado.  
<img width="640" height="367" alt="image" src="https://github.com/user-attachments/assets/6a42c831-92f8-4e3d-9ca9-ccd18204b375" />
##
---
## Traslación
Una traslación es el movimiento en línea recta de un objeto de una posición a otra. Movimiento de una figura, sin rotarla ni voltearla. "Deslizar".
La figura sigue viéndose exactamente igual, solo que en un lugar diferente. Se aplica una transformación en un objeto para cambiar su posición a lo largo de la trayectoria de una línea recta de una dirección de coordenadas a otra. 
Se traslada un punto de la posición coordenada (X, Y) a una nueva posición (x’, y’) agregando distancias de traslación, Tx y Ty, a las coordenadas originales: x’ = x + Tx, y’ = y + Ty. 
El par de distancia de traslación (Tx, Ty) se denomina también vector de traslación o bien vector de cambio. 
Los polígonos se trasladan agregando las distancias de traslación especificadas a las coordenadas de cada punto extremo de la línea en el objeto. 
Los objetos trazados con curvas se trasladan cambiando las coordenadas definidoras del objeto. Para cambiar la posición de una circunferencia o elipse, se trasladan las coordenadas centrales y se vuelve a trazar la figura en la nueva localidad. 
Las distancias de traslación pueden especificarse como cualquier número real (positivo, negativo o cero). Si un objeto se traslada más allá de los límites del despliegue en coordenadas del dispositivo, el sistema podría retornar un mensaje de error, suprimir partes del objeto que sobrepasan los límites del despliegue o presentar una imagen distorsionada.


##
---
## Escalonamiento
Una transformación para alterar el tamaño de un objeto se denomina escalamiento. Dependiendo del factor de escalamiento el objeto sufrirá un cambio en su tamaño pasando a ser mayor, o menor en su segmento de longitud. Esta es la transformación del objeto especialmente interesante, pues con ella se consigue el efecto Zoom.   
<img width="320" height="262" alt="image" src="https://github.com/user-attachments/assets/bede7908-b3a2-4a2b-be2c-d6a754d73444" />                                                
La operación de escalado modifica la distancia de los puntos sobre los que se aplica, respecto a un punto de referencia. Para definir esta operación son necesarios dos factores de escala, Sx y Sy, según las direcciones x e y, y un punto o eje de referencia.
Cualquier valor numérico positivo puede asignarse a los factores de escalación Sx y Sy. 
Los valores menores que 1 reducen el tamaño de los objetos; 
Los valores mayores que 1 producen un agrandamiento. 
Si se especifica un valor de 1 para Sx y Sy se mantiene inalterado el tamaño de los objetos. 
Cuando a Sx y Sy se les asigna el mismo valor, se produce una escalación uniforme, la cual mantiene las propiedades relativas del objeto a escala. 
Escalado uniforme: El factor de escala es el mismo en las dos coordenadas, es decir Sx=Sy, y por lo tanto varía el tamaño pero no la forma del objeto.
Escalado diferencial: El factor de escala es distinto en cada dirección, es decir Sx es distinto de Sy, y se produce una distorsión en la forma del objeto.
##
---
## Rotación
La rotación es el movimiento circular de un objeto alrededor de un centro. Es posible rotar diferentes figuras en un ángulo alrededor del punto central. Matemáticamente, una rotación se define como un mapa. Todas las rotaciones alrededor de un punto fijo que forman un grupo dentro de una estructura se denominan grupo de rotación de un espacio único. En el caso de las figuras tridimensionales, podemos girar o rotar los objetos alrededor de un número infinito de líneas imaginarias conocidas como ejes de rotación. Ahora bien, ¿qué es la rotación de ejes ? Aquí está la respuesta. Las rotaciones alrededor de los ejes X, Y y Z se conocen como rotaciones principales. Las rotaciones alrededor de cualquier eje se pueden realizar tomando la rotación alrededor del eje X, seguida del eje Y y finalmente del eje Z.

Fórmula de rotación
La rotación puede realizarse en ambos sentidos, tanto en el sentido de las agujas del reloj como en el sentido contrario. Los ángulos de rotación más comunes son 90°, 180° y 270°. Sin embargo, una rotación en el sentido de las agujas del reloj implica una magnitud negativa, mientras que una rotación en sentido contrario tiene una magnitud positiva. Existen reglas específicas para la rotación en el plano cartesiano. Estas son:
<img width="1033" height="824" alt="image" src="https://github.com/user-attachments/assets/0f2a0d3b-c531-470f-ae37-55bd472795fa" />
##
---
## Sesgado
El sesgado es un tipo de transformación no rígida, pues existe una deformación del objeto original al aplicar dicha transformación. Existen dos tipos de sesgo: sesgo horizontal y sesgo vertical. 
<br> Sesgo horizontal. Las coordenadas adyacentes al eje x permanecen fijas, los valores de y no cambian. 
<br> Sesgo vertical. Las coordenadas adyacentes al eje y permanecen fijas, los valores de x no cambian. 
<img width="329" height="321" alt="image" src="https://github.com/user-attachments/assets/2db39fd6-68d1-4206-b2ea-25e814117e27" />
## 
---
## Representación matricial de las transformaciones bidimensionales
Representación matricial.
En el área de la graficación por computadora, es común encontrar la representación de las ecuaciones de transformación por medio de matrices, y se pueden encontrar dos tipos de notaciones para representarlas:
1.- Repesentando las coordenadas de un punto p como vectores renglón (en este caso una matriz de transformación M en 2 dimensiones, multiplica al punto por la derecha para obtener el nuevo punto p'.
p= [x1    x2],   p'=[x1    x2]= p*M

2.- Representando las coordenadas de un punto p como vectores columna, en este caso una matriz de transformación M, multiplica al punto por la izquierda para obtener el nuevo punto p'.

       x1            x1'
p=[ x2 ],  p'=[ x2' ] =M*p 
 

Muchas aplicaciones incluyen secuencias de transformaciones geométricas:
– Una animación requiere que los objetos se trasladen y roten en cada fotograma
– Un diseño CAD requiere muchas transformaciones hasta obtener el resultado final
• Debemos formular de forma muy eficiente toda la secuencia de transformaciones, cada transformación puede representarse como P’ = P M1+ M2

 La matriz M1 contiene la información de ángulos y factores de escala
 La matriz M2 contiene los términos de traslación asociados al punto fijo y al centro de rotación

Para producir una secuencia de transformaciones hay que calcular las nuevas
coordenadas en cada transformación!
P’’ = P’ M3+ M4= … = P M1M3+ M2 M3+ M4<br>
<img width="640" height="355" alt="image" src="https://github.com/user-attachments/assets/58de7462-13e6-4a05-9bcc-e360f00a5fee" />
##
---
## Trazo de líneas curvas
El trazo de líneas curvas en graficación 2D, esencial para formas orgánicas y complejas, se basa en unir puntos de control, frecuentemente utilizando los principios de las curvas de Bézier. A diferencia de las líneas rectas, las curvas requieren definir puntos intermedios o nodos (inicial, final y puntos de control) para determinar la curvatura. Se pueden trazar mediante software (herramientas como Pluma o Bézier en aplicaciones) o técnicas manuales con regla.
<br><img width="259" height="194" alt="image" src="https://github.com/user-attachments/assets/eeba0011-f8ed-490a-96d4-129a1287f83f" />
##
---
## Bézier
Se denomina curvas de Bézier a un sistema que se desarrolló hacia los años 1960 para el trazado de dibujos técnicos, en el diseño aeronáutico y en el de automóviles. Su denominación es en honor a Pierre Bézier, quien ideó un método de descripción matemática de las curvas que se comenzó a utilizar con éxito en los programas de CAD.
Las curvas de Bézier fueron publicadas por primera vez en 1962 por el ingeniero francés, Pierre Bézier y posteriormente, trabajando en la Renault, las usó con abundancia en el diseño de las diferentes partes del automóvil. Las curvas fueron desarrolladas por Paul de Casteljau usando el algoritmo que lleva su nombre. Se trata de un método numéricamente estable para evaluar las curvas de Bézier.

Posteriormente, los inventores del PostScript, lenguaje que permitió el desarrollo de sistemas de impresión de alta calidad desde el ordenador, introdujeron en ese código el método de Bézier para la generación del código de las curvas y los trazados. El lenguaje PostScript sigue empleándose ampliamente y se ha convertido en un estándar de calidad universal; por ello, los programas de diseño vectorial como Adobe Illustrator, el extinto Macromedia FreeHand y Corel Draw, tres de los programas más importantes de dibujo vectorial y otros como Inkscape, denominan «bézier» a algunas de sus herramientas de dibujo, y se habla de «trazados bézier», «pluma bézier», «lápiz bézier», etc. Su facilidad de uso la ha estandarizado en el diseño gráfico, extendiéndose también a programas de animación vectorial, como Adobe Flash, y retoque fotográfico (bitmap), como Photoshop y Gimp, donde se usa para crear trazos, formas cerradas o selecciones.<br>
<img width="2048" height="1792" alt="image" src="https://github.com/user-attachments/assets/118d19c1-1730-4f5c-b855-82ad21c93008" />
##
---
##  B-spline
 Una curva B-spline se define como una curva polinómica por partes con soporte mínimo. La naturaleza por partes de una curva B-spline implica que su ecuación representativa es una combinación lineal de B-splines de grados específicos. Todas las curvas B-spline se construyen definiendo los siguientes elementos:<br>
 <br>Grado del polinomio : El usuario tiene libertad para determinar el grado del polinomio que se utilizará para interpolar sus datos a un modelo de curva B-spline. Un grado polinómico más alto generalmente proporciona resultados más precisos, aunque existe el riesgo de sobreajuste entre los puntos de datos cuando estos son escasos.
<br><br>Nudos : Son puntos a lo largo de una curva B-spline donde las secciones de la curva se unen y conectan. Todas las curvas B-spline tienen al menos dos nudos, que definen los puntos finales de la curva.
<br><br>Puntos de control : Los puntos de control son como los datos utilizados para la interpolación; determinarán la forma de la curva B-spline resultante y es posible que la curva no interseque con estos puntos.
<br><br>Funciones base : Se trata de funciones polinómicas que se suman de forma iterativa en cada sección de la curva. Los nodos definen dónde se activa una nueva función base y comienza a contribuir a la curvatura general de la curva B-spline.
<br><img width="960" height="720" alt="image" src="https://github.com/user-attachments/assets/3b9e53c7-4f0c-4ca2-870f-6948d7af9bc9" />
##
---
## Fractales
Un fractal es un objeto geométrico cuya estructura básica, fragmentada o irregular, se repite a diferentes escalas.[1] El término fue propuesto por el matemático Benoît Mandelbrot en 1975 y deriva del Latín fractus, que significa quebrado o fracturado. Muchas estructuras naturales son de tipo fractal. La propiedad matemática clave de un objeto genuinamente fractal es que su dimensión métrica fractal es un número no entero.

Si bien el término "fractal" es reciente, los objetos hoy denominados fractales eran bien conocidos en matemáticas desde principios del siglo XX. Las maneras más comunes de determinar lo que hoy denominamos dimensión fractal fueron establecidas a principios del siglo XX en el seno de la teoría de la medida.
<br> 
<img width="306" height="165" alt="image" src="https://github.com/user-attachments/assets/30ed2035-a330-4815-a252-9afac06d7298" />
<br>
Es geometría que no distingue entre conjunto matemático y objeto natural. Este nuevo paradigma engulle paradigmas anteriores proyectando un modelo que inagura una nueva zona o región de lo real.

Tómese un número complejo, multiplíquese por sí mismo y súmese el número inical; tómese el resultado, multiplíquese por sí mismo, súmese el inicial... y así sucesivamente. A esta iteración en principio errática se le asignan puntos sobre un plano. Disponga papel, lápiz y moneda con cara y cruz, fijemos ciertas reglas para cada lanzamieno; por ejemplo desplazar el punto X centímetros al noreste si sale cara y acercarse un 50% al centro inicial si sale cruz. Se perfila, progresiva y sorprendentemente el dibujo de la hoja de helecho (véase fig. 1) mientras el ordenador hace esta tarea menos ardua en pantalla y en décimas de segundo.<br>
<img width="343" height="147" alt="image" src="https://github.com/user-attachments/assets/afa4818e-1273-4039-81ab-ca7ad9329f6d" />
##
---
## Uso y creación de fuentes de texto
El uso y creación de fuentes en graficación abarca la selección, diseño y renderización de caracteres digitales para asegurar legibilidad, estética y comunicación efectiva. Se basa en clasificaciones (Serif, Sans Serif, Manuscritas, Decorativas) y formatos (TTF, OTF) para estructurar información en plataformas digitales y físicas.
<br>el uso y creación de fuentes en graficaciónJerarquía y Estructura: Se utilizan tamaños y grosores (negrita/regular) para guiar la mirada y destacar información crucial.
<br>Legibilidad y Personalidad: Las fuentes sin serifa son ideales para pantallas, mientras que las decorativas se usan para impacto visual, cuidando no superar dos o tres familias para mantener la legibilidad.
<br>Parámetros Técnicos: Es esencial ajustar el kerning (espacio entre letras), interlineado y el alineado (generalmente a la izquierda en occidente) para evitar la fatiga visual.
<br>Optimización Digital: La tipografía debe adaptarse a diferentes resoluciones de pantalla y dispositivos para una experiencia de usuario consistente. 
<br>Creación de Fuentes de Texto (Tipografía Digital)
<br>Diseño Vectorial: Las fuentes se crean mediante vectores para permitir el escalado sin pérdida de calidad.
<br>Formatos Estándar:
<br>TTF (TrueType Font): Formato estándar, ideal para legibilidad en pantalla.
<br>OTF (OpenType Font): Basado en PostScript, ofrece capacidades avanzadas y mayor compatibilidad entre sistemas operativos.
<br>Proceso de Creación: Implica diseñar cada glifo (letra, número, símbolo), ajustar el espaciado (métricas) y generar el archivo final utilizando software especializado. 
<br> 

https://github.com/user-attachments/assets/124e3314-acd9-4309-86d8-d77dc3d39edc



https://github.com/user-attachments/assets/8fb0ab12-b450-4df2-a3ca-b833513bdee7



https://github.com/user-attachments/assets/fced8c07-fe63-4368-bf5a-eba9491470d8



https://github.com/user-attachments/assets/e0675fee-023c-431c-b6e9-b8ede5429dc2

<img width="900" height="600" alt="image" src="https://github.com/user-attachments/assets/ef9cffe3-c645-4e69-89c9-0a6c99dc906c" />
##
---
## Referencias
Lara, J. G. (s. f.). Conceptos de: graficación en 2D, transformación bidimensional, traslación, escalación, rotación y sesgado. https://javiergarcialara.blogspot.com/2017/03/conceptos-de-graficacion-en-2d.html<br>
Liz. (2019, 2 octubre). conceptos: traslación,rotación,escalacion,sesgado. https://lizethazucenavazquezvazquez.blogspot.com/2019/10/conceptos-traslacionrotacionescalacions.html<br>
Admin. (2021, 9 noviembre). Rotation. BYJUS. https://byjus.com/maths/rotation/<br>





