# Lab-instrumentaci-n-1
# Monitoreo del patrón y frecuencia respiratoria mediante capnografía
Presentado por: Jhonathan David Guevara
                Juan Pablo Díaz
                María Paula Fernández 
                
a.Introducción:
La frecuencia respiratoria (FR) es uno de los signos vitales fundamentales utilizados en la evaluación clínica del estado fisiológico de un paciente. Representa el número de ciclos respiratorios por minuto y refleja directamente la actividad del sistema respiratorio y el balance ácido-base del organismo. Alteraciones en la FR suelen ser uno de los primeros indicadores de deterioro clínico, incluso antes de cambios en la frecuencia cardíaca o la presión arterial .

En el ámbito hospitalario, la medición manual de la frecuencia respiratoria presenta baja confiabilidad debido a errores humanos, variabilidad del observador y monitoreo discontinuo. Por esta razón, en la ingeniería biomédica se han desarrollado sistemas automáticos de monitorización basados en sensores fisiológicos, entre ellos la capnografía, la cual permite evaluar la ventilación pulmonar mediante la medición del dióxido de carbono (CO₂) exhalado .

La capnografía no solo permite obtener la frecuencia respiratoria, sino también información sobre ventilación, perfusión y metabolismo. Debido a esto, se ha convertido en una herramienta esencial en anestesia, cuidados intensivos y monitoreo clínico continuo .

El objetivo del presente laboratorio fue caracterizar el funcionamiento de un sensor de capnografía con el fin de analizar la señal respiratoria obtenida y establecer las bases para la medición automática de la frecuencia respiratoria.

b.Objetivos:
Objetivo General: Evaluar la influencia del habla o verbalización sobre el
patrón respiratorio.
Objetivos Específicos
• Reconocer las variables físicas principalmente involucradas en el proceso
respiratorio.
• Desarrollar un sistema que extraiga el patrón respiratorio y la frecuencia
respiratoria.
• Identificar tareas de verbalización a partir del patrón y/o la frecuencia
respiratoria.

c.Marco teórico
Fisiología de la respiración

La respiración es el proceso fisiológico mediante el cual el organismo intercambia gases con el medio ambiente, permitiendo la entrada de oxígeno (O₂) y la eliminación de dióxido de carbono (CO₂). Este proceso comprende tres etapas: ventilación pulmonar, difusión alveolocapilar y transporte de gases en la sangre [1].

La ventilación pulmonar corresponde al movimiento mecánico del aire hacia dentro y fuera de los pulmones generado por la contracción del diafragma y los músculos intercostales. Durante la inspiración aumenta el volumen torácico y disminuye la presión intrapulmonar, permitiendo la entrada de aire; en la espiración ocurre el proceso inverso [2].

El intercambio gaseoso se realiza en los alvéolos pulmonares por difusión a favor del gradiente de presión parcial: el oxígeno difunde hacia la sangre y el CO₂ hacia el aire alveolar [1]. Posteriormente, el oxígeno es transportado principalmente unido a la hemoglobina, mientras el CO₂ se transporta mayoritariamente en forma de bicarbonato [2].

En adultos sanos en reposo, la frecuencia respiratoria normal se encuentra entre 12 y 20 respiraciones por minuto [3].

2.2 Control de la respiración

El ritmo respiratorio está controlado automáticamente por centros respiratorios localizados en el bulbo raquídeo y la protuberancia. Estos centros ajustan la ventilación en respuesta a cambios químicos en la sangre, principalmente la concentración de CO₂ y el pH [2].

Los quimiorreceptores centrales detectan variaciones del pH del líquido cefalorraquídeo, mientras los quimiorreceptores periféricos responden a disminuciones de la presión parcial de oxígeno arterial [1]. El principal estímulo respiratorio en condiciones normales es el aumento del CO₂ sanguíneo [2].

Aunque es un proceso automático, la respiración puede modificarse voluntariamente por control cortical durante actividades como el habla, canto o apnea voluntaria [4].

2.3 Mecánica y patrón respiratorio

El ciclo respiratorio consta de dos fases:

Inspiración: fase activa dependiente de la contracción muscular

Espiración: fase pasiva en reposo

En condiciones normales, la espiración dura ligeramente más que la inspiración. Sin embargo, durante la fonación la espiración se prolonga considerablemente para permitir la producción de sonido, modificando la regularidad del patrón respiratorio [4].

El patrón respiratorio puede caracterizarse mediante la frecuencia respiratoria, amplitud ventilatoria y relación inspiración-espiración [3].

2.4 Capnografía

La capnografía es una técnica de monitoreo no invasiva que mide la presión parcial o concentración de CO₂ en el aire espirado en función del tiempo [5]. El valor máximo al final de la espiración se denomina dióxido de carbono al final de la espiración (EtCO₂) y refleja indirectamente la ventilación alveolar [5].

El capnograma presenta cuatro fases:

Aire del espacio muerto sin CO₂

Mezcla de aire alveolar

Meseta alveolar

Inspiración con caída brusca del CO₂

Cada ciclo corresponde a una respiración, por lo que la frecuencia respiratoria puede calcularse contando los ciclos por unidad de tiempo [5].

2.5 Relación entre respiración y habla

Durante el reposo la respiración es automática y rítmica; sin embargo, durante el habla interviene el control voluntario cortical, el cual modifica la ventilación para producir fonación. Esto genera espiraciones prolongadas e inspiraciones rápidas, produciendo irregularidades en el patrón respiratorio [4].

Por ello, el análisis temporal de la señal capnográfica permite diferenciar estados fisiológicos como reposo y verbalización.


d.MATERIALES

Sensor de capnografía (CO₂)

Arduino LEONARDO

Protoboard y cables

Computador con MATLAB

Serial Plotter Arduino

e.Adquisición de la señal

El sensor de CO₂ se ubicó en ___ (cerca a nariz/boca) para capturar el aire espirado.

El sensor entrega un voltaje proporcional a la concentración de CO₂, el cual fue digitalizado mediante el ADC del Arduino y enviado por comunicación serial al computador.

- Visualización

Se verificó la señal utilizando el Serial Plotter en dos condiciones:

Reposo

Lectura en voz alta

- Adquisición en MATLAB

Se desarrolló un código para captura temporizada de 30 segundos.

Frecuencia de muestreo: ___ Hz

Se guardaron los archivos:

reposo.mat

habla.mat

-Procesamiento

Se aplicó un filtro pasa-bajas para eliminar ruido de alta frecuencia.

Frecuencia de corte: ___ Hz

Posteriormente se obtuvo el espectro mediante FFT para hallar la frecuencia dominante.

f.Resultados
g.Análisis de Resultados
h.Preguntas
i.Conclusiones
j.Referencias
