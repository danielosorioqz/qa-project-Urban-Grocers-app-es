Project for the eight Sprint (Urban Grocers App) By Daniel Osorio, Group 35.

Another QA Engineer working with you is checking how the Urban Grocers app creates product kits. Several checklists have been created, one of which is for the name field in the product kit creation request.

Your task is to automate the tests from this checklist, upload the code to GitHub, and submit the repository for review.

Steps to Execute the Tests
Setup

Installing Pytest and Requests Libraries There are two methods to install Pytest and Requests. Choose the one that’s most convenient for you.

1️⃣ Using the "pip" command in the terminal:

Open the terminal or console. Enter the command pip install pytest. Enter the command pip install requests. pip is Python’s package manager. It allows you to install and manage libraries and additional tools.

📎 If the pip command doesn’t work, try using pip3 instead.

2️⃣ Through the PyCharm interface in "Python Packages":

In your PyCharm project, go to the bottom panel and select the "Python Packages" tab. In the search field, enter "Pytest." Locate and select the "Pytest" package from the list and click the "Install" button. Do the same for "Requests."

Running Tests
You have two options for running your tests: directly from PyCharm's console or using its graphical interface.

1️⃣ From the PyCharm terminal

Go to the "Terminal" tab at the bottom of PyCharm. By default, this terminal is in your project directory.

To run all tests in your project, simply type: pytest (within your directory) (e.g., Downloads/QA_BOOTCAMP/SPRINT_7/projects/qa-project-Urban-Grocers-app-en)

Then run the tests from the file create_kit_name_kit_test.py: pytest create_kit_name_kit_test.py

You’ll work with Git and GitHub for this project. Follow the steps below to set up your project:

Step 1: Connect your GitHub The first step is to link your GitHub account to TripleTen. To do this, click the "Link GitHub account" button in the widget at the top of this page. This will take you to a new browser tab where you’ll be asked to confirm that you want to link your GitHub account. If you haven’t logged into GitHub yet, you’ll be prompted to enter your username and password. Upon confirming, your TripleTen profile will be connected to your GitHub profile via GitHub’s secure API. This will allow you to submit your projects automatically with just a click, directly within the TripleTen platform.

Step 2: Clone the repository to your computer Once you’ve linked your TripleTen account with GitHub, a repository will be created automatically. The repository name will be qa-project-Urban-Grocers-app-en.

Go to GitHub and clone the new repository to your local computer by following these steps:

Open the command line on your computer. If you haven’t done so, create a directory to store all your projects. Clone the repository with SSH. Step 3: Work on the project locally Now you have a local copy of the project and can open the project folder on your computer.

Press the "Start Server" button to get your server URL.

Open the documentation to review the Urban Grocers app’s API: /docs/.

Look for "Main.Kits" → "Create a kit."

Creating a kit for the user You’ll create a kit within a particular user, not a card. To do so, follow these steps:

Send a request to create a new user and remember the authentication token (authToken). Send a request to create a personal kit for this user. Be sure to also pass the Authorization header. After that, simply use the checklist. Test results will vary each time, depending on the request body. However, the steps will remain the same.

Test Checklist

Allowed number of characters (1): kit_body = { "name": "a" } Response code: 201. The "name" field in the response body matches the "name" field in the request body.

Allowed number of characters (511): kit_body = { "name": "The test value for this check will be under the limit" } Response code: 201. The "name" field in the response body matches the "name" field in the request body.

Number of characters is less than the allowed amount (0): kit_body = { "name": "" } Response code: 400.

Number of characters exceeds the allowed amount (512): kit_body = { "name": "The test value for this check exceeds the limit" } Response code: 400.

Special characters are allowed: kit_body = { "name": "№%@," } Response code: 201. The "name" field in the response body matches the "name" field in the request body.

Spaces are allowed: kit_body = { "name": " A Aaa " } Response code: 201. The "name" field in the response body matches the "name" field in the request body.

Numbers are allowed: kit_body = { "name": "123" } Response code: 201. The "name" field in the response body matches the "name" field in the request body.

The parameter is not included in the request: kit_body = { } Response code: 400.

A different parameter type is passed (number): kit_body = { "name": 123 } Response code: 400.

Proyecto para el octavo sprint (Urban Grocers app) Por Daniel Osorio grupo 35.

Otro QA Engineer que trabaja contigo está comprobando cómo la aplicación Urban Grocers crea kits de productos. Se han creado varias listas de comprobación, una de ellas es para el campo name en la solicitud de creación de un kit de productos.

Tu tarea es automatizar las pruebas desde esta lista de comprobación, cargar el código en GitHub y enviar el repositorio a revisión

Pasos para ejecutar las pruebas
Configuración

Instalando Librerias Pytest y Requests
Existen dos métodos para instalar Pytest y Requests. Elige el que te resulte más conveniente.

1️⃣ Usando el comando "pip" en la terminal:

Abre la terminal o consola. Ingresa el comando pip install pytest. Ingresa el comando pip install requests. pip es el gestor de paquetes de Python. Te permite instalar y gestionar bibliotecas, así como herramientas adicionales.

