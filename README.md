# SMX2_Sportflix

## Índice
<details>
	<summary>Apartados</summary>

Nombre del proyecto: SMX2-Sportflix

1.Introducción - ¿qué estamos haciendo?

2.Briefing de ideas

3.Informe Backend

4.Arquitectura del software

5.Tecnologías a utilizar

6.Red

a.Diagrama de la red

b.Mapa físico

c.Mapa lógico

7.Web

d.Diseño

e.Mockup

f.Mapa de navegabilidad

8.Servicios

g.DNS

h.DHCP

i.Apache

j.Firewall

k.Copias de seguridad

9.Conclusiones

10.Bibliografía

</details>

### 1.Introducción - ¿qué estamos haciendo?
<details>
	<summary>Explicación</summary>
Estamos haciendo un projecto que consiste en crear una web que en nuestro caso es de notícias de fórmula 1 y tendrá apartados exclusivamente con pilotos 3D españoles, también su apartado de soporte para mirar los problemas frecuentes que suceden en nuestra web, su apartado de última hora y también su apartado de introducción explicando quienes somos. 
</details>

  ### 2.Briefing de ideas
  <details>
	 <summary>Apartados</summary> 
	  
### Idea seleccionada y justificación: 
Porque hemos escogido esta idea: Lo hemos escogido porque es original, también porque hay mucha información sobre los temas que hemos escogido para la web y para finalizar nuestra web se puede personalizar lo que también nos ayudaría a que el público este más atento a nuestra web y sea más llamativo. 

  
### Objectivos:
* 1 Crear la página web.
* 2 Diseñar còmo seria nuestra página web.. Diseñar una página web donde se mostrará noticias, pilotos, coches y otros detalles de la F1.
* 3 Importar noticias de Formula 1 de las webs fiables y oficiales.  
* 4 Guardar todos los datos en una base de datos.
* 5 Diseñar en 3D los coches a mostrar en la web y si es posible hacer lo mismo con los pilotos.


### Publico al que va dirigido: 
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
<details>
<summary> Para el diseño web </summary>
	Equilibrio del diseño:
	<details> 
		Uso balanceado entre espacios vacíos y elementos visuales para evitar las saturaciónes.
	    Las distribuciónes simétrica y la asimétrica según el objetivo que nosotros le queremos dar a nuestra pagina web.
	</details>
	Colores del diseño:
	<details> 
		Colores principales: rojo y blanco.
		Colores secundarios : negro y blanco.
		Colores de estado: Exito (Verda), Error (Rojo), Advertencia (Amarillo), Información (Azul clarito), etc.
	</details>
	Estrucutra del diseño:
	<detail>
		Header(cabacera) fijo o dinámico con menú principal.
		Cuerpo divido en secciones claras y visualmente diferenciadas.
		Sideabar (barra lateral) opcional para navegación o contenido adicional.
		Footer (pie de página) con enlaces legales y de contacto.
	</detail>
	Colores y tipografía:
	<details>
		Colores lo he mencionando anterior mente.
		Tipografia principal: sans-serif para modernidad y legibilidad.
		Tipografia secundaria: serif o cursiva para títulos o énfasis.
		Tamaños jerárquicos: titulo, subtitulos, texto normal,etc.
		Colores tipograficos: alto contraste con fondo, color para enlaces y estados.
	</details>
	Componentes de interfaz 
	<details>
		Botones. 
		<details>
			Tipos: Menú, botón de acción, botón de hipervínculo, botón repetidor, botón  desplegable.
			Estados: Identificador, activado, desactivado, sobrevolado (hover), presionado (avive).
			Estilos: Colores y sombras para cada estado.
		</details>
		Enlaces:
		<details>
			Interactivos: barras de búsqueda, paginación.
			Contenedores: pestañas, acordeones, etc.
			Controles: navegación, contenido informativo, estructuras.
			Soporte para diferentes estados (normal,hover,visitado,etc).
		</details>
		Casillas de verificación:
		<details>
			Componentes: caja, marca de verificación, etiqueta.
			Estados: marcado, desmarcado, indeterminado (por ejemplo, en selección múltiple parcial).
		</details>
		Menús desplegables:
		<details> 
			Elementos: botones, iconos, control activador.
			Lista de opciones con indicador de opción predeterminada.
			Etiquetas claras y cierre con animación.
			Uso de clases CSS para estilos y estados.
			Botones divididos para funciones combinadas (por ejemplo, acción + menú).
		</details>
		Deslizadores (sliders)
		<details> 
			Componentes: barra, manija (thumb), valor numérico.
			Etiquetas claras para valores mínimos y máximos.
			Marcas para intervalos o puntos destacados.
			Área sombreada para rango seleccionado.
			Dirección: horizontal o vertical.
			Eventos para interacción (drag, click).
		</details>
		Menús deslizadores:
		<details> 
			Principal con submenús desplegables.
			Pestañas para secciones.
			Menú de pie de página con enlaces secundarios.
			Panel lateral (sidebar) con navegación secundaria.
			Breadcrumbs (migas de pan) para orientación.
			Botón para volver a página inicio.
			Widgets de navegación adicionales (filtros, buscadores).
		</details>
		Barras de herramientas:
		<details> 
			Conjunto de iconos y botones para acciones ràpidas.
		</details>
		Barras de búsquedas
		<details>
			Campo de texto con botón o icono de búsqueda.
			Autocompletado y sugerencias.
		</details>
		Pestañas:
		<details>
			Navegación de pestañas para continido relacionado.
			Cambio de estado visual y de continido según pestaña activa.
		</details>
		Botones de retroceso
		<details> 
			Iconos o botones para regresar a la página anterior.
		</details>
		Imagénes
		<details> 
			Soporte para imagénes responsivas.
			Uso de formatos optimizados (webpp, svg para iconos).
			Alt-text para accesibilidad.
		</details>
		Cabeceras
		<details> 
			Jerarquia clara (h1, h2, h3, etc).
			Diseño con separación y posible uso de iconos o elementos gráficos.
		</details>
		Pies de página:
		<details>
			Información de contacto, redes sociales, enlaces legales y mapa del sitio.
		</details>
		Barras laterales:
		<details>
			Contenido adicional: widgets, publicidad, navegación secundaria, etc.
		</details>
		Áreas de cuerpo de la página:
		<details> 
			Zonas bien definidas para contenido principal.
			Uso de tarjetas, listas, o grids según contenido.
		</details>
		Formularios:
		<details> 
			Campos claros y accesibles.
			Validaciones visibles.
			Botones de envío y reset.
		</details>
		Notificaciones:
		<details> 
			Mensajes emergentes (toast, modales) con estados: éxito, error, advertencia, info.
			Posición fija (arriba o abajo) para no interferir con el contenido.
		</details>


### 7f.Mapa de navegabilidad
<details>
	<sumary>Apartado</sumary>
		</details>




### 8.Servicios	
