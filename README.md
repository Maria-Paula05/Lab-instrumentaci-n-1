# Laboratorio Numero 1 Instrumentación Biomédica y Biosensores
# Monitoreo del patrón y frecuencia respiratoria mediante capnografía
Presentado por: Jhonathan David Guevara,
                ,Juan Pablo Díaz
                ,María Paula Fernández 
                
a.Introducción:

La frecuencia respiratoria (FR) es uno de los signos vitales fundamentales utilizados en la evaluación clínica del estado fisiológico de un paciente. Representa el número de ciclos respiratorios por minuto y refleja directamente la actividad del sistema respiratorio y el balance ácido-base del organismo. Alteraciones en la FR suelen ser uno de los primeros indicadores de deterioro clínico, incluso antes de cambios en la frecuencia cardíaca o la presión arterial .

En el ámbito hospitalario, la medición manual de la frecuencia respiratoria presenta baja confiabilidad debido a errores humanos, variabilidad del observador y monitoreo discontinuo. Por esta razón, en la ingeniería biomédica se han desarrollado sistemas automáticos de monitorización basados en sensores fisiológicos, entre ellos la capnografía, la cual permite evaluar la ventilación pulmonar mediante la medición del dióxido de carbono (CO₂) exhalado .

La capnografía no solo permite obtener la frecuencia respiratoria, sino también información sobre ventilación, perfusión y metabolismo. Debido a esto, se ha convertido en una herramienta esencial en anestesia, cuidados intensivos y monitoreo clínico continuo .

El objetivo del presente laboratorio fue caracterizar el funcionamiento de un sensor de capnografía con el fin de analizar la señal respiratoria obtenida y establecer las bases para la medición automática de la frecuencia respiratoria.

b.Objetivos:

Objetivo General: 

Evaluar la influencia del habla o verbalización sobre el
patrón respiratorio.

Objetivos Específicos

• Reconocer las variables físicas principalmente involucradas en el proceso
respiratorio.

• Desarrollar un sistema que extraiga el patrón respiratorio y la frecuencia
respiratoria.

• Identificar tareas de verbalización a partir del patrón y/o la frecuencia
respiratoria.

c.Marco teórico

•Fisiología de la respiración

La respiración es el proceso fisiológico mediante el cual el organismo intercambia gases con el medio ambiente, permitiendo la entrada de oxígeno (O₂) y la eliminación de dióxido de carbono (CO₂). Este proceso comprende tres etapas: ventilación pulmonar, difusión alveolocapilar y transporte de gases en la sangre [1].

La ventilación pulmonar corresponde al movimiento mecánico del aire hacia dentro y fuera de los pulmones generado por la contracción del diafragma y los músculos intercostales. Durante la inspiración aumenta el volumen torácico y disminuye la presión intrapulmonar, permitiendo la entrada de aire; en la espiración ocurre el proceso inverso [2].

El intercambio gaseoso se realiza en los alvéolos pulmonares por difusión a favor del gradiente de presión parcial: el oxígeno difunde hacia la sangre y el CO₂ hacia el aire alveolar [1]. Posteriormente, el oxígeno es transportado principalmente unido a la hemoglobina, mientras el CO₂ se transporta mayoritariamente en forma de bicarbonato [2].

En adultos sanos en reposo, la frecuencia respiratoria normal se encuentra entre 12 y 20 respiraciones por minuto [3].

•Control de la respiración

El ritmo respiratorio está controlado automáticamente por centros respiratorios localizados en el bulbo raquídeo y la protuberancia. Estos centros ajustan la ventilación en respuesta a cambios químicos en la sangre, principalmente la concentración de CO₂ y el pH [2].

Los quimiorreceptores centrales detectan variaciones del pH del líquido cefalorraquídeo, mientras los quimiorreceptores periféricos responden a disminuciones de la presión parcial de oxígeno arterial [1]. El principal estímulo respiratorio en condiciones normales es el aumento del CO₂ sanguíneo [2].

Aunque es un proceso automático, la respiración puede modificarse voluntariamente por control cortical durante actividades como el habla, canto o apnea voluntaria [4].

•Mecánica y patrón respiratorio

El ciclo respiratorio consta de dos fases:

Inspiración: fase activa dependiente de la contracción muscular

Espiración: fase pasiva en reposo

En condiciones normales, la espiración dura ligeramente más que la inspiración. Sin embargo, durante la fonación la espiración se prolonga considerablemente para permitir la producción de sonido, modificando la regularidad del patrón respiratorio [4].

