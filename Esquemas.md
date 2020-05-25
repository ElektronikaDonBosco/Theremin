# Oscilador de Referencia

Este es el esquema que hemos utilizado para el oscilador de referencia.

Lo primero que hicimos fue crear el esquema en el programa proteus, una vez hecho el esquema y habiendo simulado continuamos llevando el esquema a la máquina LPKF para poder imprimir la placa. Testeamos para comprobar si la placa está bien hecha y después de comprobar empezamos a poner los componentes en la placa. Ya con los componentes solo teníamos que soldarlos a la placa y comprobar con el osciloscopio si funcionaba correctamente y oscilaba a la frecuencia necesaria.


El oscilador de referencia oscila alrededor de 172 kHz, con el trimmer y el potenciómetro de 10k lo ajustamos a la frecuencia correcta. Un pequeño inductor de núcleo de ferrita y varios condensadores forman el “circuito tanque”. La señal de salida de 172 kHz de este oscilador irá al circuito mezclador donde se mezclará con la señal del circuito oscilador de tono.

# Oscilador de tono

Este es el esquema que hemos utilizado para el oscilador de tono.

Hicimos lo mismo que con el oscilador de referencia, al principio creamos el esquema en el programa proteus, luego lo imprimimos en la máquina LPKF y finalmente quitando los problemas de soldadura y cambiando algún componente conseguimos hacer que oscilase correctamente.
  

El oscilador variable de tono también funciona a 172 kHz y está influenciado por la capacitancia parásita asociada con la antena de tono. El propósito de los cuatro inductores de ferrita de 10 mH es mejorar la linealidad de la relación entre la posición de la mano y el tono de el que lo toca. Sin estos componentes, el tono de Theremin se elevaría lentamente al principio y luego se elevaría repentinamente a través de varias octavas en solo unos pocos milímetros de movimiento de la mano, haciendo que el instrumento sea difícil de tocar. Como estos inductores forman un circuito resonante en serie con capacitancia parásita asociada con la antena, es difícil predecir sus valores óptimos. El valor de estos componentes se ajusta mejor mediante prueba y error para lograr la mejor relación movimiento de la mano. La salida de este oscilador también se alimenta al módulo mezclador utilizando una longitud de cable apantallado.

# Oscilador de volumen

El oscilador de volumen opera cerca de 441 kHz y ésta se varía mediante la antena de volumen. Cuando se sintoniza correctamente y acercamos la mano hacia la antena sin llegar a tocarla, la frecuencia de este oscilador coincidirá con la sintonización del circuito resonante de volumen. Esta condición hace que la señal máxima aparezca en el circuito sintonizado y corresponde al corte de audio. El potenciómetro de ajuste de 10k le permite al operador ajustar el oscilador a la frecuencia correcta. 

# Mezclador


El mezclador es el módulo más simple de ensamblar y no requiere ajuste. Su función es mezclar las señales de los dos osciladores de tono para producir una señal de audio. Como el mezclador se alimenta con las dos frecuencias de oscilador ligeramente diferentes, como resultado produce una forma de onda compleja en su salida. Si se analizará la forma de onda de salida, se vería que en realidad contiene dos frecuencias, una equivalente a la suma de las frecuencias de entrada y la otra equivalente a la resta (o diferencia) de las dos frecuencias de entrada. Como el primero sería inaudible e inútil para nuestro propósito, utilizamos un filtro de paso bajo (dos condensadores de 0.0047uF y una resistencia de 1k vease anexo 2 y 3 respectivamente) para extraer el último que estará en el rango audible. 




