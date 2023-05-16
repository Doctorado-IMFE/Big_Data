# Proyecto de evaluación

---

![Logo de la Institución](http://www.imfe.mx/inicio/wp-content/uploads/2020/05/logo_imfe.jpg)

---

## Autor: Juan Carlos González Ibarra
## Correo Institucional: juan.gonzalez.dti@imfe.mx

---

## Fecha: 15 de mayo, 2023

---

## Contenido

1. Introducción
2. Objetivo
3. Descripción de los datos
4. Análisis exploratorio
5. Desarrollo
6. Resultados
7. Conclusión
8. Bibliografía

---


# 1. Introducción

La tecnología está presente cada vez más en nuestras vidas, podemos notarlo de tal forma que nuestras actividades diarias están vinculadas a compartir información por medios digitales, sin duda esto hace que la información recolectada por estos medios digitales sea visualizada como una herramienta en la toma de decisiones y/o en la solución de problemas. Esta información para poder ser utilizada con estos propósitos previamente debe haber pasado por un proceso de análisis; este proceso de análisis ya tiene una base científica y aplicativa llamada ciencia de datos. La ciencia de datos conlleva una serie de etapas para el análisis de la información como: el entendimiento de los datos, la extracción de sus propiedades, el modelado y análisis del problema, la presentación de resultados y el desarrollo de software para explotar el conocimiento extraído. La **Ciencia de Datos** proporciona las herramientas y en ayuda del **Big Data** provee nuevas oportunidades tecnológicas para análisis masivos de información, por lo que las Tecnologías Big Data ayudan a mejorar la eficiencia, calidad y los productos y servicios personalizados ofrecidos por las organizaciones y a integrar datos estructurados y no estructurados con respuestas en tiempo real, abriendo nuevos caminos a la innovación y desarrollo.

Por lo que el **Big Data** se refiere al manejo y análisis de enormes volúmenes de datos que no pueden ser procesados de manera efectiva con las técnicas tradicionales debido a su volumen, velocidad y variedad. Los datos pueden provenir de varias fuentes, como transacciones comerciales, sensores de IoT, redes sociales, datos de salud, etc. Las técnicas de Big Data permiten descubrir patrones ocultos, correlaciones y otras ideas útiles que pueden informar la toma de decisiones empresariales y estratégicas.

Por lo que para realizar este análisis masivo de datos se debe identificar patrones que ayuden a la toma de decisiones tenemos que llevar acabo el **Análisis Exploratorio de Datos (AED)**.

## 1.1 Análisis Exploratorio de Datos
Se utiliza para analizar e investigar conjuntos de datos y resumir sus características principales, a menudo empleando métodos de visualización de datos que ayuda a entender la estructura de estos. Es un paso crucial antes de realizar modelos más complejos ya que ayuda a gestionar las fuentes de datos, descubrir patrones, detectar anomalías, probar una hipótesis, identificar relaciones y tendencias, etc.

<img src="https://datos.gob.es/sites/default/files/u322/grafico-guia_0.jpg" width="600" height="400">

El **AED** es un paso esencial en cualquier flujo de trabajo de **análisis de datos**, implica el uso de algoritmos de muestreo y agregación para reducir la escala de los datos a un tamaño manejable, y luego explorar estos datos resumidos para obtener insights. 
 
Source: https://www.ibm.com/mx-es/topics/exploratory-data-analysis


## 1.2 Metodología en el Análisis de Datos
  
Para establecer una metodología en el análisis de datos, debemos definir que el análisis de datos es el proceso de convertir datos sin procesar en información práctica e incluye una serie de herramientas, tecnologías y procesos para encontrar tendencias y resolver problemas mediante datos.

Source: https://aws.amazon.com/es/what-is/data-analytics/

<img src="https://actions.es/wp-content/uploads/2020/08/datos1-1.jpg" width="600" height="400">


# 2. Objetivo del Proyecto
El objetivo es analizar los datos y obtener información valiosa que permita a la compañía mejorar su estrategia de ventas y aumentar su rentabilidad.


# 3. Descripción de los datos

En este proyecto se cuenta con un conjunto de datos de Instacart Market Basket Analysis, que se encuentra en varios archivos CSV. 


<small> La información que contiene los archivos CSV es la siguiente:

• **orders.csv** : Contiene información de los pedidos realizados por los usuarios.
Cada fila representa un pedido y contiene la siguiente información:
- **order_id** : ID del pedido.
- **user_id** : ID del usuario que realizó el pedido.
- **order_number**: Número de pedido para cada usuario (1 = primer pedido, 2 =
segundo pedido, etc.).
- **order_dow** : Día de la semana en que se realizó el pedido.
- **order_hour_of_day** : Hora del día en que se realizó el pedido.
- **days_since_prior_order** : Días transcurridos desde el último pedido del
usuario.

• **order_products__prior.csv**: Contiene información de los productos comprados en
cada pedido. Cada fila representa un producto en un pedido y contiene la
siguiente información:
- **order_id** : ID del pedido.
- **product_id** : ID del producto comprado.
- **add_to_cart_order** : Orden en el que se agregó el producto al carrito en el
momento del pedido.
- **reordered** : Indica si el producto ha sido ordenado por el usuario
anteriormente.    

• **products.csv** : Contiene información de los productos vendidos en la tienda. Cada
fila representa un producto y contiene la siguiente información:
- **product_id** : ID del producto.
- **product_name** : Nombre del producto.
- **aisle_id**: ID del pasillo donde se encuentra el producto.
- **department_id** : ID del departamento al que pertenece el producto.

• **aisles.csv** : Contiene información de los pasillos de la tienda. Cada fila representa
un pasillo y contiene la siguiente información:
- **aisle_id** : ID del pasillo.
- **aisle** : Nombre del pasillo.

• **departments.csv** : Contiene información de los departamentos de la tienda. Cada
fila representa un departamento y contiene la siguiente información:
- **department_id** : ID del departamento.
- **department** : Nombre del departamento.    

</small>

Diagrama Entidad Relacion
<img src="/img/Proyecto_Final.png" width="600" height="400">


# 4. Análisis exploratorio

En el análisis exploratorio se analizan los archivos con la información proporcionada en la sección anterior, el propósito es analizar e investigar los conjuntos de datos, resumir sus características principales, detectar anomalías, identificar relaciones, eliminar variables irrelevantes, imputar valores faltantes y limpiar los nombres de los productos.

Se definen las tareas a realizar: 

1. Realizar un análisis exploratorio de los datos para entender la distribución de los pedidos, la cantidad de productos por pedido y la frecuencia de compras por día y hora. 
2. Identificar los productos más vendidos en la tienda y visualizar los resultados utilizando un gráfico de barras. 
3. Identificar los productos más comprados en cada departamento y visualizar los resultados utilizando un gráfico de barras. 
4. Identificar los productos que más se compran juntos, es decir, aquellos que aparecen en los mismos pedidos con mayor frecuencia, y visualizar los resultados utilizando un gráfico de red. 


En base a las tareas que se define y al analisis exploratorio se realizaran las siguientes acciones:

- **No ocupar la tabla aisles**.

- Eliminar los siguientes atributos:
- - **eval_set** de la tabla **orders**: Este atributo indica a cuál conjunto de datos (entrenamiento, prueba, etc.) pertenece cada pedido, pero no se usa en este análisis.
- - **days_since_prior_order** de la tabla **orders**: Este atributo indica cuántos días han pasado desde el último pedido del mismo usuario, pero no se usa en este análisis.
- - **aisle** de la tabla **products**: Este atributo indica el pasillo en el que se encuentra cada producto, pero no se usa en este análisis.
- - **reordered** de la tabla **order_products**: Este atributo indica si el producto fue reordenado por el mismo usuario, pero no se usa en este análisis.

- Imputar valores faltantes y limpiar los nombres de los productos.

- Se van a eliminar los espacios en blanco despues del nombre del producto.

- Se van a convertir a minusculas el nombre del producto.


# 5. Desarrollo

Para el desarrollo se va trabajar cada tarea de la siguiente forma:
1. Preprocesar los datos eliminando variables irrelevantes, imputando valores faltantes y limpiando los nombres de los productos.
2. Realizar un análisis exploratorio de los datos para entender la distribución de los pedidos.
- Visualización cantidad de productos por pedido
- Visualización frecuencia de compras por día
- Visualización frecuencia de compras por hora.
3. Identificar los productos más vendidos en la tienda y visualizar los resultados utilizando un gráfico de barras.
4. Identificar los productos más comprados en cada departamento y visualizar los resultados utilizando un gráfico de barras.
5. Identificar los productos que más se compran juntos, es decir, aquellos que aparecen en los mismos pedidos con mayor frecuencia, y visualizar los resultados utilizando un gráfico de red.


## Se ejecutan los archivos ADE para las pruebas de Python con Pandas

## Se ejecutan los archivos ADESpark para las pruebas de Spark


# 6. Resultados

Para las solicitudes de análisis en Pandas implemente el archivo ADE.ipynb.
Para las solicitudes de análisis en Spark implemente el archivo ADESpark.ipynb en:


### **Evaluacion eficencia Python con Pandas.**
#### **Se realizaron pruebas en:**

| Sistema Operativo | Tiempo de ejecucion | Uso de CPU    | Uso de memoria |
|-------------------|---------------------|---------------|----------------|
| Windows 10        | 112.2 segundos      | 26.8%         | 40.4%          |
| macOS Catalina    | 153.05 segundos     | 19.8%         | 37.3%          |
| Red Hat 9         | Error Kernel        | Error Kernel  | Error Kernel   |


<li><span style="color:red">El resultado de Red Hat de Python con Pandas se detuvo.</span></li>


### **Evaluacion eficencia Spark.**
#### **Se realizaron pruebas en:**

| Sistema Operativo | Tiempo de ejecucion | Uso de CPU    | Uso de memoria |
|-------------------|---------------------|---------------|----------------|
| Windows 10        | 86.69 segundos      | 75.7%         | 47.8%          |
| macOS Catalina    | 181.68 segundos     | 27.8%         | 51.9%          |
| Red Hat 9         | Aprox 120 segundos  | Aprox 36.66%  | Aprox 31%      |


<li><span style="color:red">El resultado de Red Hat con Spark fue aproximado.</span></li>
<li><span style="color:red">Solo genero una grafica y se paro el servicio.</span></li>
<li><span style="color:red">Posiblemente el error con Red Hat 9 se debio a su virtualización y restriccion en el tamaño del disco duro virtual con tenia 31 GB de espacio.</span></li>



### **Detalles tecnicos y Demostración de ejecución:**

### - Windows 10
- - Procesador i5 de 9th Generacion 2.30 GHz con 8 nucleos
- - Memoria RAM 32 GB
- - Disco Duro NVME de 1TB

#### Python con pandas Win 10
<img src="/img/rp_win.png" width="600" height="400">

#### Spark Win 10
<img src="/img/rs_win.png" width="600" height="400">


### - Osx Catalina
- - Procesador i5 de 5th Generacion 1.7 GHz con 2 nucleos
- - Memoria RAM 16 GB
- - Disco Duro SSD de 512GB

#### Python con pandas Osx Catalina
<img src="/img/rp_osx.png" width="600" height="400">

#### Spark Osx Catalina
<img src="/img/rs_osx.png" width="600" height="400">


### - Red Hat 9 (Maquina Virtual en Virtual Box)
- - Procesador i5 de 9th Generacion 2.30 GHz con 4 nucleos
- - Memoria RAM 8 GB
- - Disco Duro NVME de 31GB

#### Error en Python con pandas Red Hat 9
<img src="/img/rp_redh.png" width="600" height="400"> 

#### Spark Red Hat 9
<img src="/img/rs_redh.png" width="600" height="400">

#### Error en Spark Red Hat 9
<img src="/img/rs_redh-error.png" width="600" height="400">




# 7. Conclusión

El uso e implementación de técnicas de Big Data para el análisis de datos aporta al conocimiento teórico y técnico una comprensión del comportamiento de la información y el potencial que tiene para poder ayudar a la solución de problemas reales que tiene la sociedad y/o en la toma de decisiones dentro de empresas públicas y privadas, por lo que la información resulta ser invaluable para las empresas de cualquier sector productivo.

El desarrollo del análisis de datos de la información proporcionada, se tuvo en primer parte una visión global de los datos y la relación que tienen entre estos, lo que llevó a establecer el tipo de atributos que los relacionaban y el giro de servicios y/o productos que la empresa utiliza esta información. Así se tiene una comprensión más a detalle de las tareas que se van a desarrollar y los resultados que se pretenden obtener.

En el análisis de datos se establece una tienda de servicios de productos que están separados por departamentos y pasillos, también las órdenes de compra que nos dicen el cliente, la frecuencia y la cantidad de productos por cada orden de compra diaria, así se identifica los productos que se compran juntos, con más frecuencia por día o por hora y por departamento, con el resultado se puede ayudar a la empresas a desarrollar estrategias de venta cruzada más efectivas y a optimizar el diseño de sus tiendas, tanto físicas como en línea. Al mismo tiempo, conocer la frecuencia de las compras por día y hora puede ayudar a mejorar la gestión de inventario y la programación del personal, lo que a su vez puede conducir a una mayor eficiencia y ahorro de costos.

En la parte técnica del análisis de datos se utilizó las herramientas de Python con Pandas y Spark, ambas son herramientas para el manejo y análisis de datos, pero se utilizan de manera diferente dependiendo del tamaño de los datos y el entorno de procesamiento.

Por lo tanto, en la implementación de estas técnicas en este problema el uso de Python con Pandas tuvo como ventajas:

- Manipulación de datos sencilla.

- Análisis exploratorio de datos a pequeña y mediana escala

- Poder trabajar en un solo equipo de cómputo con requisitos técnicos mínimos.

Y como desventajas:

- La limitante de analizar conjuntos de datos masivos debido a las restricciones de memoria del equipo.

Por otra parte, Spark está diseñado para ser rápido y manejar grandes cantidades de datos distribuidos a través de nodos en un clúster, por lo que, lo hace más adecuado para conjuntos de datos muy grandes que no caben en la memoria del equipo y que se puede implementar en una infraestructura de cloud computing (Amazon, Azure, Google Cloud, etc.).

En la implementación de Spark en este problema tuvo ventajas:

- El tiempo de carga de datos fue más rápido.

- El análisis exploratorio mejora el rendimiento del procesador.

- El poder aumentar la cantidad de información para realmente visualizar su potencial.

Y como desventajas:

- Es complicado en su codificación, si no se tienen conocimientos previos del lenguaje de programación.

- La manipulación de datos es más compleja retomando lo dicho en el punto anterior.

- No se exploran métodos de ploteo o graficación.

- No se visualiza el rendimiento en recursos ya que todo se ejecutó en un solo equipo de cómputo.

En conclusión, el uso de Big Data y técnicas de análisis de datos (Python con Pandas y Spark) en este proyecto, ayuda a entender y clarificar el poder aplicativo como desarrollador de software en lo que es el proceso de análisis de información, y como una herramienta para la dirección de empresas (públicas, privadas, investigación, fundaciones, etc.,) en la toma de decisiones. Asi que el Big Data se posiciona como una de las áreas del conocimiento con más aplicación en el presente y como una base científica para futuras áreas de la inteligencia artificial como el Machine Learning.
Y en una ventaja para mi proyecto de investigación, ya que será la herramienta que me ayude a plantear y validar mi pregunta de investigación e hipótesis en mi proyecto de Doctorado en Tecnologías de la Información.


# 8. Bibliográfia

- Documentación oficial de Python: https://docs.python.org/3/
- Documentación oficial de Pandas: https://pandas.pydata.org/docs/
- Documentación oficial de Matplotlib: https://matplotlib.org/stable/contents.html
- Documentación oficial de Apache Spark: https://spark.apache.org/docs/latest/
- Analisis Exploratorio de Datos https://www.aprendemachinelearning.com/analisis-exploratorio-de-datos-pandas-python/
- Conceptos en Python https://www.geeksforgeeks.org
- Dudas https://stackoverflow.com/questions/tagged/pandas+python
- Analisis de datos https://ocw.uc3m.es/course/view.php?id=230
- Diccionarios de datos en data frame https://github.com/nsheikh23/COVID_StockMarket_Analysis/blob/master/52_Week.ipynb
- Procesamiento de data frames en pandas https://barcelonageeks.com/eliminar-una-o-varias-columnas-de-pyspark-dataframe/
- Data Clean https://github.com/mramshaw/Data-Cleaning
- Ploteo de datos https://github.com/tomimester/python-histogram/blob/master/plot-histogram-python-pandas.ipynb
- Creación de grafos con networkx https://ernestocrespo13.wordpress.com/2012/11/25/creacion-de-grafos-con-networkx-parte-1/
- Data Analysis Techniques with PySpark https://github.com/sedaatalay/Sample-Data-Analysis-Techniques-with-PySpark