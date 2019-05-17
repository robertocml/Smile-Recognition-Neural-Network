# Smile Recognition: Deep Learning Neural Network Application.

En este proyecto se desarrolló  una red neuronal de 4 capas como proyecto final del curso 'Deep Learning' en el Tecnológico de Monterrey Campus Monterrey. El objetivo principal de la red es clasificar una imagen como “0” en caso de que la persona no esté sonriendo o  “1” en caso de que la persona este sonriendo.


Para la realización de esta red se utilizó un dataset obtenido de kaggle, puedes revisarlo aquí:

https://www.kaggle.com/iarunava/happy-house-dataset/


## Instalación
Para correr este proyecto en tu ordenador necesitas:

-	Python3
-	Jupyter Notebook

Dicho software viene incluido en Anaconda, así que bastará con que instales y ejecutes Jupyter Notebook desde la GUI de Anaconda.
Aquí el link de descarga de anaconda: https://www.anaconda.com/distribution/

Una vez instalado y abierto Jupyter Notebook, bastara con abrir desde Jupyter el archivo llamado Proyecto_Final.ipynb

## Como funciona nuestra red? 

Nuestro dataset contiene imagenes de 64x64 pixels (usamos esa baja resolucion dado a la complejidad computacional de las operacions matriciales que necesitabamos ejecutar).
Inicialmente guardamos la informacion RGB de la imagen en un vecotr, el cual será el input que recibira nuestra red.
Asi que la capa inical nos quedaria de 64x64x3 = 12,288 neuronas de entrada.
Una vez procesado el vector inicial, pasamos por otras 3 capas escondidas antes de llegar a la capa de salida.
Aqui una imagen para explicar más gráficamente lo que esta sucediendo en nuestra red.

![Captura1](https://user-images.githubusercontent.com/12022308/57941118-a8430180-7893-11e9-9d1b-f5f2d6c3096b.PNG)

Entonces el modelo de la red, se vería masomenos así

![Captura2](https://user-images.githubusercontent.com/12022308/57942364-e1c93c00-7896-11e9-8f21-684edfabbb5a.PNG)


## Modificaciones a los hiper parametros

Se realizaron de forma sistematica bastantes (tal vez demasiadas jaja) pruebas a cada hiper-parametro. Al final concluimos que la mejor configuración para nuestra red fue la siguiente:

- Learning rate (Con un valor de 0.0075)
- Numero de capas (4 Capas)
- Numero de Iteraciones (2700)
- Funciones de activacion (Hidden layers y Output layer) (Linear, Relu y Sigmoid).



## Resultados Obtenidos.

Despues de estar configurando la red, llegamos a una exactitud del 97% en la clasificacion de las imagenes, lo cual es bastante bueno.
En las siguientes imagenes se puede observar como baja el costo logrando un 99% en la exactitud del train set y un 97% en el test set.
Comparado con los expected output inciales que teniamos, son excelentes resultados!

![Captura3](https://user-images.githubusercontent.com/12022308/57942528-4d130e00-7897-11e9-8896-cc9729c75faa.PNG)

![Captura4](https://user-images.githubusercontent.com/12022308/57942534-52705880-7897-11e9-8b11-33dbda650a80.PNG)


## Imagenes mal clasificadas... Porque?
![Captura5](https://user-images.githubusercontent.com/12022308/57942680-babf3a00-7897-11e9-98cc-62429430aaf3.PNG)

Algunos de los motivos por los cuales se obtuvieron clasificaciones erróneas son los siguientes:
 - La persona sonríe de manera inusual (boca muy abierta)
 - El ángulo de la foto no es el correcto (de frente)
 - La foto esta muy oscura
 - La postura no es muy natural
Sin embargo en general se obtuvo un excelente resultado, ya que fueron muy pocas las imágenes que se clasificaron de manera incorrecta








