# MaquinaVectorSoporte
Las máquinas de soporte vectorial es un algoritmo de aprendizaje supervisado. Estos métodos están propiamente relacionados con problemas de clasificación y regresión. Dado un conjunto de ejemplos de entrenamiento (de muestras) podemos etiquetar las clases y entrenar una SVM para construir un modelo que prediga la clase de una nueva muestra.

# La aplicacion
En el ejemplo tenemos un conjunto de puntos con su correspondiente clase, en el grafico podemos apreciar su ubicación y su clase con los colores rojo y azul.

| x1        | x2          | Class  |
| :-------: |:-----------:| :-----:|
|1|1|1|
|-1|2|1|
|-1|0|-1|
|0|-1|-1|

![alt text](https://github.com/nicoangelico/MaquinaVectorSoporte/blob/master/graficoPuntos1.png "Patrones de entrada")

A continuación generamos el string de maximización, el cual está diseñado para ser utilizado en wolframalpha (www. Wolframalpha.com), aunque la versión gratuita NO nos permite ingresar un string de gran tamaño. 

maximize {-1/2*(+u^2*2.0 +u*v*1.0 +u*w*2.0+u*z*-1.0 +v*u*1.0+v^2*5.0 +v*w*4.0+v*x*3.0 +v*y*-3.0+v*z*4.0 +w*u*2.0+w*v*4.0 +w^2*4.0+w*x*2.0 +w*y*-2.0+w*z*2.0 +x*v*3.0+x*w*2.0 +x^2*2.0+x*y*-2.0 +x*z*3.0+y*v*-3.0 +y*w*-2.0+y*x*-2.0 +y^2*2.0+y*z*-3.0 +z*u*-1.0 +z*v*4.0 +z*w*2.0 +z*x*3.0+z*y*-3.0+z^2*5.)+z+y+x+w+v+u} on +z+y+x-w-v-u = 0 and z>=0 and y>=0 and x>=0 and w>=0 and v>=0 and u>=0

Una vez que corremos el wolframalpha, nos arrojara los resultados de los alfas.
(w,x,y,z) = (1/4, 3/8, 5/8, 0)

Luego utilizando el algoritmo de MVS obtenemos la recta que mejor separa (clasifica) a los patrones de entrada como se muestra en la figura.

![alt text](https://github.com/nicoangelico/MaquinaVectorSoporte/blob/master/graficoPuntos2.png "Patrones de entrada")
