-Gestión de Alumnos

Descripción
La Gestión de Alumnos es una extensión de la aplicación de escritorio desarrollada en C# que permite administrar alumnos en un entorno educativo. La aplicación ofrece funcionalidades para agregar, modificar, eliminar y consultar alumnos, así como verificar la existencia de matrículas duplicadas. El diseño sigue la arquitectura de capas para una clara separación de responsabilidades y facilita el mantenimiento del código.

Funcionalidades

Agregar Alumno: Permite a los usuarios introducir nuevos alumnos en la base de datos.
Modificar Alumno: Facilita la actualización de la información de alumnos existentes.
Eliminar Alumno: Ofrece la opción de borrar alumnos no deseados.
Consultar Alumnos: Muestra todos los alumnos almacenados en la base de datos.
Verificar Duplicados: Previene la creación de alumnos con el mismo número de matrícula en la base de datos.
Estructura del Proyecto
El proyecto sigue una arquitectura de tres capas, organizada de la siguiente manera:

Modelo: Representa las entidades de la aplicación.
Capa de Acceso a Datos (DAL): Gestiona la comunicación con la base de datos.
Capa de Lógica de Negocio (BL): Contiene la lógica que coordina la interacción entre el modelo y la capa de acceso a datos.
Clases

Alumno
Propiedades:

IDAlumno: Identificador único del alumno.
Nombre: Nombre del alumno.
ApellidoPAt: Primer apellido del alumno.
ApellidoMat: Segundo apellido del alumno.
Email: Dirección de correo electrónico del alumno.
NumeroMatricula: Número de matrícula único del alumno.
AlumnosDAL
Métodos Principales:

InsertarAlumno: Inserta un nuevo alumno en la base de datos.
ModificarAlumno: Actualiza la información de un alumno existente.
EliminarAlumno: Elimina un alumno por su identificador.
SeleccionarAlumnos: Selecciona todos los alumnos de la base de datos.
SeleccionarUnAlumno: Selecciona un alumno específico por su identificador.
DatosRePETE: Verifica si ya existe un alumno con el mismo número de matrícula.
AlumnosBL
Métodos Principales:

Insertar: Maneja la inserción de un alumno y gestiona errores.
Modificar: Maneja la actualización de un alumno y gestiona errores.
Eliminar: Maneja la eliminación de un alumno y gestiona errores.
SeleccionarAlumnos: Obtiene todos los alumnos y gestiona errores.
SeleccionarUnAlumno: Obtiene un alumno específico y gestiona errores.
DatosRepetidos: Verifica la existencia de matrículas duplicadas.
Conexión a la Base de Datos
La aplicación utiliza una base de datos SQL Server. La cadena de conexión se configura en la clase AlumnosDAL. Debe ajustarse para apuntar al servidor y la base de datos correctos.

Diseño de la Base de Datos
La base de datos incluye una tabla llamada Alumnos con la siguiente estructura:

Campo	Tipo	Descripción
IDAlumno	INT	Identificador único del alumno
Nombre	NVARCHAR(100)	Nombre del alumno
ApellidoPAt	NVARCHAR(100)	Primer apellido del alumno
ApellidoMat	NVARCHAR(100)	Segundo apellido del alumno
Email	NVARCHAR(100)	Dirección de correo electrónico del alumno
NumeroMatricula	NVARCHAR(50)	Número de matrícula único del alumno
Uso

Interfaz de Usuario
La aplicación cuenta con una interfaz de usuario sencilla para interactuar con las funcionalidades de gestión de alumnos. A continuación, se describen los pasos para usar la aplicación:

Agregar Alumno:

Introduce el nombre, apellidos, correo electrónico y número de matrícula.
Haz clic en el botón "Agregar".
Modificar Alumno:

Selecciona un alumno de la lista.
Cambia la información deseada y haz clic en "Modificar".
Eliminar Alumno:

Selecciona el alumno que deseas eliminar y haz clic en "Eliminar".
Consultar Alumnos:

