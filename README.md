# SMX2_Sportflix

# Índice
<details>
	<summary>Apartados</summary>

Nombre del proyecto: Sportflix

1. Introducción

2. Briefing de ideas

3. Informe Backend

4. Arquitectura del software

5. Tecnologías a utilizar

6. Red

a. Diagrama de la red

b. Mapa físico

c. Mapa lógico

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

## 1. Introducción
<Details>
Estamos haciendo un projecto que consiste en crear una web que en nuestro caso es de notícias de fórmula 1 y tendrá apartados exclusivamente con pilotos 3D españoles, también su apartado de soporte para mirar los problemas frecuentes que suceden en nuestra web, su apartado de última hora y también su apartado de introducción explicando quienes somos. 
</details>

## 2. Briefing de ideas
<Details>
	 <summary>Apartados</summary> 
	  
### Idea seleccionada y justificación: 
Porque hemos escogido esta idea: Lo hemos escogido porque es original, también porque hay mucha información sobre los temas que hemos escogido para la web y para finalizar nuestra web se puede personalizar lo que también nos ayudaría a que el público este más atento a nuestra web y sea más llamativo. 

  
### Objectivos:
* 1 Crear la página web.
* 2 Diseñar còmo seria nuestra página web.. Diseñar una página web donde se mostrará noticias, pilotos, coches y otros detalles de la F1.
* 3 Importar noticias de Formula 1 de las webs fiables y oficiales.  
* 4 Guardar todos los datos en una base de datos.
* 5 Diseñar en 3D los coches a mostrar en la web y si es posible hacer lo mismo con los pilotos.


### Público al que va dirigido: 
A todos los públicos que le gusté el deporte y sobretodo la fórmula 1.

### Modulos que vamos a tocar: (Asignaturas)

### Seguridad:

MO6: Firewall: pfsense o Sophos.

MO6: Backup: Trunas y/o rsync.

MO6: Plan de contingencia y explicar los aspectos de seguridad que se han implementado o que se puedan implementar.

MO4: Diferenciar roles de usuarios en el sistema.

### Servicios de red:

MO5-MO6: Diagrama de red, mapa físico, mapa lógico de la infraestructura.

MO4-MO7: Servicio DHCP en un servidor Windows diferente.

MO7: Servidor DNS primario.

### Sistemas operativos:

MO4: Instalación y configuración de sistemas operativos (Windows Server / Linux) para alojar los diferentes servicios del proyecto.

MO4: Gestión de usuarios, grupos y permisos para diferenciar roles dentro del sistema (administrador, desarrollador, visitante).

MO4: Configuración de servidores necesarios para el funcionamiento de la web (Apache, DNS, DHCP, etc.).

MO4: Administración y monitorización del sistema para garantizar su correcto rendimiento y seguridad.

MO4: Virtualización de los diferentes servidores y estaciones de trabajo utilizando herramientas como VirtualBox, VMware o Proxmox.

MO4: Implementación de políticas básicas de seguridad y actualización del sistema operativo.

MO4: Automatización de tareas administrativas mediante scripts (bash o PowerShell).

### Aplicaciones web:

MO8: Mapa de navegabilidad y Mockups.

MO8: Web responsive.

### Programación (optativa)

MO8: HTML (estructura básica de páginas web).

MO8: CSS (diseño y estilos de páginas web).

MO8: JavaScript (funcionalidades interactivas).

### Materiales necesarios (fisicos y lógicos).
  Físicos: Tener una libreta a mano para apuntar ideas, comandos, así podernos organizar, ordenador.

  Lógicos: Tener el drive del proyecto abierto, visual studio instalado, enlaces a recursos para hacer el proyecto, trello, github y tener el microsoft office abierto para hacer la
  infraestructura de red.
  </details>
  
### Recursos
<Details>
	 <summary>Nuestros Recursos</summary>

## Bibliografia: 

Github (https://docs.github.com/es/get-started/start-your-journey/hello-world) , (https://gist.github.com/dasdo/9ff71c5c0efa037441b6) y (https://prestashop.es)
MySQL (https://www.mysqltutorial.org/) y (https://blog.baehost.com/comandos-basicos-para-mysql/)
Cloudflare (https://raiolanetworks.com/blog/cloudflare/) y (https://developers.cloudflare.com/cloudflare-one/connections/connect-networks/do-more-with-tunnels/local-management/tunnel-useful-commands/)
Promox (https://www.nakivo.com/es/blog/top-10-proxmox-cli-commands/) y (https://www.nakivo.com/blog/proxmox-install/)
</Details>


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

MySQL Workbench: https://github.com/Eulalia17/SMX_2Sportflix/blob/main/Diagrama%20base%20de%20datos%20Sportflix.mwb
https://raw.githubusercontent.com/Eulalia17/SMX_2Sportflix/main/Diagrama%20base%20de%20datos%20Sportflix.mwb



</details>


## 4. Arquitectura del software
<details> 
	<sumary>Apartados</sumary>
</details>

## 5. Tecnologías a utilizar

## 6. Red
<details>
	<summary>Diagrama de red y mapas lógicos y físicos</summary>

### 6.a Diagrama de la red

<img width="1025" height="761" alt="image" src="https://github.com/user-attachments/assets/7063ad88-f83f-47fb-a6a7-840643012833" />


### 6.b Mapa físico


### 6.c Mapa lógico
	
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
<sumary>Mapa de navegabilidad</sumary>
		
</details>


## 8. Servicios	
<details>
	<summary>Apartados</summary>
	
8.g DNS

8.h DHCP

8.i Apache

8.j Firewall

8.k Copias de seguridad
</details>

## 9. Conclusiones


## 10. Bibliografía
<details>
	<summary>Bibliografía</summary>

Github (https://docs.github.com/es/get-started/start-your-journey/hello-world) , (https://gist.github.com/dasdo/9ff71c5c0efa037441b6) y (https://prestashop.es) 

MySQL (https://www.mysqltutorial.org/) y (https://blog.baehost.com/comandos-basicos-para-mysql/) 

Cloudflare (https://raiolanetworks.com/blog/cloudflare/) y (https://developers.cloudflare.com/cloudflare-one/connections/connect-networks/do-more-with-tunnels/local-management/tunnel-useful-commands/) 

Promox (https://www.nakivo.com/es/blog/top-10-proxmox-cli-commands/) y (https://www.nakivo.com/blog/proxmox-install/)
</details>
