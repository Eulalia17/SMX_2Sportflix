<img width="672" height="677" alt="image" src="https://github.com/user-attachments/assets/80dba62e-8d83-4fd6-b0b3-5089749d29e6" />



# 📌Índice
<details>
  <summary>&#8203;</summary> <!-- desplegable vacío -->
	
Nombre del proyecto: Sportflix

1. Introducción

2. Briefing de ideas

3. Informe Backend

4. Arquitectura del software

5. Tecnologías a utilizar

6. Red

a. Diagrama de la red

7. Web

d. Diseño

e. Mockup

f. Mapa de navegabilidad

8. Servicios

g. DNS

h. DHCP

i. Apache

j. Firewall

k. Copias de seguridad

9. Conclusiones

10. Bibliografía
</details>


## 🏎️ 1. Introducción
<details>
  <summary>&#8203;</summary> <!-- desplegable vacío -->
Estamos haciendo un projecto que consiste en crear una web que en nuestro caso es de notícias de fórmula 1 y tendrá apartados exclusivamente con pilotos 3D españoles, también su apartado de soporte para mirar los problemas frecuentes que suceden en nuestra web, su apartado de última hora y también su apartado de introducción explicando quienes somos. 
</details>

## 2. Briefing de ideas
<details>
  <summary>&#8203;</summary> <!-- &#8203; es un "zero-width space" -->

### Idea seleccionada y justificación
Porque hemos escogido esta idea: Lo hemos escogido porque es original, también porque hay mucha información sobre los temas que hemos escogido para la web y, además, nuestra web se puede personalizar, lo que ayudará a mantener la atención del público y hacerla más atractiva.

### Objetivos
* Crear la página web.
* Diseñar cómo sería la página web donde se mostrarán noticias, pilotos, coches y otros detalles de la F1.
* Importar noticias de Fórmula 1 de webs fiables y oficiales.  
* Guardar todos los datos en una base de datos.
* Diseñar en 3D los coches a mostrar en la web y, si es posible, hacer lo mismo con los pilotos.

### Público al que va dirigido
A todos los públicos que les guste el deporte y, sobre todo, la Fórmula 1.

### Módulos que vamos a tocar (Asignaturas)

**Seguridad**
- MO6: Firewall: pfsense o Sophos.
- MO6: Backup: Trunas y/o rsync.
- MO6: Plan de contingencia y explicación de aspectos de seguridad implementados o a implementar.
- MO4: Diferenciar roles de usuarios en el sistema.

**Servicios de red**
- MO5-MO6: Diagrama de red, mapa físico y mapa lógico de la infraestructura.
- MO4-MO7: Servicio DHCP en un servidor Windows diferente.
- MO7: Servidor DNS primario.

**Sistemas operativos**
- MO4: Instalación y configuración de sistemas operativos (Windows Server / Linux) para alojar los servicios del proyecto.
- MO4: Gestión de usuarios, grupos y permisos para diferenciar roles (administrador, desarrollador, visitante).
- MO4: Configuración de servidores necesarios para la web (Apache, DNS, DHCP, etc.).
- MO4: Administración y monitorización del sistema.
- MO4: Virtualización de servidores y estaciones de trabajo (VirtualBox, VMware o Proxmox).
- MO4: Implementación de políticas básicas de seguridad y actualización del sistema operativo.
- MO4: Automatización de tareas administrativas mediante scripts (bash o PowerShell).

**Aplicaciones web**
- MO8: Mapa de navegabilidad y Mockups.
- MO8: Web responsive.

**Programación (opcional)**
- MO8: HTML (estructura básica de páginas web).
- MO8: CSS (diseño y estilos de páginas web).
- MO8: JavaScript (funcionalidades interactivas).

### Materiales necesarios
**Físicos:** Libreta para apuntar ideas, ordenador.  
**Lógicos:** Drive del proyecto, Visual Studio, enlaces a recursos, Trello, GitHub, Microsoft Office para la infraestructura de red.

</details>

### Recursos
<details>
  <summary>Nuestros Recursos</summary>

