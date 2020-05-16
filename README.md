## **ECOBICI DATA**

Este repositorio contiene trabajo realizado sobre datos abiertos del sistema público de *Bike Sharing* de la Ciudad Autónoma de Buenos Aires, concretamente sobre viajes en bicicletas de dicho sistemas, registrados desde 2010 hasta 2019.

Los datos estan disponibles [aquí](https://data.buenosaires.gob.ar/dataset/bicicletas-publicas)

Sumado a éstos, se utilizan otros datos sobre las estaciones de biciletas públicas, disponibles [aquí](https://data.buenosaires.gob.ar/dataset/estaciones-bicicletas-publicas)

### **Entorno de trabajo**
Los datos se han procesado principalmente con PySpark, trabajando sobre una imágen de docker con todo lo necesario para trabajar.
[Aquí](https://jupyter-docker-stacks.readthedocs.io/en/latest/using/selecting.html) puede consultar sobre la imágen utilizada, llamada *jupyter/pyspark-notebook*, donde también puede encontrar otras imágenes útiles al momento de trabajar con data, machine learning, entre otras cosas relacionadas.

### **Esquema**
En [get_schema.ipynb](get_schema.ipynb) se ven las columnas a mantener entre los archivos para tener un esquema homogéneo entre todos dado que la cantidad, orden y nombres de columnas varía entre archivos.

### **Sobre los recorridos**
En [rides.ipynb](rides.ipynb) se trabaja con los datos de los recorridos, se eliminan y completan valores nulos, según corresponda. Finalmente se cargan los datos procesados a alguna fuente (tal vez una database)