# Creacion de un CRUD basico en Python.
* ##  Introduccion
    En este repositorio veremo la creacion de un **CRUD** sencillo (pero bastante enrevesado) en el lenguaje de programacion Python con el uso de el directorio [openpyxl](https://openpyxl.readthedocs.io/en/stable/), pero primero que nada veamos los requisitos minimos para crear nuestra **CRUD**.
    *  ### Requisitos minimos:

    Requisitos minimos | Descripcion
    -------------------|------------
    **Microsoft Office** (Cualquier version preferiblemente con Excel). | Es necesario el uso del paquete Office (mas exactamente **Excel**) para usar uno de sus programas como base de datos (esto se hace para remplazar el uso del lenguaje de programacion **PHP**).
    **[Python3](https://www.python.org/downloads/)** instalado en el sistema. | Es bastante evidente que la necesidad del lenguaje **python** en nuestro PC.
    Paquete **[openpyxl](https://openpyxl.readthedocs.io/en/stable/)** instalado. | Este paquete es necesario ser instalado en nuestro PC para poder hacer uso de este mismo ( ya que este no viene incluido en la instalacion de **Python3**).
    Editor de texto cualquira(**[Visual Studio Code](https://code.visualstudio.com/)** es uno de los mas destacados). | Necesitamos un editor de texto el cual podamos posteriormente convertir en un IDE el cual usaremos para estructurar nuestro CRUD.
* ## ¿Que es un CRUD?
    Un CRUD o por sus siglas en ingles (**Create Read Uptade Delete | Crear Leer Actualizar Eliminar**) es el conjunto de acciones basicar (y necesarias) para la gestion de datos. Varios procesos de gestión de datos están basados en CRUD, en los que dichas operaciones están específicamente adaptadas a los requisitos del sistema y de usuario, ya sea para la gestión de bases de datos o para el uso de aplicaciones.<br>
    Si quieres tener mas conocimiento al respecto de CRUD's te recomiendo usar el navegador duckduckgo.com.
* ## ¿Que es openpyxl?
    opoenpyxl es una libreria de Python3 la cual es utilizada para la lectura o modificacion de archivos **Excel**, si quieres profundizar mas sobre openpyxl haz click [aqui](https://openpyxl.readthedocs.io/en/stable/).

    * ### Instalacion de openpyxl:
        Para instalar el paquete **openpyxl** necesitamos tener **Python3** previamente instalado en nuestro sistema.<br>
        * #### Paso 1:
            Abrir nuestra terminal, CMD o Windows Powershell.
        * #### Paso 2:
            Ya dentro de nuestra terminal colocar la siguiente linea de comando: <br>
            ```tcl
            pip install openpyxl 
            ```
            y esperamos que se complete la instalacion, para comprobar si la instalacion fue realizada corectamente insertamos la siguiente linea de comando en nuestra terminal:<br>
            ```tcl
            python -m show openpyxl 
            ```
* ## Creacion de nuestro CRUD:
    * ### Prerequisitos:
        * Antes de empezar a hacer nuestro codigo necesitamos crear una archivo **Excel** al cual le pondremos el nombre de "__Base crud__", luego de haber creado nustro documento procederemos a abrirlo y cambiamos el nombre de la primera pagina por "__Datos    del crud__".
        * Luego necesitamos saber la ubicacion exacta de nuestro archivo **Excel**.
        * Abrir nuestro editor y crear nuestro archivo con extension .py.
        * Y por ultimo estar relajados y listos para enfrentarnos a muchos errores.
        >"El error es la parte mas importante del aprendizaje"
    * ### Iniciando con nuestro Codigo:
        ya estando dentro de nuestro editor de texto tenemos que escribir el esqueletro de nuestro **CRUD**, pero incluso antes de hacer esto debemos importar los paquetes que usaremos en la realizacion de nuestro **CRUD**.
        <br>
        ```python
        from datetime import datetime
        from openpyxl import load_workbook
        ```
        En estas dos lineas de codigo estamos importando dos librerias de python, la primer es **datetime** la cual es usada para el manejo de fechas como datos, y la otra (la mas importante entre las dos) es nuestra libreria **openpyxl** la cual tomamos de esta la funcion especifica de **load_workbook** la cual como su nombre indica esta cargara nuestro archivo de **Excel**.<br>
        Habiendo importado nuestras librerias nos queda escribir nuestro esqueleto el cual va a constar de 4 funciones, una por cada funcion de un **CRUD**, o sea las funciones seran: Agregar, Leer, Actualizar y Borrar, asi que pasemoslo a nuestro codigo.<br>
        Antes de empezar a colocar nuestras funciones debemos crear una variable que contendra una string con la ruta de nuestro archivo **Excel**, en mi caso es *"C:\Users\deavi\CRUD\Base crud.xlsx"*, pero para tenemos que tener en cuenta que si colocamos \ la string lo reconocera como un comando de manipulacion de strings, asi que tenemos dos opciones:<br>
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
            Como vemos la ruta va a ser una string ya que lleva caracteres alfanumericos y los datos son almacenados en un diccionario el cual veremos su uso posteriormente.
        2. #### Funcion leer
            Ahora procedamos a crear nuestra funcion leer la cual va a tener dos parametros los cuales van a ser **ruta** y **extraer**, ya es sabido que ruta es la direccion a la cual se va a enviar informacion pero en este caso es la direccion en la cual se va a **consultar** informacion, y el parametro extraer va a almacenar el contenido almacenado en la ruta.
            ```python
            def leer(ruta: str, extraer: str)
            return
            ```
            Al igual que la funcion crear nuestro parametro ruta va a ser una string la cual va almacenar nuestra ruta del documento y extraer va ser el parametro el cual sacara la informacion en un diccionario el cual va a contener la informacion.
        3. #### Funcion actualizar
            A continuacion creamos nuestra funcion actualizar la cual va atener tres parametros los cuales van a ser  **ruta, identificador y datos_actualizados**, la ruta es la direccion a la cual le vamos a actualizar la informacion, el identificador es el numero por el cual nuestro proceso va a ser caracterizado y por ultimo datos_actualizados es evidente lo que contiene.
            ```python
            def actualizar(ruta: str, identificador: int, datos_actualizados: dict):
                return
            ```
            Como las funciones anteriores el parametro ruta siempre va a ser una string, el identificador al ser un numero usaremos un int, y datos_actualizados es una lista la cual va a ser filtrada y usada para actualizar informacion en nuestra ruta.
        4. #### Funcion borrar
            Por ultimo crearemos nuestra funcion borra la cual va a tomar dos parametros los cuales seran **ruta y identificador**, ruta va a ser la ruta en la cual vamos a eliminar la informacion y identificador es el numero por el cual esta caracterizado el objeto que querramos eliminar.
            ```python
            def borrar(ruta: str, identificador: int):
                return
            ```
            El parametro ruta como se menciono solo puede ser una string ya que contiene caracteres alfanumericos y el identificador va a ser un entero ya que este es el numero de identificacion de el proceso 