El patrón respiratorio puede caracterizarse mediante la frecuencia respiratoria, amplitud ventilatoria y relación inspiración-espiración [3].

•Capnografía

La capnografía es una técnica de monitoreo no invasiva que mide la presión parcial o concentración de CO₂ en el aire espirado en función del tiempo [5]. El valor máximo al final de la espiración se denomina dióxido de carbono al final de la espiración (EtCO₂) y refleja indirectamente la ventilación alveolar [5].

El capnograma presenta cuatro fases:

1.Aire del espacio muerto sin CO₂

2.Mezcla de aire alveolar

3.Meseta alveolar

4.Inspiración con caída brusca del CO₂

Cada ciclo corresponde a una respiración, por lo que la frecuencia respiratoria puede calcularse contando los ciclos por unidad de tiempo [5].

•Relación entre respiración y habla

Durante el reposo la respiración es automática y rítmica; sin embargo, durante el habla interviene el control voluntario cortical, el cual modifica la ventilación para producir fonación. Esto genera espiraciones prolongadas e inspiraciones rápidas, produciendo irregularidades en el patrón respiratorio [4].

Por ello, el análisis temporal de la señal capnográfica permite diferenciar estados fisiológicos como reposo y verbalización.


d.Materiales

•Sensor de capnografía (CO₂)

•Arduino UNO

•Protoboard y cables

•Computador con MATLAB

•Serial Plotter Arduino

e.Adquisición de la señal

El sensor de CO₂ se ubicó en una mascarilla de nebulización pediátrica (cerca a nariz/boca) para capturar el aire espirado.
<img width="1200" height="1600" alt="image" src="https://github.com/user-attachments/assets/7cb38f12-a0be-430a-8295-4f74ea02ebc1" />
Figura 1: circuito que adquiere señal capnográfica

El sensor entrega un voltaje proporcional a la concentración de CO₂, el cual fue digitalizado mediante el ADC del Arduino y enviado por comunicación serial al computador.

- Visualización

Se verificó la señal utilizando el Serial Plotter en dos condiciones:

•Reposo

•Lectura en voz alta/charla

- Adquisición en MATLAB

Se desarrolló un código para captura temporizada de 60 segundos.

Frecuencia de muestreo: 100 Hz

Se guardaron los archivos:

reposo.mat

habla.mat

f.Resultados:

Para la evaluación del sistema se adquirieron señales capnográficas durante 60 segundos en dos condiciones fisiológicas:

•Respiración en reposo

•Respiración durante lectura en voz alta/charla

Las señales obtenidas fueron procesadas en MATLAB para su visualización en el dominio del tiempo y de la frecuencia.

•Señal respiratoria en reposo
<img width="1391" height="790" alt="image" src="https://github.com/user-attachments/assets/4b0ad83b-abfe-4e73-b335-a0ec1cd33121" />

Figura 2. Señal capnográfica en reposo

En la señal se observan ciclos respiratorios periódicos correspondientes a la ventilación automática.
El periodo promedio entre ciclos fue de:

T reposo =    s

Por tanto la frecuencia respiratoria calculada fue de:

FR reposo= 60/T reposo=       respiraciones/min

•Señal respiratoria durante verbalización

<img width="1373" height="815" alt="image" src="https://github.com/user-attachments/assets/311c4dbc-eb18-4062-9b76-8f347b8fea58" />

Figura 3. Señal capnográfica durante habla.
Se observan variaciones en la amplitud y periodicidad asociadas al control voluntario de la espiración durante la fonación.

El periodo promedio fue:

T habla =       s

FR habla=60/Thabla=                respiraciones/min

Dominio de la frecuencia
<img width="1367" height="740" alt="image" src="https://github.com/user-attachments/assets/55894cef-0e9b-4f6e-8042-8fc4f19a1a96" />

Figura 4. Espectro de frecuencia durante reposo

g.Análisis de Resultados

El sistema implementado permitió adquirir la señal capnográfica bajo dos condiciones fisiológicas: respiración en reposo y durante verbalización. La señal obtenida representa la variación de la concentración de CO₂ espirado a lo largo del tiempo, por lo que cada ciclo corresponde a una respiración.

En condición de reposo se espera un patrón respiratorio relativamente periódico, con ciclos regulares debido al control automático ejercido por los centros respiratorios del bulbo raquídeo. En este estado la ventilación responde principalmente a la regulación química del CO₂ sanguíneo, manteniendo una frecuencia respiratoria estable.