**Bibliografía:**  
- Github: [Docs GitHub](https://docs.github.com/es/get-started/start-your-journey/hello-world), [Gist](https://gist.github.com/dasdo/9ff71c5c0efa037441b6)  
- PrestaShop: [prestashop.es](https://prestashop.es)  
- MySQL: [Tutorial MySQL](https://www.mysqltutorial.org/), [Comandos básicos](https://blog.baehost.com/comandos-basicos-para-mysql/)  
- Cloudflare: [Blog Cloudflare](https://raiolanetworks.com/blog/cloudflare/), [Developers](https://developers.cloudflare.com/cloudflare-one/connections/connect-networks/do-more-with-tunnels/local-management/tunnel-useful-commands/)  
- Proxmox: [Top comandos CLI](https://www.nakivo.com/es/blog/top-10-proxmox-cli-commands/), [Instalación](https://www.nakivo.com/blog/proxmox-install/)

</details>


## 3. Informe Backend

<details>
<summary>Nuestro informe</summary>
	
### 1. Descripción general del proyecto web

¿De qué trata tu web?
            Crear una web de noticias de Fórmula 1 con los pilotos españoles y  
            también queremos que cuando clickeis al perfil del piloto os salga su coche en 3D.
            (*Puede ser que pongamos algún piloto de otro país.*)


¿Qué funcionalidades ofrecerá a los usuarios?
             Las funcionalidades que ofreceremos a los usuarios son:


Crear una cuenta al momento de entrar a la página (Registrarse y Logearse).
Tendrán un apartado donde podrán ver las últimas noticias de todos esos pilotos a la vez.
Tener un apartado de favoritos para poner sus pilotos favoritos.
Interactuar con los elementos de la web como el piloto y el coche.
 


### 2. Identificación de entidades principales
¿Qué elementos importantes hay en tu web que necesitan almacenarse?
            Usuarios: nombre, apellido1, contraseña, número de identificación, fecha en la que inició  
            sesión en la web, email.
	
            Piloto: Nombre, nacionalidad, estadísticas, número, equipo, edad, posición en las                      
            carreras,trofeos, victorias, poles y mejor puesto.
            
            Coche: Modelo, marca, color, escuderías , eslogan, motor, democión, tipo de motor,  
            fabricante de motor, cilindrada de motor, patrocinadores de los coches.


            Noticias: Origen de la web, fecha, horas,calendario de las carreras,resultados de las   
            carreras, clasificación de los pilotos, palmarés de los pilotos o los coches, clasificación  
            de los constructores.
            
¿Qué tema de información almacena? Datos de los usuarios como por ejemplo correo electrónico, contraseñas, nombre, apellido, número de identificación y la fecha en que se inició la cuenta. 


También los datos del piloto como son el nombre, nacionalidad, estadísticas, número, equipo, edad, posición en las carreras, trofeos, victorias, poles y mejor puesto. También los datos importantes del coche como es el modelo, marca, color, escuderías, eslogan, motor, democión, tipo de motor, fabricante de motor, cilindrada de motor, los patrocinadores de los coches y luego para finalizar los elementos importantes de las noticias: origen de la web, fecha, horas,calendario de las carreras,resultados de las   
carreras, clasificación de los pilotos, palmarés de los pilotos o los coches, clasificación de los constructores.








¿Por qué necesitas guardarla en la base de datos?
Porque así nos aseguramos que toda la información importante y necesaria esté bien guardada y dividida por apartados.








### 3. Datos que se deben guardar de cada entidad (atributos)
-Nombre
-Apellidos
-Correo electrónico
-Número de identificación 
-Contraseñas
-Fecha

El tipo de dato que utilizaremos es de texto, número, fecha, links y la definición que considero que corresponde es varchar, int, decimal, date, datetime y el auto increment.









### 4. Relaciones entre las entidades
<summary>Relaciones entre las entidades</summary>	
¿Cómo se relacionan unas entidades con otras?
Ejemplo:


            Usuarios:
            -id usuario 
            -nombre
            -email
            -contraseña


             Pedidos:
             -id pedido
             -id usuario (*Id Identificación*)
             -Fecha pedido
              
<img width="659" height="415" alt="image" src="https://github.com/user-attachments/assets/b815cd48-8405-49c0-bd90-d58f80f554d1" />





	




### 5. Ejemplo de datos (simulación)
<summary>Datos</summary>

	

Incluye un ejemplo de cada entidad con datos ficticios pero realistas.

Nombre: Pepe

Apellido: Morientes

Correo electrónico: pepem@gmail.com

Número de identificación: Pep2345

Contraseñas:ppm75345

Fecha de registro: 11-09-25 a las 15:40:25.

### 6. Reflexiones, dificultades y dudas que tienes sobre la base de datos
¿Qué partes te han resultado más difíciles de pensar?


Las partes que nos ha resultado más difíciles de pensar ha sido lo que les vamos a ofrecer a los usuarios porque como estamos comenzando el proyecto posiblemente se nos puede ocurrir nuevas ideas y que también podría encajar bien en nuestro proyecto.


¿Qué no tienes claro sobre la información que hay que guardar?
            
            Lo que no tenemos claro sobre la información que hay que guardar es lo del número   
            de identificación porque con el nombre y apellido pensamos que con eso es    
            suficiente. 

### 7. Diagrama de base de datos

Primero hemos realizado un borrador del diagrama de base de datos de nuestro proyecto en canva para después hacer el definitivo en MySQL WorkBench.
<img width="1103" height="641" alt="image" src="https://github.com/user-attachments/assets/65418b17-ff1d-402d-9c34-eaa50a0586d0" />

Los cambios que hemos realizado han sido los siguientes:

Tabla Lista -> Tabla intermedia entre Usuarios y Pilotos: "Pilotos_favoritos"

Tabla Marcas se elimina porque la información se guardará en la tabla Escuderia

Tabla Historial -> Cambia de nombre a Auditoria_registro y eliminamos el atributo acción

Tabla Ayuda -> Eliminada, el manual de uso y ayuda será estático en la web

Tabla Perfil -> Eliminada yta que tendremos todos los datos de cada perfil en la tabla usuarios

Y aquí os muestro una captura de nuestro diagrama definitivo:
<img width="777" height="479" alt="image" src="https://github.com/user-attachments/assets/842edf6b-bef1-42b8-ba4a-2d1b2e796c74" />

### Enlace diagrama Canva y archivo de MySQL Workbench
Canva: https://www.canva.com/design/DAG4k7iY37E/NoqqAwjC69FU2OK2PILwGA/edit

MySQL Workbench: <a src=\Diagrama base de datos Sportflix.mwb>Diagrama Relacional</a>

</details>


## 4. Arquitectura del software
<details> 
Funcionalidades 
En este apartado asignamos unos requisitos y funcionalidades, asignando prioridades y fechas de entrega para cada tarea del proyecto y también hemos organizado cada ítem indicando su estado actual y objetivo correspondiente.
	
<img width="914" height="453" alt="image" src="https://github.com/user-attachments/assets/f7186cac-dbec-4bff-95de-71de30f78ebb" />

<img width="911" height="218" alt="image" src="https://github.com/user-attachments/assets/a1d992c3-9111-499b-8b5e-fcb63fe8bc71" />

### Objetivos
<details>
	<summary>Objetivo 1</summary>

Objetivo 1: Implementar un servidor web

1.1 Instalación y configuración básica del servidor CP1.2 – Se ha instalado y configurado un sistema operativo en red
Descripción de la tarea: Se ha instalado un sistema operativo en red (por ejemplo Ubuntu Server 22.04). Se ha configurado la red con una IP estática, el hostname del servidor y el acceso remoto mediante SSH.
El servidor queda actualizado y preparado para la instalación de servicios web.

1.2 Configurar la política de usuarios y privilegios
CP1.2 – Se ha instalado y configurado un sistema operativo en red
Descripción de la tarea:
Se han creado los usuarios necesarios para la administración del servidor.
Se han asignado los permisos adecuados mediante sudo y grupos específicos.
Se ha configurado la seguridad del acceso, deshabilitando el acceso root por SSH y asegurando contraseñas/claves.

1.3 [David] Instalación y configuración de los servicios web Apache, MySQL DB, PHP 8.2 y PHPMYADMIN para el proyecto Sportflix
CP3.1.1 – Se configura y se garantiza el funcionamiento de un servicio de servidor web
Descripción de la tarea: Se ha instalado y configurado el stack necesario para desplegar el proyecto del repositorio:
https://github.com/Eulalia17/SMX_2Sportflix

Las acciones realizadas incluyen:

Instalación del servidor web Apache.

Instalación del motor de base de datos MySQL DB, creación de la base de datos y del usuario asignado al proyecto.


Instalación de PHP 8.2 junto a los módulos necesarios para el funcionamiento del sitio.


Instalación y configuración de phpMyAdmin.


Clonado del repositorio SMX_2Sportflix en el directorio web del servidor.


Configuración del bloque de servidor (server block) en NGINX para apuntar a la ruta del proyecto.


Asignación de permisos adecuados al directorio del proyecto.


Configuración de acceso a la base de datos desde el archivo de conexión del proyecto.


Comprobación final del correcto funcionamiento del servicio web y del acceso mediante navegador.
</details>
<details>
<summary>Objetivo 2</summary>

Objetivo 2: Programar la front-page (visual studio).

2.1 Crear la estructura del index.html con CSS

CP2.1.6 – Los ficheros de lenguaje de marcas empleados tienen un código correcto y adecuado, transmiten al usuario la información correctamente y ofrecen una buena experiencia de usuario a nivel gráfico.

Descripción de la tarea:

Se ha creado la estructura base del archivo index.html utilizando etiquetas HTML semánticas.

Se ha añadido una hoja de estilos CSS que define la distribución principal de la landing page, la tipografía, paleta de colores, espaciados y elementos visuales necesarios.

El código cumple los estándares de accesibilidad y ofrece una presentación clara e intuitiva al usuario.


2.2 Crear el header y el footer comunes de todas las páginas
CP2.1.6 – Los ficheros de lenguaje de marcas empleados tienen un código correcto y adecuado, transmiten al usuario la información correctamente y ofrecen una buena experiencia de usuario a nivel gráfico.

Descripción de la tarea:

Se han programado el header y footer globales que se integrarán en todas las páginas del proyecto.

El header incluye el logotipo, el menú de navegación y los enlaces principales.

El footer contiene la información de contacto, enlaces secundarios y secciones informativas necesarias.

Ambos elementos están maquetados con CSS para mantener coherencia visual en toda la web.

2.3 Programar el formulario de contacto de la front-page

CP2.1.6 – Los ficheros de lenguaje de marcas empleados tienen un código correcto y adecuado, transmiten al usuario la información correctamente y ofrecen una buena experiencia de usuario a nivel gráfico.

Descripción de la tarea:

Se ha desarrollado un formulario de contacto integrado en la front-page con campos de nombre, correo electrónico, mensaje y botón de envío.

El formulario se ha maquetado con CSS manteniendo la estética del resto de la página.

Se han aplicado validaciones básicas en HTML5 (required, type="email") para mejorar la experiencia del usuario y garantizar la correcta introducción de datos.
</details>
<details>
	<summary>Objetivo 3</summary>

Objetivo 3: Servidor MySQL

3.1 Instalar y configurar MV con Ubuntu Server LTS versión 22.04.

3.2 Instalar y configurar MySQL versión 8.0 para crear y gestionar bases de datos.

3.3 Instalar y configurar PHPMYADMIN para administrar nuestra base de datos a través de una interfaz web permitiendo realizar tareas que serán crear/eliminar bases de datos y tablas, editar datos, ejecutar consultas SQL y exportar/importar bases de datos sin necesidad de usar la línea de comandos.
</details>
<details>
	<summary>Objetivo 4</summary>

Objetivo 4: Servidor web

4.1 Configurar MV con ubuntu server 22.04.

4.2 Buscar guía de instalación para instalar Apache y PHP.

4.3 Instalar Apache.

4.4 Definir nombre del dominio que será https://sportflix.com/. 
</details>
<details>
	<summary>Obejtivo 5</summary>

Objetivo 5: Servidor DNS

5.1 Instalar y configurar MV con ubuntu server 22.04.

5.2 Buscar guía de instalación para servidor DNS de Pi-hole.

5.3 Instalar Pi-hole.
</details>
<details>
	<summary>Objetivo 6</summary>

Objetivo 6: Servidor TRUENAS + RSYNC


6.1 Instalar y configurar  MV con la ISO del truenas versión 25.04.2.6, tipo BSD y versión freeBSD 64 bits para que funcione bien la máquina.

6.2 Buscar guía de instalación para Truenas y rsync.

6.3 Instalar Truenas y recibir el enlace con la IP y ponerlo en el buscador de google.

6.4 Poner el usuario truenas_admin y la contraseña.

6.5 Crear un dataset.

6.6 Activar el protocolo SMB.

6.7 Desencriptar el dataset.

6.8 Activar todos los permisos de escribir, leer y ejecutar. 

6.9 Crear y configurar una MV Linux para el Rsync.
 
6.10 Entramos al terminal para apuntar los comandos siguiendo las instrucciones de la guía del tutorial de Rsync.
 
6.11 Hacer la transferencia de archivos a través de conexiones de red en la terminal de nuestra MV. 

### Arquitectura del sistema

<details>

<img width="911" height="361" alt="image" src="https://github.com/user-attachments/assets/0e271397-e234-414d-b4a9-91ec4283ac16" />

<img width="915" height="372" alt="image" src="https://github.com/user-attachments/assets/9c88b829-54d7-4aa7-a70f-e66ed6eb6b41" />

<img width="911" height="232" alt="image" src="https://github.com/user-attachments/assets/32f9229f-38ed-4fa9-8695-c69b1f1152c7" />

<img width="911" height="140" alt="image" src="https://github.com/user-attachments/assets/72184075-c32a-4e19-9522-5e4cf1cfd0f1" />


### Diagrama de la base de datos
<details>
Resumen de la DB de tu aplicación web:
¿Qué datos son necesarios para mi aplicación? 
Los datos importantes son administración, usuarios, pilotos, escuderías, notícias, coches y auditoría.

¿Qué datos voy a pedir al usuario y que tipos de usuarios voy a tener?
Los datos a pedir al usuario son el correo electrónico y su contraseña para que se puedan crear su cuenta y también que puedan tener su propio perfil de usuario y voy a tener cualquier tipo de usuario.

¿Qué tipo de dato necesitaré para cada información? (Aquí tienes la documentación oficial de MySQL)
El tipo de datos que necesitamos son:
             
IDs → INT UNSIGNED AUTO_INCREMENT


Nombres, correos, modelos, etc. → VARCHAR(15-40)


Contraseñas → VARCHAR(14) 


Fechas → DATETIME


Contenido largo → TEXT


Listas cerradas → ENUM()


URLs → VARCHAR(255)


Tablas puente (N:N) → dos INT UNSIGNED


¿Qué clave primaria voy a implantar en cada tabla? ¿Cómo las relacionaré entre ellas?
La clave primaria: id_usuario, id_noticias, id_pilotos, id_escuderías, id_registro, id_coches. 
Las relacionaré de esta forma:
Usuarios → Auditoria: relación 1:N


Usuarios ↔ Pilotos: relación N:N mediante Pilotos_favoritos


Escuderías → Pilotos: relación 1:N


Escuderías → Coches: relación 1:N


Pilotos ↔ Noticias: relación N:N mediante Pilotos_has_Noticias


Escuderías ↔ Noticias: relación N:N mediante Escuderías_has_Noticias


Coches ↔ Noticias: relación N:N mediante Noticias_has_Coches

- Las funcionalidades de la BD:
  	- Auditoria_registro --> A.P
  	- Noticias --> C.F
  	- Usuarios --> B.S
  	- Pilotos_favoritos --> C.F
  	- Pilotos_has_noticias --> C.F
  	- Escuderias_has_noticias --> C.F
  	- Noticas_has_coches --> C.F
  	- Coches --> C.F
  	- Pilotos --> C.F
  	- Escuderías --> C.F

  
Mi Diagrama de Base de datos
<img width="802" height="529" alt="image" src="https://github.com/user-attachments/assets/25a4fa83-df89-46a4-aa32-1d6658d3677a" />

</details>


## 5. Tecnologías a utilizar
<details>
- Estos son nuestras tecnologías:
	
	1. En el apartado de hardware
	
		1.1. Router del aula
		
	     - Se utilizará para proporcionar conexión de red a todos los equipos y gestionar el tráfico interno y externo de 			internet.
		 
		1.2. Servidor:
		
	  		1.2.1. Truenas
			
				- Versión --> 25.04.2.6
				
				- Para alojar servicios como páginas web, base de datos y almacenamiento en red, además de centralizar 						recursos para prácticas y gestión del aula.
				
			1.2.2. Apache
			
				- Versión --> 2.4.x estable
				
				- Lo he puesto anteriormente.
				
			1.2.3. MySQL
			
				- Versión --> 8.0.x LTS estable
				
				- Lo he puesto anteriormente.
				
		1.3. HDD para Backup
		
			- Realizará copias de seguridad de la información del servidor y evitar pérdida de datos ante fallos o errores.
			
	2. Sistemas operativos
	
		2.1. Ubuntu server
		
			- Versión --> Ubuntu LTS 24.10 
			
			- Usaremos ubuntu server para gestionar y ejecutar servicios en un servidor para el alojamiento de sitios web, 				administración de bases de datos.
			
	3. Inerfaz de usuarios (Frontend)
	
		3.1. HTML 5
		
			- Versión --> HTML 5
			
			- Lo utilizaremos para definir el estilo visual y la presentación de nuestra página HTML.
			
		3.2. CSS 3
		
			- Versión --> CSS 3
			
			- Lo utilizaremos para definir el estil visual y la presentación de nuestra página HTML.
			
		3.3. Javascript
		
			- Versión--> ES2020
			
			- Lo utilizaremos para hacer nuestra página interactiva, permitiendo que reaccionen a las acciones del usuario 					y muestra el contenido dinámico.
			
		3.4. Bootstrap 5
		
			- Versió --> Bootstrap 5
			
			- Lo utilizamos para crear la página web.
			
     4. Lógica de negocio (Backend)
	 
		4.1. PHP
		
			- Versión --> PHP 8.4
			
			- Lo utilizaremos para crear la página web.
			
	5. Servidor web
	
		5.1. Apache
		
			- Versión --> Apache 2.4 
			
			- Lo usuaremos para alojar páginas web y ejecutar.
			
		5.2. PHP
		
			- Versión --> PHP 8.4
			
			- Lo usaremos para alojar páginas web y ejecutar.
			
	6. Base de datos
	
		6.1. MySQL
		
			- Versión --> MySQL 8.0
			
			- Lo utilizaremos para gestionar y almacenar las bases de datos
			
	7. Sistema gestor de base de datos
	
		7.1. PHPMyAdmin
		
			- Versión --> PHPmyAdmin
			
			- Lo utilizaremos para administrador bases de datos en MySQL
			
</details>

## 6. Red
<details>
	<summary>Diagrama de red</summary>

### 6.a Diagrama de la red


<img width="1025" height="761" alt="image" src="https://github.com/user-attachments/assets/7063ad88-f83f-47fb-a6a7-840643012833" />

	
</details>

## 7. Web
<details>
	<summary>Diseño, Mockup, Mapa de navegabilidad</summary>

## 7.d Diseño Web 

### Equilibrio del diseño, Colores y Estructura
- Mantener un uso balanceado entre espacios vacíos y elementos visuales para evitar saturaciones.
- Uso de distribución simétrica o asimétrica según el objetivo de la página.
- Colores principales: **Rojo** y **Blanco**  
  Colores secundarios: **Negro** y **Blanco**  
  Colores de estado: Éxito (**Verde**), Error (**Rojo**), Advertencia (**Amarillo**), Información (**Azul clarito**), etc.
- Estructura del diseño:  
  Header (cabecera) fijo o dinámico con menú principal.  
  Cuerpo dividido en secciones diferenciadas visualmente.  
  Sidebar (barra lateral) opcional.  
  Footer (pie de página) con enlaces legales y de contacto.

### Colores y Tipografía
- Tipografía principal: **Sans-serif** para modernidad y legibilidad.  
- Tipografía secundaria: **Serif o cursiva** para títulos y puntos destacados.  
- Tamaños con jerarquía visual (título, subtítulo, texto normal...).  
- Colores tipográficos con alto contraste, color especial para enlaces y estados.

### Componentes de Interfaz
- **Botones:** menú, acción, hipervínculo, repetidor, desplegable.  
  Estados: identificador, activado, desactivado, hover, presionado.  
- **Enlaces:** soportan estados (normal, hover, visitado).  
  Elementos interactivos: barras de búsqueda, paginación, pestañas, acordeones, etc.  
- **Casillas de verificación:** marcado, desmarcado, indeterminado.  
- **Menús desplegables:** lista de opciones, opción predeterminada, cierre animado, botones divididos.  
- **Sliders:** barra, thumb, valores mínimo/máximo, rango sombreado, horizontal o vertical.  
- **Menús deslizadores:** submenús, pestañas, breadcrumbs, sidebar secundaria, filtros y buscadores.  
- **Barras de herramientas:** acciones rápidas mediante iconos y botones.  
- **Imágenes:** responsivas, usar WebP y SVG para iconos, alt-text para accesibilidad.  
- **Formularios:** campos claros, validaciones visibles, botones enviar/reset.  
- **Notificaciones:** toasts / modales para éxito, error, advertencia, info.

### Redacción
- Redacción clara, directa y sin saturación técnica innecesaria.  
- Mantener coherencia de nombres/terminología en componentes, estructuras y esta#dos UI.

### 7.e Mockup 
En nuestra pantalla de inicio de la web "SPORTFIX", nos hemos inspirado en Netflix y deportes, con el logo de F1 y un coche de F1 en una pista de carreras. También hemos puesto un iniciar sesión y al lado un menú desplegable con su footer también con algunas noticias, pilotos, algunas razones para unirte y las políticas de nuestra web. 
		
<img width="1016" height="570" alt="image" src="https://github.com/user-attachments/assets/94747aec-3159-41f7-b05c-dcd5b039a308" />
<img width="1016" height="570" alt="image" src="https://github.com/user-attachments/assets/44a49fb4-e336-4a54-b01d-34c3f2ae26c1" />
<img width="1016" height="570" alt="image" src="https://github.com/user-attachments/assets/843a8252-6f0a-43d4-922b-72f216319ba2" />
<img width="1016" height="570" alt="image" src="https://github.com/user-attachments/assets/a3145822-e452-4083-9aad-b329e47c14e1" />
<img width="1016" height="570" alt="image" src="https://github.com/user-attachments/assets/af540d3a-364d-4c03-bb0d-db10ecc15571" />


En esta sección os mostraremos como será el apartado login / register.

<img width="451" height="359" alt="image" src="https://github.com/user-attachments/assets/99a16176-2994-482d-a974-b078a51cdd32" />


En esta sección os enseñaremos la función mi lista para guardar a tus pilotos favoritos, escuderías.
<img width="531" height="424" alt="image" src="https://github.com/user-attachments/assets/5a7f7f86-deee-4f5a-bd55-d58bc38d5497" />


En esta sección os mostraremos como será la función donde puedes modificar, añadir y eliminar perfil.
<img width="356" height="585" alt="image" src="https://github.com/user-attachments/assets/e58df532-49bc-44b0-8642-caf7d9cc7921" />


En esta sección os mostraremos como será la función del administrador.
<img width="535" height="422" alt="image" src="https://github.com/user-attachments/assets/094c38b2-66c4-4421-afdb-80300aef9dd3" />


En esta sección explicaremos "¿Quiénes somos?"de la web. Hemos mencionado los creadores que somos yo y mi compañero. Somos estudiantes de segundo año de SMX, con la intención de crear una web de noticias de F1 inspirada en Netflix, pero con el objetivo claro de parecerse a "Marca".

<img width="496" height="398" alt="image" src="https://github.com/user-attachments/assets/52f120cb-7ac4-483d-bbb8-7d0bf43385c4" />


En este apartado podemos encontrar nuevas noticias de última hora. 

<img width="496" height="396" alt="image" src="https://github.com/user-attachments/assets/3de29ac8-18a5-455a-9a96-cf18dcf719ec" />


En este apartado hablaremos sobre los pilotos como por ejemplo sobre Fernando Alonso.

<img width="493" height="397" alt="image" src="https://github.com/user-attachments/assets/2f6431b7-6184-4df1-a87e-d34f8a546189" />


En esta sección es sobre ayuda, explicamos que para acceder a la página de inicio se debe ingresar vuestro correo electrónico y la contraseña asociada a ese correo.

<img width="497" height="391" alt="image" src="https://github.com/user-attachments/assets/4f2d8bc0-5316-459b-85dd-b9d7120ea969" />

En este apartado hablaremos sobre el menú de navegación principal con varias secciones.
<img width="504" height="635" alt="image" src="https://github.com/user-attachments/assets/a440ff9b-42bf-4f81-a0c9-26d02369b5d9" />

En esta sección es sobre la historia de los pilotos de F1. Explicaremos el origen del Campeonato Mundial de Pilotos en 1950 hasta la actualidad. En la imagen podemos ver un mono plazo de Senna, un mono plazo de Max Verstappen y un Renault de Alonso.

<img width="575" height="431" alt="image" src="https://github.com/user-attachments/assets/765703f3-010e-4b78-a239-f50696d48c67" />


Hemos creado una ficha dedicada a Ayrton Senna porque fue la mejor leyenda de F1.

<img width="509" height="639" alt="image" src="https://github.com/user-attachments/assets/2bc4dd3d-ff63-481b-ae27-cb69d2de740b" />

En esta sección os hablaremos sobre los pilotos actuales.

<img width="573" height="435" alt="image" src="https://github.com/user-attachments/assets/82107f3d-8f42-48c1-83d2-00def98086d5" />

Hemos creado una ficha dedicada a Checo Perez porque fue uno de los grandes pilotos de la actualidad.

<img width="512" height="635" alt="image" src="https://github.com/user-attachments/assets/62ef6f53-5348-4266-8230-e63809ea6191" />


Una sección de escuderías. Presentamos una ilustración con los logos de Ferrari,Mercedes , Red Bull y etc. Porque hablaremos sobre las escuderías de F1 , su función ,mencionaremos los equipos más actuales y la plantilla.

<img width="572" height="432" alt="image" src="https://github.com/user-attachments/assets/ae09dc7d-055e-4c08-a5e8-211061cc74e6" />


En esta sección os mostramos la escudería de ferrari.

<img width="526" height="423" alt="image" src="https://github.com/user-attachments/assets/e4d6a2a1-e815-4789-b699-1835785fb390" />


Es una sección de los coches. En el texto descriptivo que hemos puesto describimos cómo son los mono plazos aerodinámicos , ultra-ligeros, construidos con fibra de carbono , etc.

<img width="576" height="433" alt="image" src="https://github.com/user-attachments/assets/86e3c6b0-67b1-441b-9bc7-72ad4fc1b106" />

Artículo dedicado a la escudería de Ferrari. Mostramos su logo, un coche.

<img width="383" height="627" alt="image" src="https://github.com/user-attachments/assets/831a64c6-09cb-4247-9856-afb4d53b15fb" />


### Enlace canva:
https://www.canva.com/design/DAG1Fwp_OVo/nzsDZnid_HPaMEl-ohBuFw/edit

### 7.f Mapa de navegabilidad
<details>
<sumary>Mapa de navegabilidad</sumary>
Enlace mapa de navegabilidad: https://www.figma.com/design/FBrxqjpqsaJRffB4uZcP2K/Diagrama-de-navegaci%C3%B3n?node-id=0-1&t=iLyWYkiAOAoIzT9d-1		
</details>


## 8. Servicios	
<details>
	<summary>Apartados</summary>
	
### 8.g DNS

### 8.h DHCP

8.i Apache

8.j Firewall

8.k Copias de seguridad
</details>

## 9. Diseño y programación del sitio web.
<details>
	<sumary>Diseño y programación</sumary>
9.1. Maquetación web con HTML, CSS, JS.
9.2. Crear la DB en MySQL.
9.3. Trabajar PHP.
</details>

## 10. Implementación de la infraestructura


### 10.1. Configuración un entorno de backup
<details>

</details>

### 10.2. Instalar y configurar un DNS primario 
<details>
<summary>DNS</summary>

## 1. Tecnologías a Utilizar

Servidor: Ubuntu Server / Debian. 

Servicio de Red: Netplan (YAML). 

Servicios de Infraestructura: Pi-Hole (DNS y DHCP). 

Herramientas de Diagnóstico: ip a, nslookup, ping, lsof.


## Introducción al Servicio

¿Qué es?: Un sistema de nomenclatura jerárquico que traduce nombres de dominio (legibles por humanos) en direcciones IP. 

¿Por qué es necesario?: Evita memorizar IPs, permite cambiar la IP de un servidor sin afectar el acceso por nombre y facilita la administración de servicios web o correo

## Información oficial:

(https://www.cloudflare.com/es-es/learning/dns/what-is-dns/)

https://www.ibm.com/es-es/think/topics/dns-server

https://punkymo.gitbook.io/miwiki/servicios/servidores-dns

## Detalles de la MV

Adaptador 1 (enp0s3): Adaptador Puente (Internet y panel web). 

Adaptador 2 (enp0s8): Red Interna (Servicio a clientes locales). 

Capturas necesarias: 
 
<img width="623" height="291" alt="image" src="https://github.com/user-attachments/assets/efb8e8f1-0f84-4eb5-905c-991921efff60" />

<img width="624" height="297" alt="image" src="https://github.com/user-attachments/assets/78b42adf-2ae1-4404-81d8-ccea4adccf6e" />

<img width="625" height="283" alt="image" src="https://github.com/user-attachments/assets/afaff1f3-302c-4e20-b2ac-fea63c7a2859" />


## Pasos a Seguir

Configuración de Netplan: Editar el archivo /etc/netplan/00-installer-config.yaml. 

YAML: Configurar enp0s3 con DHCP y enp0s8 con IP estática 10.10.10.254/24. 

Validación: 

Aplicar con sudo netplan apply

<img width="420" height="29" alt="image" src="https://github.com/user-attachments/assets/ca761cbb-a8f5-41d6-afe8-e0cf4f848823" />

<img width="619" height="191" alt="image" src="https://github.com/user-attachments/assets/41b95cdc-d1d3-4b90-972c-fff11fb619d9" />

Verificar con ip a. 

<img width="618" height="277" alt="image" src="https://github.com/user-attachments/assets/c9304531-7f0b-468a-bc27-76915d7a4565" />

Instalación: Ejecutar curl -sSL https://install.pi-hole.net | bash. 

<img width="464" height="433" alt="image" src="https://github.com/user-attachments/assets/ce5b2d39-8d8b-42d9-810f-6ab70e6ecd18" />

Contraseña: Establecer clave con sudo pihole setpassword. 

<img width="548" height="103" alt="image" src="https://github.com/user-attachments/assets/108fff45-cc0a-4f9f-82b9-2c10b394af18" />

Prueba: Ejecutar nslookup y ping google.com.

<img width="621" height="202" alt="image" src="https://github.com/user-attachments/assets/94ce301a-c314-4335-b453-4b816f878fe2" />

<img width="299" height="177" alt="image" src="https://github.com/user-attachments/assets/9d995c95-9f24-4fea-b6e6-799c74361e80" />

<img width="292" height="166" alt="image" src="https://github.com/user-attachments/assets/75cf54e9-acc8-4459-8c4c-c09163e8d9b9" />

## Incidencias

Error de sintaxis: Uso accidental de comandos inexistentes como tryip en lugar de try. 

<img width="409" height="22" alt="image" src="https://github.com/user-attachments/assets/f2b1cedd-f516-473b-808c-0cdc282da257" />

<img width="615" height="66" alt="image" src="https://github.com/user-attachments/assets/13ef5fb2-e434-4300-b8d3-7fd563515d76" />

Permisos: Advertencias de Netplan indicando que los permisos del archivo YAML son "too open" (demasiado abiertos).

</details>

### 10.3. Instalar y configurar un servidor DHCP 

<details>
	
<summary>DHCP</summary>

## Introducción al Servicio

¿Qué es?: Protocolo que asigna automáticamente parámetros de configuración IP (IP, máscara, DNS) a dispositivos. 

¿Por qué es necesario?: Automatiza la configuración, evita errores humanos y previene conflictos de IPs duplicadas.

## Información oficial:

https://www.fortinet.com/lat/resources/cyberglossary/dynamic-host-configuration-protocol-dhcp

https://www.redeszone.net/tutoriales/internet/que-es-protocolo-dhcp/

https://punkymo.gitbook.io/miwiki/servicios/servidores-dhcp

## Detalles de la MV

Equipo Cliente: Únicamente un adaptador en modo Red Interna.

<img width="561" height="276" alt="image" src="https://github.com/user-attachments/assets/5621955d-d69a-48b0-b68d-31cfc68a2d65" />

## Pasos a Seguir

Habilitar DHCP: Acceder a http://192.168.135.35/admin e ir a Settings -> DHCP. 

<img width="231" height="287" alt="image" src="https://github.com/user-attachments/assets/dae78ae4-8fc1-4368-8bd6-5ed2f0b73dfb" />

Verificación del Puerto: Comprobar con sudo lsof -i que el proceso pihole-FTL escucha en el puerto bootps (67 UDP) (Cap 12). 

<img width="622" height="262" alt="image" src="https://github.com/user-attachments/assets/db86cd54-bbde-43a5-8a22-e52005a04c38" />

## Prueba en Cliente

Verificar IP recibida con ip a. 

<img width="624" height="217" alt="image" src="https://github.com/user-attachments/assets/7a504df1-82b3-4680-8c0e-211a55cfd671" />

Confirmar resolución DNS con nslookup.

<img width="337" height="325" alt="image" src="https://github.com/user-attachments/assets/76be6a2e-da3d-46df-bff0-8107733ab098" />

## Incidencias

Enlace de Resolución: En caso de que el cliente no resuelva nombres, es necesario forzar el enlace simbólico del archivo resolv.conf

</details>

### 10.4. Configurar servidor APACHE

### 10.5. Configurar firewall (pfSense)
</details>

## 11. Seguridad
<details>
	<sumary>Seguridad</sumary>
11.1. Plan contigencia
11.2. Auditoria de seguridad
</details>

## 12. Control
<details> 
	<sumary>Control</sumary>
12.1. La programación de las funcionalidades
12.2. Evaluar requisito web responsive
</details>

## 13. Cierre
<details>
	<summary>Final</summary>
13.1. Cloudflare
13.2. Revisiones
</details>

## 14.Conclusiones

## 15. Bibliografía
<details>
	<summary>Bibliografía</summary>

Github (https://docs.github.com/es/get-started/start-your-journey/hello-world) , (https://gist.github.com/dasdo/9ff71c5c0efa037441b6) y (https://prestashop.es) 

MySQL (https://www.mysqltutorial.org/) y (https://blog.baehost.com/comandos-basicos-para-mysql/) 

Cloudflare (https://raiolanetworks.com/blog/cloudflare/) y (https://developers.cloudflare.com/cloudflare-one/connections/connect-networks/do-more-with-tunnels/local-management/tunnel-useful-commands/) 

Promox (https://www.nakivo.com/es/blog/top-10-proxmox-cli-commands/) y (https://www.nakivo.com/blog/proxmox-install/)
</details>
