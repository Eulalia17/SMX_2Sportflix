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
	<summary>Apartados</summary>

7.d Diseño


7.e Mockup 

## Diseño Web - Lineamientos Base

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
- Mantener coherencia de nombres/terminología en componentes, estructuras y estados UI.



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
