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

## 2.Briefing de ideas
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

Seguridad:

Servicios de red:

Sistemas operativos:

Seguretat:

Aplicaciones web

Programación (optativa)

* MO5-MO6 -> Diagrama de red,mapa fisico,mapa lógico de la infraestrucutra.
* MO4-MO7 -> Servicio DHCP en un servidor Windows diferente.
* MO7 -> Servidor DNS primario.
* MO6 -> Firewall: pfsense o Sophos.
* MO6 -> Backup: Trunas y/o rsync.
* MO8 -> Mapa de navegabilidad y Mockups.
* MO8 -> web responsive.
* MO4 -> Diferenciar roles de usuarios en el sistema.
* MO6 -> Plan de contigencia y explicar los aspects de seguridad que se han implementado o que se puedan implementar.

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
</details>


## 4. Arquitectura del software
<details> 
	<sumary>Apartados</sumary>
</details>

## 5. Tecnologías a utilizar

## 6.Red
<details>
	<summary>Apartados</summary>
6a.Diagrama de la red


6.b.Mapa físico


6.c.Mapa lógico
	
</details>

## 7. Web
<details>
	<summary>Diseño, Mockup, Mapa de navegabilidad</summary>

## 7.d Diseño Web - Lineamientos Base

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

### 7e.Mockup 
En nuestra pantalla de inicio de la web "SPORTFIX", nos hemos inspirado en Netflix y deportes, con el logo de F1 y un coche de F1 en una pista de carreras. También hemos puesto un iniciar sesión y al lado un menú desplegable con su footer también con algunas noticias, pilotos, algunas razones para unirte y las políticas de nuestra web. 
		
<img width="1016" height="570" alt="image" src="https://github.com/user-attachments/assets/94747aec-3159-41f7-b05c-dcd5b039a308" />
<img width="767" height="435" alt="image" src="https://github.com/user-attachments/assets/44a49fb4-e336-4a54-b01d-34c3f2ae26c1" />
<img width="874" height="440" alt="image" src="https://github.com/user-attachments/assets/843a8252-6f0a-43d4-922b-72f216319ba2" />
<img width="876" height="399" alt="image" src="https://github.com/user-attachments/assets/3bcd5b00-654e-4261-8240-2839a154eabc" />
<img width="634" height="420" alt="image" src="https://github.com/user-attachments/assets/af540d3a-364d-4c03-bb0d-db10ecc15571" />
		
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

Una ficha dedicada a Max Verstappen, es el terror en la pista de carreras.

<img width="508" height="636" alt="image" src="https://github.com/user-attachments/assets/524cbc36-5ba2-41f6-946b-e7d42979deba" />

Una ficha al mejor español de la historia Fernando Alonso, porque hay una buena rivalidad popular en redes sociales que es entre él o Hamilton y hemos elegido a Alonso.

<img width="508" height="636" alt="image" src="https://github.com/user-attachments/assets/7cdea7a2-8007-43a4-a39d-dad4418a6121" />

Una ficha al segundo mejor piloto español a Carlitos Sainz Vázquez de Castro (Smooth Operator).

<img width="508" height="638" alt="image" src="https://github.com/user-attachments/assets/36122147-442e-4b5d-bbd6-d2c508e2d5a1" />

Una ficha a Charles Lecler,porque tuvo el peor pasado de todos los pilotos y porque es el mejor amigo de Carlitos.

<img width="512" height="635" alt="image" src="https://github.com/user-attachments/assets/8fe64e21-dca2-42f9-a277-b5784e24726b" /> 

Una ficha a Oscar Piastri,porque siendo joven tiene mucho talento y carisma a la hora de conducir un coche.

<img width="510" height="641" alt="image" src="https://github.com/user-attachments/assets/154242e1-1ac8-469a-be65-6a4f96437d0c" />

Una ficha a Lando Norris , porque aunque tiene talento , es de papaya rules (un apodo que esta Oscar también está incluido), algunas personas no le gusta su actitud pero a mi si.

<img width="508" height="634" alt="image" src="https://github.com/user-attachments/assets/5d38e4da-1e2c-4439-a301-90c0653aeb6b" />

Una sección de escuderías. Presentamos una ilustración con los logos de Ferrari,Mercedes , Red Bull y etc. Porque hablaremos sobre las escuderías de F1 , su función ,mencionaremos los equipos más actuales y la plantilla.

<img width="572" height="432" alt="image" src="https://github.com/user-attachments/assets/ae09dc7d-055e-4c08-a5e8-211061cc74e6" />

Es una sección de los coches. En el texto descriptivo que hemos puesto describimos cómo son los mono plazos aerodinámicos , ultra-ligeros, construidos con fibra de carbono , etc.

<img width="798" height="634" alt="image" src="https://github.com/user-attachments/assets/b838e5d2-101c-4266-9b96-1ed38378e8b4" />

Artículo dedicado a la escudería de Ferrari. Mostramos su logo, un coche.

<img width="383" height="627" alt="image" src="https://github.com/user-attachments/assets/831a64c6-09cb-4247-9856-afb4d53b15fb" />

El artículo sobre McLaren con su descripción resalta que McLaren (sigue innovando en cada carrera y desafiando los límites).

<img width="415" height="639" alt="image" src="https://github.com/user-attachments/assets/f624c7f1-d368-4d2a-aa33-5e89f03223bb" />

Artículo de Williams , hemos puesto un breve descripción (ha demostrado su excelencia en la F1 y anima a descubrir más sobre su historia).

<img width="359" height="637" alt="image" src="https://github.com/user-attachments/assets/07a81988-369a-4fc7-a985-0a96f219944d" />

Artículo de Red Bull , hemos puesto de titular (la escudería red bull en la f1 ). Invitando a descubrir su historia y los éxitos.

<img width="351" height="625" alt="image" src="https://github.com/user-attachments/assets/e94d7166-b6eb-4b6b-9da5-394467790fcc" />

Artículo de Mercedes, hemos puesto de descripción(la velocidad y precisión de Mercedes).  

<img width="376" height="636" alt="image" src="https://github.com/user-attachments/assets/5224e54e-5750-45ff-bef7-f1bddfb50b52" />
</details>


### 7f.Mapa de navegabilidad
<details>
	<sumary>Apartado</sumary>
		
</details>


## 8.Servicios	
<details>
	<summary>Apartados</summary>
	
8.g DNS

8.h DHCP

8.i Apache

8.j Firewall

8.k Copias de seguridad
</details>

## 9. Conclusiones


## 10.Bibliografía
<details>
	<summary>Bibliografía</summary>
Github (https://docs.github.com/es/get-started/start-your-journey/hello-world) , (https://gist.github.com/dasdo/9ff71c5c0efa037441b6) y (https://prestashop.es) MySQL (https://www.mysqltutorial.org/) y (https://blog.baehost.com/comandos-basicos-para-mysql/) Cloudflare (https://raiolanetworks.com/blog/cloudflare/) y (https://developers.cloudflare.com/cloudflare-one/connections/connect-networks/do-more-with-tunnels/local-management/tunnel-useful-commands/) Promox (https://www.nakivo.com/es/blog/top-10-proxmox-cli-commands/) y (https://www.nakivo.com/blog/proxmox-install/)
</details>