Durante la verbalización el patrón respiratorio cambia notablemente, ya que la respiración deja de ser completamente automática y pasa a estar parcialmente controlada por el sistema nervioso central superior (control cortical). La producción de voz requiere prolongar la espiración para permitir la fonación, generando inspiraciones más rápidas e irregulares. Como consecuencia, la señal presenta variaciones en amplitud, duración de los ciclos y periodicidad.

Adicionalmente, en el dominio de la frecuencia se espera observar que la señal en reposo presenta un pico dominante claramente definido, mientras que durante el habla el espectro se dispersa debido a la irregularidad temporal del patrón ventilatorio.

El sistema construido permite estimar la frecuencia respiratoria de manera adecuada; sin embargo, su precisión depende de la correcta ubicación del sensor y de la reducción de artefactos por movimiento o ruido ambiental.

h.Preguntas

1.¿Son los patrones respiratorios y frecuencias respiratorias iguales o diferentes en cada caso? ¿A qué se debe esto?

Los patrones respiratorios y la frecuencia respiratoria son diferentes entre reposo y verbalización.

En reposo la respiración es automática y rítmica, regulada por los centros respiratorios del tronco encefálico en respuesta a la concentración de CO₂ en sangre, por lo que el patrón presenta periodicidad constante.

Durante el habla la respiración se vuelve parcialmente voluntaria debido al control cortical necesario para la fonación. La espiración se prolonga para producir sonido y la inspiración se realiza de manera rápida y variable. Esto produce irregularidades en el patrón respiratorio y cambios en la frecuencia respiratoria.

Por tanto, la diferencia se debe a que la respiración pasa de un control químico automático a un control neuromuscular voluntario.

2.¿Cuáles serían las ventajas y desventajas de emplear múltiples sensores para el monitoreo del proceso respiratorio?

•Ventajas

-Mayor precisión en la medición

-Reducción de ruido y artefactos

-Posibilidad de medir varias variables fisiológicas simultáneamente (flujo, volumen, CO₂, movimiento torácico)

-Mayor confiabilidad del sistema mediante redundancia

-Detección más temprana de alteraciones respiratorias

•Desventajas

-Mayor costo del sistema

-Mayor complejidad electrónica y computacional

-Mayor incomodidad para el paciente

-Mayor consumo energético

-Mayor dificultad de calibración

•Razón fisiológica

Cada sensor mide una variable diferente del proceso respiratorio (ventilación mecánica, intercambio gaseoso o movimiento torácico). La respiración es un fenómeno multifactorial, por lo que un solo sensor no describe completamente el estado respiratorio; sin embargo, integrar varios sensores aumenta la exactitud a costa de complejidad.

i.Conclusiones

•La señal capnográfica permite identificar el ciclo respiratorio porque el CO₂ espirado refleja directamente la ventilación alveolar, la cual depende del intercambio gaseoso pulmonar.

•En reposo el patrón respiratorio es regular debido al control automático de los centros respiratorios bulbares regulados principalmente por la concentración de CO₂ sanguíneo.

•Durante la verbalización la respiración se altera fisiológicamente, ya que el control cortical voluntario prolonga la espiración para la fonación, generando irregularidad en el patrón y cambios en la frecuencia respiratoria.

•La medición de CO₂ espirado constituye una variable adecuada para el monitoreo respiratorio porque se relaciona directamente con la ventilación pulmonar y el equilibrio ácido-base.

•El sistema implementado permite estimar la frecuencia respiratoria, aunque su exactitud depende de la correcta adquisición de la señal y de la reducción de artefactos externos.

j.Referencias

[1] J. E. Hall, Guyton and Hall Textbook of Medical Physiology, 14th ed. Elsevier, 2021.
https://www.ncbi.nlm.nih.gov/books/NBK541028/

[2] B. R. West, Respiratory Physiology: The Essentials, 10th ed. Wolters Kluwer, 2016.
https://www.ncbi.nlm.nih.gov/books/NBK482268/

[3] Cleveland Clinic, “Respiratory Rate.”
https://my.clevelandclinic.org/health/articles/10881-vital-signs

[4] Kent, R. D., “Speech breathing physiology.”
https://www.ncbi.nlm.nih.gov/books/NBK279539/

[5] StatPearls, “Capnography.”
https://www.ncbi.nlm.nih.gov/books/NBK539754/
