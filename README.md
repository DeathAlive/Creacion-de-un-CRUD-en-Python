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
    opoenpyxl es una libreria de Python3 la cual es utilizada para la lectura o modificacion de archivos **Excel**.

    * ### Instalacion de openpyxl:
        Para instalar el paquete **openpyxl** necesitamos tener **Python3** previamente instalado en nuestro sistema.<br>
        * #### Paso 1:
            Abrir nuestra terminal, CMD o Windows Powershell.
        * ### Paso 2:
            Ya dentro de nuestra terminal colocar la siguiente linea de comando: <br>
            ```tcl
            pip install openpyxl 
            ```
            y esperamos que se complete la instalacion, para comprobar si la instalacion fue realizada corectamente insertamos la siguiente linea de comando en nuestra terminal:<br>
            ```tcl
            python -m show openpyxl 
            ```
