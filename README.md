# Creacion de un CRUD basico en Python.
* ## Indice
    Indice|
    ------|
    [Introduccion](https://github.com/DeathAlive/Creacion-de-un-CRUD-en-Python/blob/main/README.md#introduccion)
    [¿Que es un CRUD?](https://github.com/DeathAlive/Creacion-de-un-CRUD-en-Python/blob/main/README.md#que-es-un-crud)
    [¿Que es openpyxl?](https://github.com/DeathAlive/Creacion-de-un-CRUD-en-Python/blob/main/README.md#que-es-openpyxl)
    [Creacion de nuestro CRUD](https://github.com/DeathAlive/Creacion-de-un-CRUD-en-Python/blob/main/README.md#creacion-de-nuestro-crud)

    Extras|
    ------|
    [Archivo final](https://github.com/DeathAlive/Creacion-de-un-CRUD-en-Python/blob/main/Archivo-Final.py)
* ##  Introduccion
    En este repositorio veremos la creación de un **CRUD** sencillo (pero bastante enrevesado) en el lenguaje de programación Python con el uso del directorio [openpyxl](https://openpyxl.readthedocs.io/en/stable/), pero primero que nada veamos los requisitos mínimos para crear nuestra **CRUD**.
    *  ### Requisitos mìnimos: 
    Requisitos mínimos | Descripción
    -------------------|------------
    **Microsoft Office** (Cualquier versión preferiblemente con Excel). | Es necesario el uso del paquete Office (más exactamente **Excel**) para usar uno de sus programas como base de datos (esto se hace para remplazar el uso del lenguaje de programación **PHP**).
    **[Python3](https://www.python.org/downloads/)** instalado en el sistema. | Es bastante evidente que la necesidad del lenguaje **python** en nuestro PC.
    Paquete **[openpyxl](https://openpyxl.readthedocs.io/en/stable/)** instalado. | Este paquete es necesario ser instalado en nuestro PC para poder hacer uso de este mismo ( ya que este no viene incluido en la instalación de **Python3**).
    Editor de texto cualquiera(**[Visual Studio Code](https://code.visualstudio.com/)** es uno de los más destacados). | Necesitamos un editor de texto el cual podamos posteriormente convertir en un IDE el cual usaremos para estructurar nuestro CRUD.
* ## ¿Que es un CRUD?
    Un CRUD o por sus siglas en ingles (**Create Read Uptade Delete | Crear Leer Actualizar Eliminar**) es el conjunto de acciones básica (y necesarias) para la gestión de datos. Varios procesos de gestión de datos están basados en CRUD, en los que dichas operaciones están específicamente adaptadas a los requisitos del sistema y de usuario, ya sea para la gestión de bases de datos o para el uso de aplicaciones.<br>
    Si quieres tener más conocimiento al respecto de CRUD's te recomiendo usar el navegador duckduckgo.com. 
* ## ¿Que es openpyxl?
    openpyxl es una librería de Python3 la cual es utilizada para la lectura o modificación de archivos **Excel**, si quieres profundizar más sobre openpyxl haz click [aqui](https://openpyxl.readthedocs.io/en/stable/).

    * ### Instalacion de openpyxl:
        Para instalar el paquete **openpyxl** necesitamos tener **Python3** previamente instalado en nuestro sistema.<br>
        * #### Paso 1:
            Abrir nuestra terminal, CMD o Windows Powershell.<br>
        * #### Paso 2:
            Ya dentro de nuestra terminal colocar la siguiente línea de comando: <br>
            ```tcl
            pip install openpyxl 
            ```
            Y esperamos que se complete la instalación, para comprobar si la instalación fue realizada correctamente insertamos la siguiente línea de comando en nuestra terminal:<br>
            ```tcl
            python -c "import opeyxl"
            >> echo $? 
            ```
            Esto devolvera '**TRUE**' si la libreria esta instalada y '**FALSE**' si no existe
* ## Creacion de nuestro CRUD:
    * ### Prerequisitos:
        * Antes de empezar a hacer nuestro código necesitamos crear una archivo **Excel** al cual le pondremos el nombrede "__Base crud__" luego de haber creado nuestro documento procederemos a abrirlo y cambiamos el nombre de la primera página por"__Datos    del crud__".
        * Luego necesitamos saber la ubicacion exacta de nuestro archivo **Excel**.
        * Abrir nuestro editor y crear nuestro archivo con extension .py.
        * Y por ultimo estar relajados y listos para enfrentarnos a muchos errores.
        >"El error es la parte mas importante del aprendizaje"
    * ### Iniciando con nuestro Codigo: 
        Ya estando dentro de nuestro editor de texto tenemos que escribir el esqueleto de nuestro **CRUD**, pero incluso antes de hacer esto debemos importar los paquetes que usaremos en la realización de nuestro **CRUD**.
        <br>
        ```python
        from datetime import datetime
        from openpyxl import load_workbook
        ```
        En estas dos líneas de código estamos importando dos librerías de Python, la primera es **datetime** la cual es usada para el manejo de fechas como datos, y la otra (la mas importante entre las dos)es nuestra librería **openpyxl** la cual tomamos de esta la función especifica de **load_workbook** la cual como su nombre indica estacargara nuestro archivo de **Excel**.<br>
        Habiendo importado nuestras librerías nos queda escribir nuestro esqueleto el cual va a constar de 4 funciones,una por cada función de un **CRUD**, o sea las funciones serán: Agregar, Leer, Actualizar y Borrar,así que pasémoslo a nuestro código.<br>
        Antes de empezar a colocar nuestras funciones debemos rear una variable que contendrá una string con la ruta de nuestro archivo **Excel**, en mi caso es *"C:\Users\deavi\CRUD\Base crud.xlsx"* pero tenemos que tener en cuenta que si colocamos \ la string lo reconocerá como un comando de manipulación de strings así que tenemos dos opciones:<br>
        **Usando el formato rstring (r"" o r'') el cual no hará caso a los comandos de manipulacion de strings.**
        ```python
            rut = r'C:\Users\deavi\CRUD\Base crud.xlsx'
        ``` 
        **Usando \  dobles.**
        ```python
            rut = 'C:\\Users\\deavi\\CRUD\\Base crud.xlsx'
        ```
        Ahora si empecemos a crear nusetras funciones.
        1. #### Funcion agregar
            Primero tenemos que crear nuestra funcion agregar la cual va a recibir dos parametros, los cuales son **ruta** y **datos**, ruta siendo la direccion en la cual vamos a ingresar los datos y datos pues la informacion que se va a ingresar en la ruta.
            ```python
            def agregar(ruta: str, datos: dict):
            return
            ```
            Como vemos la ruta va a ser una string, ya que lleva caracteres alfanuméricos y los datos son almacenados en un diccionario el cual veremos su uso posteriormente.
        2. #### Funcion leer
            Ahora procedamos a crear nuestra función leer la cual va a tener dos parámetros los cuales van a ser **ruta** y **extraer**, ya es sabido que ruta es la dirección a la cual se va a enviar información, pero en este caso es la dirección en la cual se va a **consultar** información, y el parámetro extraer va a almacenar el contenido almacenado en la ruta.
            ```python
            def leer(ruta: str, extraer: str)
            return
            ```
            Al igual que la función crear nuestro parámetro ruta va a ser una string la cual va a almacenar nuestra ruta del documento y extraer va a ser el parámetro el cual sacara la información en un diccionario el cual va a contener la información.
        3. #### Funcion actualizar
            A continuación creamos nuestra función actualizar la cual va a tener tres parámetros los cuales van a ser  **ruta, identificador y datos_actualizados**, la ruta es la dirección a la cual le vamos a actualizar la información, el identificador es el número por el cual nuestro proceso va a ser caracterizado y por último datos_actualizados es evidente lo que contiene.
            ```python
            def actualizar(ruta: str, identificador: int, datos_actualizados: dict):
                return
            ```
            Como las funciones anteriores el parámetro ruta siempre va a ser una string, el identificador al ser un número usaremos un int, y datos_actualizados es una lista la cual va a ser filtrada y usada para actualizar información en nuestra ruta.
        4. #### Funcion borrar
            Por último crearemos nuestra función borra la cual va a tomar dos parámetros los cuales serán **ruta e identificador**, ruta va a ser la ruta en la cual vamos a eliminar la información e identificador es el número por el cual está caracterizado el objeto que queramos eliminar.
            ```python
            def borrar(ruta: str, identificador: int):
                return
            ```
            El parámetro ruta como se mencionó solo puede ser una string ya que  contiene  caracteres alfanuméricos y el identificador va a ser un entero, ya que este es el número de identificación del proceso.
    * ### Funcion filtrar
    En el siguiente texto veremos la explicacion de la funcion filtro, la cual usaremos para filtrar datos de nuestros inputs

    ```python
        def filtrar(info:dict, filtro:str):
        aux={}

        for i in info:
        if info[i]['estado']==filtro:
        aux.setdefault(i, info[i])
        return aux
    ```







