# Proyecto_Analisis-de-empresa-de-telecomunicaciones-ConnectaTel
Proyecto Bootcamp - TripleTen

## Objetivo

Entender cómo los clientes usan los servicios móviles (llamadas y mensajes) para identificar patrones de uso, detectar comportamientos atípicos y qué segmentos de clientes muestran necesidades diferenciadas, con el fin de optimizar la oferta comercial y mejorar la experiencia del usuario. 

## Herramientas 

* JUPYTER NOTEBOOK. 
* PHYTON (PANDAS, NUMPY, SEABORN, MATPLOTLIB).

## Preguntas clave

1. ¿Qué segmentos de clientes muestran mayor o menor uso de llamadas y mensajes?
   
2. ¿Qué usuarios presentan valores atípicos que puedan indicar comportamientos inusuales, fraude o errores de registro?
   
3. ¿Cómo varía el uso según la edad y el tipo de plan contratado?
   
4. ¿Qué patrones pueden ayudar a diseñar mejores planes, optimizar la oferta y mejorar la satisfacción del cliente?
  

## Metodología

* Explorar datos:
Cargar y explorar los datos para tener una visión de la estructura y tipo de columnas que se tienen en los Dataset. 

* Identificar problematicas:
Conteno de nulos, detección de sentinels e información general de los datos para priorizar problemas que pueden sesgar decisiones.

* Limpieza de datos: 
Tener datos consistentes y listos para realizar el ánalisis estadístico por medio de acciones como reemplazar sentinels, convertir fechas, imputar o marcar NA según reglas.

* Revisar estadísticas:
Revisar las medidas clave en variables categóricas y numéricas que muestran el comportamiento típico y extremo.

* Visualización & outliers:
Visualización de sesgos, patrones de usuarios o datos atípicos.

* Segmentación:
Crear segmentos accionables que permiten diseñar ofertas, campañas y migraciones de plan.

## Hallazgos y recomendaciones

#### Hallazgos iniciales:

- El grupo de jovenes es una oportunidad para la compañia, puesto que son los usuarios quienes utilizan menos el plan básico y premium.
  
- La mayoria de los usuarios son adultos, posteriormente quienes lo usan son los adultos mayores. 
  
- En los tres grupos de usuarios por edad prefieren utilizar el plan basico.
  
- Esto sugiere que la mayoria de los usuarios prefieren utilizar el plan basico. Por lo que se deben realizar acciones para que los usuarios prefieran utilizar el plan premium.

- Es importante mencionar que las filas en las cuales la fecha aparece con registro, es debido a que el usuario dejó de utilizar la línea, se puede interpretar como "bajas de usuarios". 

- Mientras que las lineas con nulos, son líneas que continuan en servicio. No se deberán imputar los datos puesto que se tendría un error al querer analizar las líneas activas y las líneas dadas de baja.

- Para el dataset  `users ` se tienen valores nulos en dos columnas:
  * Columna  `City `: se tienen 469 nulos del total de 4000 datos. Lo que representa un 11.72%.  
  * Columna  `churn_date `: tiene un total de 3534 valores nulos, lo que representa un 88.35% de datos faltantes. 

- En el dataset  `usage ` se tiene un total de 40000 datos, dentro de este existen 3 columnas con datos nulos.
  * Columna  `date `: se tiene un faltante de 50 datos, representan solo el 0.12% del total.
  * Columna  `duration `: tiene un faltante del 55.19% (22076 datos).
  * Columna `length `: se tiene un faltante total de 17896 datos, lo que representa un 44.74%.
  
#### Recomendaciones:

- Se recomienda revisar el costo del plan premium puesto que pocos usuarios tienen ese plan activado.
  
- Se sugiere tener en cuenta el total de uso que tiene cada plan para modificarlo y sea más remunerable para la compañia y usuarios.
  
- Se sugiere realizar alguna campaña para tener más uso del plan premium entre los jovenes. Para este segmento de usuarios al momento de contratar el plan se podría dar beneficios para el usuario.

Algunos podrian ser: el uso de redes sociales ilimitado, algun convenio con una app de reproducción de música, ciertos GB de internet para juegos y navegar o tener dinamicas de recompensa por el uso del paquete (obsequiar accesorios, juntar puntos para intercambio de regalos, descuentos y ofertas especiales).

- Para los adultos mayores que tienen menos uso del plan premium se puede hacer más atractivo dando beneficios en intercambio de puntos en cosas de interes como equipos o en compra de despensa. 


## Diccionario de datos
 
 #### *Usuarios:*

   * Nombre del dataset: users_latam.csv (4,000 filas)

   * Descripción: Información de cada usuario (datos personales, plan, fecha de registro, churn).

   * Campos

    * user_id — identificador único del usuario
    * first_name — nombre
    * last_name — apellido
    * age — edad
    * city — ciudad
    * reg_date — fecha de registro
    * plan — tipo de plan contratado
    * churn_date — fecha de baja (nulo si sigue activo)




#### *Plan:* 

 * Nombre del dataset: plans.csv (2 filas)

 * Descripción: atálogo de planes con sus precios y beneficios.

 * Campos

   * plan_name — nombre del plan (Basico / Premium)
   * messages_included — mensajes incluidos en el plan
   * gb_per_month — GB incluidos por mes
   * minutes_included — minutos incluidos en el plan
   * usd_monthly_pay — costo mensual en USD
   * usd_per_gb — costo por GB extra
   * usd_per_message — costo por mensaje extra
   * usd_per_minute — costo por minuto extra


#### *Actividad del usuario:* 

 * Nombre del dataset: usage.csv (40,000 filas)

 * Descripción: Actividad generada por los usuarios: llamadas, mensajes, duración, longitud. 

 * Campos

   * id — identificador del registro
   * user_id — identificador del usuario
   * type — tipo de uso (call o text)
   * date — fecha del uso
   * duration — duración en minutos (solo llamadas)
   * length — longitud en caracteres (solo mensajes)