Haz clic en "Ver Alumnos" para listar todos los alumnos.
Verificar Duplicados:

Al intentar agregar un alumno con un número de matrícula ya existente, se mostrará un mensaje de error.


Gestión de Asignaturas
Descripción
La Gestión de Asignaturas es una aplicación de escritorio desarrollada en C# que permite administrar asignaturas en un entorno educativo. La aplicación ofrece funcionalidades para agregar, modificar, eliminar y consultar asignaturas, así como verificar la existencia de asignaturas duplicadas. El diseño sigue la arquitectura de capas, lo que promueve una clara separación de responsabilidades y facilita el mantenimiento del código.

Funcionalidades
Agregar Asignaturas: Permite a los usuarios introducir nuevas asignaturas en la base de datos.
Modificar Asignaturas: Facilita la actualización de información de asignaturas existentes.
Eliminar Asignaturas: Ofrece la opción de borrar asignaturas no deseadas.
Consultar Asignaturas: Muestra todas las asignaturas almacenadas en la base de datos.
Verificar Duplicados: Previene la creación de asignaturas con nombres ya existentes en la base de datos.
Estructura del Proyecto
El proyecto está organizado en tres capas principales:

Modelo: Representa las entidades de la aplicación.
Capa de Acceso a Datos (DAL): Se encarga de la comunicación con la base de datos.
Capa de Lógica de Negocio (BL): Contiene la lógica que gestiona la interacción entre el modelo y la capa de acceso a datos.

Clases
1. Asignatura
Propiedades:
CodigoAsignatura: Identificador único de la asignatura.
NombreAsignatura: Nombre de la asignatura.
Creditos: Número de créditos asignados a la asignatura.

2. AsignaturaDAL
Métodos Principales:
InsertarAsigna: Inserta una nueva asignatura en la base de datos.
Modificar: Actualiza la información de una asignatura existente.
Borrar: Elimina una asignatura por su identificador.
SelecionarTodo: Selecciona todas las asignaturas de la base de datos.
SeleccionarUno: Selecciona una asignatura específica por su identificador.
DatosDupli: Verifica si ya existe una asignatura con el mismo nombre.

3. AsignaturaBL
Métodos Principales:
InsertarAsigna: Maneja la inserción de una asignatura y gestiona errores.
Modificar: Maneja la actualización de una asignatura y gestiona errores.
Borrar: Maneja la eliminación de una asignatura y gestiona errores.
SeleccionarTodo: Obtiene todas las asignaturas y gestiona errores.
SeleccionarUno: Obtiene una asignatura específica y gestiona errores.
DatosDupli: Verifica la existencia de asignaturas duplicadas.

Conexión a la Base de Datos
La aplicación utiliza una base de datos SQL Server. La cadena de conexión se configura en la clase AsignaturaDAL. Es necesario ajustarla para apuntar al servidor y la base de datos correctos.
Diseño de la Base de Datos
La base de datos incluye una tabla llamada Asignaturas con la siguiente estructura:

Campo			Tipo			Descripción
CodigoAsignatura	INT			Identificador único de la asignatura
NombreAsignatura	NVARCHAR(100)		Nombre de la asignatura
Creditos		INT			Número de créditos asignados a la asignatura

Uso
Interfaz de Usuario
La aplicación cuenta con una interfaz de usuario sencilla que permite interactuar con las funcionalidades de gestión de asignaturas. A continuación se describen los pasos para usar la aplicación:

Agregar Asignatura:

Introduce el nombre de la asignatura y la cantidad de créditos.
Haz clic en el botón "Agregar".
Modificar Asignatura:

Selecciona una asignatura de la lista.
Cambia la información deseada y haz clic en "Modificar".
Eliminar Asignatura:

Selecciona la asignatura que deseas eliminar y haz clic en "Eliminar".
Consultar Asignaturas:

Haz clic en "Ver Asignaturas" para listar todas las asignaturas.
Verificar Duplicados:

Al intentar agregar una asignatura con un nombre ya existente, se mostrará un mensaje de error.