📎 Si el comando pip no funciona, intenta usar pip3 en su lugar.

2️⃣ A través de la interfaz de PyCharm en "Python Packages":

En tu proyecto de PyCharm, dirígete al panel inferior y selecciona la pestaña "Python Packages". En el campo de búsqueda, introduce "Pytest". Localiza y selecciona el paquete "Pytest" de la lista y haz clic en el botón "Install". Haz lo mismo con "Requests"

Ejecución de pruebas
Tienes dos opciones para ejecutar tus pruebas: directamente desde la consola de PyCharm o utilizando su interfaz gráfica.

1️⃣ Desde la terminal de PyCharm

Dirígete a la pestaña "Terminal" en la parte inferior de PyCharm. Por defecto, esta terminal se ubica en el directorio de tu proyecto.

Para ejecutar todas las pruebas de tu proyecto, simplemente escribe: pytest (dentro de tu directorio) (Ej:Downloads/QA_BOOTCAMP/SPRINT_7/projects/qa-project-Urban-Grocers-app-es)

Luego ejecuta las pruebas desde el archivo create_kit_name_kit_test.py: pytest create_kit_name_kit_test.py

Trabajarás con Git y GitHub en este proyecto. Sigue los pasos a continuación para configurar tu proyecto:

Paso 1: conecta tu GitHub El primer paso es enlazar tu cuenta de GitHub a TripleTen. Para ello, haz clic en el botón "Enlazar la cuenta de GitHub" en el widget en la parte superior de esta página. Esto te llevará a una nueva pestaña del navegador donde se te pedirá que confirmes que deseas enlazar tu cuenta de GitHub. Si aún no has iniciado sesión en GitHub, se te pedirá que introduzcas tu nombre de usuario y contraseña. Al confirmarlo, tu perfil de TripleTen se conectará a tu perfil de GitHub a través de la API segura de GitHub. Esto te permitirá enviar tus proyectos automáticamente con tan solo hacer clic en un botón, directamente dentro de la plataforma de TripleTen.

Paso 2. Clona el repositorio en tu computadora Una vez que hayas vinculado tu cuenta de TripleTen con GitHub, se creará un repositorio automáticamente. El nombre del repositorio será qa-project-Urban-Grocers-app-es.

Ve a GitHub y clona el nuevo repositorio en tu computadora local, siguiendo estos pasos:

Abre la línea de comandos en tu computadora.
Si aún no lo has hecho, crea un directorio para almacenar todos tus proyectos.
Clona el repositorio con SSH.
Paso 3. Trabaja con el proyecto de forma local Ahora tienes una copia local del proyecto y puedes abrir la carpeta del proyecto en tu computadora.

Presiona el botón "Iniciar el servidor" para obtener la URL de tu servidor.

Abre la documentación para estudiar la API de la aplicación de Urban Grocers: /docs/.

Busca "Main.Kits" →" Crear un kit.”

Creación de un kit para el usuario o usuaria

Vas a crear un kit dentro de un usuario o usuaria particular, no una tarjeta. Para ello, sigue estos pasos:

Envía una solicitud para crear un nuevo usuario o usuaria y recuerda el token de autenticación (authToken). Envía una solicitud para crear un kit personal para este usuario o usuaria. Asegúrate de pasar también el encabezado Autorization. Después de eso, simplemente utiliza la lista de comprobación. Los resultados de la prueba serán diferentes cada vez, según el cuerpo de solicitud. Sin embargo, los pasos serán los mismos.

Lista de comprobación de pruebas

El número permitido de caracteres (1): kit_body = { "name": "a"} Código de respuesta: 201 El campo "name" del cuerpo de la respuesta coincide con el campo "name" del cuerpo de la solicitud

El número permitido de caracteres (511): kit_body = { "name":"El valor de prueba para esta comprobación será inferior a"} Código de respuesta: 201 El campo "name" en el cuerpo de la respuesta coincide con el campo "name" en el cuerpo de la solicitud

El número de caracteres es menor que la cantidad permitida (0): kit_body = { "name": "" } Código de respuesta: 400

El número de caracteres es mayor que la cantidad permitida (512): kit_body = { "name":"El valor de prueba para esta comprobación será inferior a” } Código de respuesta: 400

Se permiten caracteres especiales: kit_body = { "name": ""№%@"," } Código de respuesta: 201 El campo "name" del cuerpo de la respuesta coincide con el campo "name" del cuerpo de la solicitud

Se permiten espacios: kit_body = { "name": " A Aaa " } Código de respuesta: 201 El campo "name" del cuerpo de la respuesta coincide con el campo "name" del cuerpo de la solicitud

Se permiten números: kit_body = { "name": "123" } Código de respuesta: 201 El campo "name" del cuerpo de la respuesta coincide con el campo "name" del cuerpo de la solicitud

El parámetro no se pasa en la solicitud: kit_body = { } Código de respuesta: 400

Se ha pasado un tipo de parámetro diferente (número): kit_body = { "name": 123 } Código de respuesta: 400.