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

## 💡 2. Briefing de ideas
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
  <summary>&#8203;</summary> <!-- desplegable vacío -->

**Bibliografía:**  
- Github: [Docs GitHub](https://docs.github.com/es/get-started/start-your-journey/hello-world), [Gist](https://gist.github.com/dasdo/9ff71c5c0efa037441b6)  
- PrestaShop: [prestashop.es](https://prestashop.es)  
- MySQL: [Tutorial MySQL](https://www.mysqltutorial.org/), [Comandos básicos](https://blog.baehost.com/comandos-basicos-para-mysql/)  
- Cloudflare: [Blog Cloudflare](https://raiolanetworks.com/blog/cloudflare/), [Developers](https://developers.cloudflare.com/cloudflare-one/connections/connect-networks/do-more-with-tunnels/local-management/tunnel-useful-commands/)  
- Proxmox: [Top comandos CLI](https://www.nakivo.com/es/blog/top-10-proxmox-cli-commands/), [Instalación](https://www.nakivo.com/blog/proxmox-install/)

</details>

## 🗄️3. Informe Backend
<details>
  <summary>&#8203;</summary> <!-- desplegable vacío -->

### 1. Descripción general del proyecto web
- **¿De qué trata tu web?**  
  Crear una web de noticias de Fórmula 1 centrada en pilotos españoles, con visualización de sus coches en 3D al visitar su perfil.  
  (*Puede incluir algún piloto de otros países si se desea.*)

- **¿Qué funcionalidades ofrecerá a los usuarios?**  
  * Crear una cuenta (registro y login).  
  * Ver últimas noticias de los pilotos.  
  * Apartado de favoritos para guardar pilotos preferidos.  
  * Interactuar con elementos de la web como pilotos y coches.

### 2. Identificación de entidades principales
- **Usuarios:** nombre, apellidos, correo electrónico, contraseña, número de identificación, fecha de registro.  
- **Piloto:** nombre, nacionalidad, estadísticas, número, equipo, edad, posición en carreras, trofeos, victorias, poles, mejor puesto.  
- **Coche:** modelo, marca, color, escudería, eslogan, motor, cilindrada, tipo de motor, fabricante de motor, patrocinadores.  
- **Noticias:** origen de la web, fecha, hora, calendario de carreras, resultados, clasificación de pilotos, palmarés, clasificación de constructores.

**¿Por qué necesitamos guardarla en la base de datos?**  
Para asegurar que toda la información importante esté organizada, accesible y dividida por apartados.

### 3. Datos que se deben guardar de cada entidad (atributos)
- Nombre  
- Apellidos  
- Correo electrónico  
- Número de identificación  
- Contraseña  
- Fecha de registro  

**Tipos de datos recomendados:** varchar, int, decimal, date, datetime, auto_increment, links según corresponda.

### 4. Relaciones entre las entidades
<img width="659" height="415" alt="image" src="https://github.com/user-attachments/assets/b815cd48-8405-49c0-bd90-d58f80f554d1" />

- Usuarios → Auditoria: relación 1:N  
- Usuarios ↔ Pilotos: relación N:N mediante tabla intermedia `Pilotos_favoritos`  
- Escuderías → Pilotos: relación 1:N  
- Escuderías → Coches: relación 1:N  
- Pilotos ↔ Noticias: relación N:N mediante `Pilotos_has_Noticias`  
- Escuderías ↔ Noticias: relación N:N mediante `Escuderías_has_Noticias`  
- Coches ↔ Noticias: relación N:N mediante `Noticias_has_Coches`  

### 5. Ejemplo de datos (simulación)
- **Usuario:**  
  Nombre: Pepe  
  Apellido: Morientes  
  Correo: pepem@gmail.com  
  ID: Pep2345  
  Contraseña: ppm75345  
  Fecha registro: 11-09-25 15:40:25  

### 6. Reflexiones, dificultades y dudas
- **Dificultades:** definir todas las funcionalidades a ofrecer a los usuarios, ya que podrían surgir nuevas ideas a lo largo del proyecto.  
- **Dudas:** si es necesario almacenar el número de identificación, dado que nombre y apellidos podrían ser suficientes.

### 7. Diagrama de base de datos
- Primer borrador realizado en Canva, luego finalizado en MySQL Workbench.
  <img width="1103" height="641" alt="image" src="https://github.com/user-attachments/assets/65418b17-ff1d-402d-9c34-eaa50a0586d0" />
- Cambios realizados:  
  * Tabla `Lista` → Tabla intermedia `Pilotos_favoritos`.  
  * Tabla `Marcas` eliminada (info incluida en `Escudería`).  
  * Tabla `Historial` → `Auditoria_registro` (atributo `acción` eliminado).  
  * Tabla `Ayuda` eliminada (manual estático en la web).  
  * Tabla `Perfil` eliminada (datos incluidos en `Usuarios`).  
<img width="777" height="479" alt="image" src="https://github.com/user-attachments/assets/842edf6b-bef1-42b8-ba4a-2d1b2e796c74" />

**Enlaces:**
- [Diagrama Canva](https://www.canva.com/design/DAG4k7iY37E/NoqqAwjC69FU2OK2PILwGA/edit)  
- [Diagrama MySQL Workbench](\Diagrama base de datos Sportflix.mwb)  

</details>


## 🏗️ 4. Arquitectura del software
<details>
  <summary>&#8203;</summary> <!-- desplegable vacío -->

### Funcionalidades
En este apartado se asignan requisitos y funcionalidades, indicando prioridades y fechas de entrega, estado actual y objetivos.

### Objetivos

<details>
  <summary>Objetivo 1: Implementar un servidor web</summary>
  1.1 Instalación y configuración básica del servidor (Ubuntu Server 22.04, IP estática, hostname, SSH).  
  1.2 Configuración de usuarios y privilegios (sudo, grupos, seguridad SSH).  
  1.3 Instalación y configuración de Apache, MySQL, PHP 8.2 y phpMyAdmin.  
  1.4 Clonado del repositorio del proyecto en el directorio web y comprobación final.
</details>

<details>
  <summary>Objetivo 2: Programar la front-page (Visual Studio)</summary>
  2.1 Crear la estructura del index.html con CSS (landing page accesible y clara).  
  2.2 Programar header y footer globales para todas las páginas.  
  2.3 Programar formulario de contacto con validaciones HTML5.
</details>

<details>
  <summary>Objetivo 3: Servidor MySQL</summary>
  3.1 Instalar y configurar MV con Ubuntu Server 22.04 LTS.  
  3.2 Instalar MySQL 8.0 y gestionar bases de datos.  
  3.3 Instalar phpMyAdmin para administración web de la base de datos.
</details>

<details>
  <summary>Objetivo 4: Servidor web</summary>
  4.1 Configurar MV con Ubuntu Server 22.04.  
  4.2 Instalar Apache y PHP según guía.  
  4.3 Definir el dominio: https://sportflix.com/
</details>

<details>
  <summary>Objetivo 5: Servidor DNS</summary>
  5.1 Configurar MV con Ubuntu Server 22.04.  
  5.2 Instalar y configurar Pi-hole como servidor DNS.
</details>

<details>
  <summary>Objetivo 6: Servidor TRUENAS + RSYNC</summary>
  6.1 Instalar y configurar MV con Truenas 25.04.2.6 (FreeBSD 64 bits).  
  6.2 Configurar dataset, protocolo SMB y permisos completos.  
  6.3 Crear MV Linux para Rsync y transferir archivos mediante red.
</details>

### Arquitectura del sistema
- Diagramas de arquitectura mostrando servidores, bases de datos, clientes y conexiones de red.  
- Integración de servicios web, backend y base de datos.  

<img width="911" height="361" alt="image" src="https://github.com/user-attachments/assets/0e271397-e234-414d-b4a9-91ec4283ac16" />

<img width="915" height="372" alt="image" src="https://github.com/user-attachments/assets/9c88b829-54d7-4aa7-a70f-e66ed6eb6b41" />

<img width="911" height="232" alt="image" src="https://github.com/user-attachments/assets/32f9229f-38ed-4fa9-8695-c69b1f1152c7" />

<img width="911" height="140" alt="image" src="https://github.com/user-attachments/assets/72184075-c32a-4e19-9522-5e4cf1cfd0f1" />

### Diagrama de la base de datos
- Tablas principales: Administración, Usuarios, Pilotos, Escuderías, Noticias, Coches, Auditoría.  
- Tipos de datos recomendados: INT, VARCHAR, DATETIME, TEXT, ENUM, AUTO_INCREMENT, según corresponda.  
- Relaciones:
  * Usuarios → Auditoría: 1:N  
  * Usuarios ↔ Pilotos: N:N (`Pilotos_favoritos`)  
  * Escuderías → Pilotos/Coches: 1:N  
  * Pilotos ↔ Noticias: N:N (`Pilotos_has_Noticias`)  
  * Escuderías ↔ Noticias: N:N (`Escuderías_has_Noticias`)  
  * Coches ↔ Noticias: N:N (`Noticias_has_Coches`)  

<img width="802" height="529" alt="image" src="https://github.com/user-attachments/assets/25a4fa83-df89-46a4-aa32-1d6658d3677a" />

</details>



## 🧰 5. Tecnologías a utilizar
<details>
  <summary>&#8203;</summary> <!-- desplegable vacío -->

### 1. Hardware

#### 1.1 Router del aula
- Se utilizará para proporcionar conexión de red a todos los equipos y gestionar el tráfico interno y externo de Internet.

#### 1.2 Servidor

##### 1.2.1 TrueNAS
- **Versión:** 25.04.2.6  
- Se utilizará para alojar servicios como páginas web, base de datos y almacenamiento en red, además de centralizar recursos y copias de seguridad.

##### 1.2.2 Apache
- **Versión:** 2.4.x estable  
- Servidor web encargado de alojar y servir el contenido de la aplicación Sportflix.

##### 1.2.3 MySQL
- **Versión:** 8.0.x LTS  
- Sistema gestor de bases de datos para almacenar toda la información del proyecto.

#### 1.3 HDD para Backup
- Disco duro destinado a realizar copias de seguridad y evitar la pérdida de datos ante fallos del sistema.

---

### 2. Sistemas Operativos

#### 2.1 Ubuntu Server
- **Versión:** Ubuntu Server LTS  
- Se utilizará para gestionar y ejecutar los servicios del servidor web y de base de datos.

---

### 3. Interfaz de Usuario (Frontend)

#### 3.1 HTML5
- Define la estructura base de las páginas web.

#### 3.2 CSS3
- Se utiliza para el diseño visual y estilos de la web.

#### 3.3 JavaScript
- **Versión:** ES2020  
- Aporta interactividad y contenido dinámico a la web.

#### 3.4 Bootstrap
- **Versión:** Bootstrap 5  
- Framework utilizado para crear una web responsive y visualmente atractiva.

---

### 4. Lógica de Negocio (Backend)

#### 4.1 PHP
- **Versión:** PHP 8.4  
- Lenguaje utilizado para el desarrollo del backend y la lógica de la aplicación.

---

### 5. Servidor Web

#### 5.1 Apache
- **Versión:** Apache 2.4  
- Gestiona las peticiones HTTP y sirve las páginas web.

#### 5.2 PHP
- **Versión:** PHP 8.4  
- Ejecuta el código del backend en el servidor.

---

### 6. Base de Datos

#### 6.1 MySQL
- **Versión:** MySQL 8.0  
- Almacena y gestiona los datos del proyecto.

---

### 7. Sistema Gestor de Base de Datos

#### 7.1 phpMyAdmin
- Interfaz web para la administración de bases de datos MySQL.

</details>


## 🌐 6. Red
<details>
	<summary>&#8203;</summary> <!-- desplegable vacío -->

Este proyecto consiste en el diseño y despliegue de una infraestructura de red segura para la plataforma web Sportflix. El objetivo principal es crear un entorno robusto que permita ofrecer servicios en línea a usuarios externos, garantizando que el tráfico sea fluido y que la información crítica esté protegida frente a posibles amenazas o fallos del sistema.

En el esquema visualizamos una estructura dividida en tres capas: el acceso externo gestionado por Cloudflare, el núcleo de red controlado por un firewall pfSense, y la capa de servicios donde residen el servidor web y la base de datos. Cada componente está interconectado de forma lógica para que la comunicación sea eficiente y esté bajo supervisión constante.

La seguridad es el eje central de la implementación. Utilizamos pfSense como puerta de enlace inteligente para filtrar todas las peticiones, mientras que un servidor DNS y DHCP organiza el direccionamiento interno. Además, el uso de Cloudflare añade una capa de protección adicional contra ataques externos antes de que el tráfico llegue siquiera a nuestro router.

Para la parte funcional, estamos utilizando el estándar de la industria mediante un servidor Apache. Este se encarga de procesar el código PHP y servir la interfaz visual construida con HTML5, CSS3 y JavaScript, permitiendo que el cliente final disfrute de una experiencia dinámica y moderna al navegar por la aplicación.

Finalmente, la gestión de datos se realiza de forma independiente para asegurar la integridad de la información. La base de datos MySQL se apoya en un sistema de almacenamiento TrueNAS y discos dedicados para backups, lo que garantiza que, ante cualquier eventualidad técnica, los datos de Sportflix siempre puedan ser recuperados rápidamente.

### 6.a Diagrama de la red


<img width="1025" height="761" alt="image" src="https://github.com/user-attachments/assets/7063ad88-f83f-47fb-a6a7-840643012833" />

	
</details>

## 🖥️ 7. Web 
<details>
  <summary>&#8203;</summary> <!-- desplegable vacío -->

---

## 7. Diseño Web

### Equilibrio del diseño, colores y estructura
- Uso equilibrado de espacios en blanco y elementos visuales para evitar saturación.
- Distribución simétrica o asimétrica según el objetivo de cada página.
- **Colores principales:** Rojo y Blanco  
- **Colores secundarios:** Negro y Blanco  
- **Colores de estado:**  
  - Éxito (Verde)  
  - Error (Rojo)  
  - Advertencia (Amarillo)  
  - Información (Azul claro)
- **Estructura general del diseño:**
  - Header (cabecera) fijo o dinámico con menú principal.
  - Cuerpo dividido en secciones visualmente diferenciadas.
  - Sidebar (barra lateral) opcional.
  - Footer (pie de página) con enlaces legales y de contacto.

---

### Colores y tipografía
- Tipografía principal: **Sans-serif** para mayor legibilidad.
- Tipografía secundaria: **Serif o cursiva** para títulos o elementos destacados.
- Jerarquía visual clara (títulos, subtítulos y texto).
- Alto contraste en textos y colores diferenciados para enlaces y estados.

---

### Componentes de interfaz
- **Botones:** menú, acción, hipervínculo, repetidor y desplegable.  
  Estados: activo, desactivado, hover, presionado.
- **Enlaces:** estados normal, hover y visitado.
- **Elementos interactivos:** buscador, paginación, pestañas y acordeones.
- **Checkbox:** marcado, desmarcado e indeterminado.
- **Menús desplegables:** opciones dinámicas con animaciones.
- **Sliders:** valores mínimo/máximo, horizontal o vertical.
- **Menús deslizables:** submenús, breadcrumbs, filtros y sidebar secundaria.
- **Barras de herramientas:** iconos y botones de acceso rápido.
- **Imágenes:** responsive, uso de WebP/SVG y texto alternativo.
- **Formularios:** validaciones claras y botones de acción.
- **Notificaciones:** modales y toasts para éxito, error, advertencia e información.

---

### Redacción
- Lenguaje claro, directo y sin tecnicismos innecesarios.
- Coherencia en nombres, componentes y estructuras de la interfaz.

---

## 7. Mockup

### Pantalla principal

La pantalla de inicio de **SPORTFIX** está inspirada en Netflix y el mundo del deporte.  
Incluye el logo de F1, un coche en pista, acceso a iniciar sesión, menú desplegable y un footer con noticias, pilotos, motivos para unirse y políticas de la web.

<img src="https://github.com/user-attachments/assets/94747aec-3159-41f7-b05c-dcd5b039a308" />
<img src="https://github.com/user-attachments/assets/44a49fb4-e336-4a54-b01d-34c3f2ae26c1" />
<img src="https://github.com/user-attachments/assets/843a8252-6f0a-43d4-922b-72f216319ba2" />
<img src="https://github.com/user-attachments/assets/a3145822-e452-4083-9aad-b329e47c14e1" />
<img src="https://github.com/user-attachments/assets/af540d3a-364d-4c03-bb0d-db10ecc15571" />

### Login / Register

Nos muestra dos tarjetas blancas una al lado de a la otra sobre un fondo negro, correspondientes a los forularios de entrada de una aplicación.

Lado izquierdo , podemos observer el login. Contiene campos para "Correro electrónico", "contraseña", un enlace de "¿Olvidaste tu contraseña?" y un botón rojo que dice Login.

Lado derecho, podemos ver por donde mas adelante nos registraremos . Incluyendo campos para "nombre,correro electronico y contraseña". Ofrece la opción de "inciar sesión con "mediantes logo de google.

<img src="https://github.com/user-attachments/assets/99a16176-2994-482d-a974-b078a51cdd32" />

### Mi lista (pilotos y escuderías favoritas)

Muestra una interfaz de seleción o gestión de elementos.
Bajo el titulo de "mi lista", se presenta una cuadrícula de tres columnas con etiquetas que van desde "lista 1" hasta "lista 19".

<img src="https://github.com/user-attachments/assets/5a7f7f86-deee-4f5a-bd55-d58bc38d5497" />

### Gestión de perfiles

Representa la sección de configuración del perfil de usuario. 
Elementos visuales. Debajo del titulo "Perfil", aparecen dos iconos circulares relacionados con los coches de carreras "automovilismo" (uno con un coche de Fórmula 1 y otro con el logotipo oficial de F1).
Botones un boton central que dice eliminar/crear nuevo perfil.Otro boton en la parte inferior para confirmar los cambios realicados.

<img src="https://github.com/user-attachments/assets/e58df532-49bc-44b0-8642-caf7d9cc7921" />

### Panel de administrador

Una interfaz de gestion organizada en una cuadrícula con varios módulos de control.Secciones el panel se divide en ocho categorias principales: Pilotos, Coches, Marcas, Escuderias, Noticias, Ayuda, Cuentas y Listas. Funcionalidad cada categoria dispone de un boton rojo que permite realizar acciones de mantenimiento.

<img src="https://github.com/user-attachments/assets/094c38b2-66c4-4421-afdb-80300aef9dd3" />

### ¿Quiénes somos?

Un apartado de la presentacion del equipo detras del proyecto, con una estética fuertemente inspirada en el automovilismo. Visauales presenta el logotipo oficial de la F1 (Formula 1) en la parte superior y una ilustración de un monoplaza rojo en un circuito de carreras en la parte inferior. Texto informativo nos indica que los creadores son Eulalia y David, alumnos de SMX2. Explican que su intención es crear una web de noticias de F1 inspirada visualmente en Netflix, pero con un enfoque de contenido similar al diario Marca.

<img src="https://github.com/user-attachments/assets/52f120cb-7ac4-483d-bbb8-7d0bf43385c4" />

### Noticias de última hora

Una interfaz de noticias de ultima hora con un deseño de tarjetas deslizables.
Encabezado titulo principal "news" y subtitulo "noticias de última hora"sobre un fondo rojo desgradado. Contenido de noticias aparecen cuatro tarjetas con fotos de pilotos y titulares especificos:

  Carlos Sainz
  Charles Leclerc
  George Rusell
  Lando Norris
  
<img src="https://github.com/user-attachments/assets/3de29ac8-18a5-455a-9a96-cf18dcf719ec" />

### Pilotos (ejemplo: Fernando Alonso)

Una ficha dedicada al piloto español en un entorno de color rojo. Visuales muestra una caricatura tipo avatar de Fernando Alonso vestido con un mono azul de Alpine dorsal 14. Coche en la parte inferior aparece una imagen del monoplaza historico Renault R25/R26 con los colores azul y amarillo.

<img src="https://github.com/user-attachments/assets/2f6431b7-6184-4df1-a87e-d34f8a546189" />

### Ayuda

Una sección de asistencia para el usuario con fondo desgradado rojo y la silueta de un monoplaza. Instrucción explica que para acceder a la página web, es necesario introducir el correo electrónico y la contraseña asociada a ese correo.

<img src="https://github.com/user-attachments/assets/4f2d8bc0-5316-459b-85dd-b9d7120ea969" />

### Menú de navegación

Muestra la barra de navegación lateral o menú desplegable de la aplicación. Opciones disponibles incluye enlaces a ¿Quines somos?, Ayuda, Noticias, Historia, Plotos, Escuderias, Coches y Marcas. Diseño es de color oscuro con texto en blanco, flaqueado por imagenes decorativas de pilotos y neumáticos.

<img src="https://github.com/user-attachments/assets/a440ff9b-42bf-4f81-a0c9-26d02369b5d9" />

### Historia de la F1

Esta sección detalla lor origenes de la competición sobre una ilustración artistica de monoplazas de distintas épocas. Fundación: Se indica que la F1 se fundó en 1950 con la primera temporada del Campeonato Mundial de Pilotos, iniciada en el circuito de Silverstone con una carrera de 24 horas.
Evolución: Describe la transición de coches grandes con motores delanteros hacia monoplazas ligeros, aerodinámicos y con motores traseros, destacando el uso de fibra de carbono y el efecto suelo.
Leyendas mencionadas: El texto anticipa una lista de pilotos destacados que incluye a Senna, James Hunt, Graham Lauda, Mika Hakkinen, Denny Hulme y Juan Manuel Fangio.

<img src="https://github.com/user-attachments/assets/765703f3-010e-4b78-a239-f50696d48c67" />

### Ficha leyenda: Ayrton Senna

Una página de tributo dedicada a uno de los pilotos más icónicos.
Título: "AYRTON SENNA: MITO Y LEYENDA" bajo la etiqueta "LA GRANDEZA DE LA F1".
Visual: Incluye una composición artística de Senna caminando con su casco amarillo frente a la bandera de Brasil y su monoplaza.

<img src="https://github.com/user-attachments/assets/2bc4dd3d-ff63-481b-ae27-cb69d2de740b" />

### Pilotos actuales

Una presentación visual de la indumentaria de pilotos famosos.
Equipación: Se muestran los monos de Senna (Camel/Nacional), Checo Pérez (Red Bull/Oracle) y el de Fernando Alonso en su etapa de Renault (Team Spirit).
Lista de pilotos: El texto anuncia que se mostrarán genios destacados como Checo Pérez, Fernando Alonso, Carlos Sainz, Charles Leclerc, Max Verstappen, Oscar Piastri y Lando Norris.

<img src="https://github.com/user-attachments/assets/82107f3d-8f42-48c1-83d2-00def98086d5" />

### Ficha piloto: Checo Pérez

Esta pantalla está diseñada como una ventana de interfaz de usuario retro.
Mensaje: Un cuadro de texto superior indica: "Checo Pérez: El mejor de México en F1".
Imagen: En el centro aparece una fotografía circular de Checo Pérez celebrando con la bandera de México y su coche de Red Bull Racing (dorsal 11).

<img src="https://github.com/user-attachments/assets/62ef6f53-5348-4266-8230-e63809ea6191" />

### Escuderías

Presenta una visión general de los equipos de la competición con un estilo artístico de pintura al óleo.
Definición: Explica que las escuderías son organizaciones que diseñan, fabrican y operan los coches, compitiendo por el título de constructores.
Equipos mencionados: El texto destaca a Ferrari, McLaren, Williams, Red Bull y Mercedes.
Logotipos: Visualmente se muestran los escudos de Ferrari, Mercedes-Benz, Red Bull Racing, McLaren y Alpine.

<img src="https://github.com/user-attachments/assets/ae09dc7d-055e-4c08-a5e8-211061cc74e6" />

### Escudería Mercedes

Un desglose detallado de los miembros y especificaciones técnicas del equipo Mercedes.
Personal Clave: * Pilotos principales: George Russell y Kimi Antonelli.
Jefe de equipo: Toto Wolf.
Director técnico: James Allison.
Información Técnica: * Motor: Mercedes-Benz.
Chasis: Menciona el diseño del modelo Mercedes W16.
Otros Pilotos: Nombra a Valtteri Bottas y Frederik Vesti como pilotos de reserva, y a Dorian Pin, Yuanpu Cun y Alex Powell en la academia.

<img src="https://github.com/user-attachments/assets/d815de21-a143-4e85-82a7-724824580990" />

### Coches de F1

Presenta un collage artístico con los logotipos de los equipos más emblemáticos de la parrilla.
Función de los equipos: Explica que las escuderías son las encargadas de diseñar, fabricar y operar los coches para competir por el título de constructores.
Logotipos visibles: Se muestran los escudos de Ferrari, Mercedes, Red Bull Racing, McLaren y Alpine.
Objetivo: Señala que cuentan con ingenieros y técnicos para maximizar el rendimiento en cada Gran Premio.

<img src="https://github.com/user-attachments/assets/86e3c6b0-67b1-441b-9bc7-72ad4fc1b106" />

### Artículo Formula 1

Identidad Visual: Destacan los logotipos oficiales de Ferrari y de la Fórmula 1, reforzando la marca.
Contenido Principal: Una fotografía de un monoplaza de Ferrari en una carrera nocturna, capturando la estética clásica de la escudería.
Mensaje Central: Un texto en español que define a Ferrari como un ícono mundial basado en la unión de la pasión, la velocidad y la innovación.
Formato: Se presenta como una diapositiva o "story" digital, con un diseño gráfico moderno de estilo collage sobre un fondo oscuro.

<img src="https://github.com/user-attachments/assets/831a64c6-09cb-4247-9856-afb4d53b15fb" />

---

### Enlace Canva
https://www.canva.com/design/DAG1Fwp_OVo/nzsDZnid_HPaMEl-ohBuFw/edit

---

## Mapa de navegabilidad
<details>
  <summary>Mapa de navegabilidad</summary>

Interfaces de Usuario y Configuración
Login y Registro: Formulario doble para ingresar a la plataforma (con correo y contraseña) o crear una cuenta nueva (incluye nombre y opción de Google).

Mi lista: Pantalla de gestión que muestra una cuadrícula con 19 elementos ("Lista 1" a "Lista 19") y un botón para Guardar lista.

Perfil: Sección para personalizar el usuario con avatares de F1, opción para eliminar/crear perfiles y un botón de Guardar perfil.

Administración: Panel de control con botones para añadir, modificar o eliminar datos en categorías como Pilotos, Coches, Marcas, Escuderías, Noticias, Ayuda, Cuentas y Listas.

Menú: Barra de navegación lateral que organiza todas las secciones (Historia, Pilotos, Coches, etc.).

Ayuda: Pantalla informativa que explica que el acceso a la web requiere el uso de correo electrónico y contraseña.

Contenido Informativo y Noticias
¿Quiénes somos?: Presentación de los autores, Eulalia Fernández y David Blanco, quienes buscan crear una web con estética de Netflix y contenido estilo Marca.

News: Sección de "Última Hora" con noticias en directo sobre los pilotos Carlos Sainz, Charles Leclerc, George Russell y Lando Norris.

Historia: Relato sobre la fundación de la F1 en 1950 en Silverstone y la evolución técnica de los monoplazas.

Ayrton Senna: Una página dedicada al "mito y leyenda" de este piloto brasileño.

Secciones de F1 (Pilotos, Escuderías y Coches)
Pilotos: * Ficha de Fernando Alonso con su avatar de Alpine y el Renault histórico.

Presentación de los monos de carrera de leyendas y pilotos actuales (Senna, Checo Pérez, etc.).

Mención especial a Checo Pérez como el mejor piloto mexicano en la F1.

Escuderías:

General: Definición de escudería y muestra de logos (Ferrari, Mercedes, Red Bull, McLaren, Alpine).

Mercedes: Ficha técnica detallada que incluye a los pilotos (Russell y Antonelli), el chasis Mercedes W16 y el equipo directivo liderado por Toto Wolf.

Coches: Explicación técnica sobre los monoplazas híbridos de fibra de carbono, el sistema KERS y la importancia de la aerodinámica.

Mapa del Proyecto
Estructura General: La última imagen muestra un esquema de flujo que conecta todas las pantallas mencionadas anteriormente, visualizando cómo se organiza la navegación del sitio web.

<img src="https://github.com/user-attachments/assets/78015beb-2148-4ebf-832c-b0dbedd1dc9a" />

</details>

</details>



## 🔧 8. Servicios	
<details>
	<summary>&#8203;</summary> <!-- desplegable vacío -->
	
### 8.1. DNS

Es el servicio encargado de traducir los nombres de dominio (como f1-news.com) en direcciones IP que las máquinas pueden entender. En tu proyecto, es lo que permitiría que un usuario escriba la dirección de tu web en el navegador para acceder a la página de Noticias o Historia sin tener que recordar una serie de números.

### 8.2. DHCP

Es el protocolo que asigna automáticamente una dirección IP y otros parámetros de red a cada dispositivo que se conecta. Sería el responsable de que, cuando un administrador entra al panel de Administración, su ordenador reciba la configuración de red necesaria para comunicarse con el servidor de la base de datos.

### 8.3. Apache

Es el software que "sirve" las páginas web. Cuando un usuario intenta acceder al Login o al Registro, Apache procesa la solicitud y envía los archivos visuales (HTML/CSS) al navegador del usuario para que pueda ver la interfaz.

### 8.4. Firewall

Es un sistema de seguridad que controla el tráfico de red entrante y saliente según reglas establecidas. En tu web, su función es proteger la sección de Cuentas y el Panel de Administración, bloqueando accesos no autorizados y permitiendo solo el tráfico legítimo para evitar ataques externos.

### 8.5. Copias de seguridad

Es el proceso de duplicar los datos del sitio para evitar su pérdida. Esto es vital para tu proyecto, ya que asegura que si el servidor falla, no se pierda la información de las Escuderías, los datos de los Pilotos o la configuración de los perfiles de usuario que han sido guardados.

</details>

## 💻 9. Diseño y programación del sitio web.
<details>
    <summary>&#8203;</summary> <!-- desplegable vacío -->

### 9.1. Maquetación web con HTML, CSS, JS.

Es la construcción de la parte visual (Front-end) que el usuario ve en el navegador.
HTML: Define la estructura de las páginas, como los títulos de "Historia" o los campos del formulario de "Login".
CSS: Se encarga del diseño, los colores rojos corporativos de la F1, el fondo oscuro y la disposición de las tarjetas en la sección de "News".
JS (JavaScript): Aporta interactividad, como hacer que el menú lateral se despliegue o que los botones de "Eliminar/Crear perfil" ejecuten una acción sin recargar la página.

### 9.2. Crear la DB en MySQL.

Es el "almacén" de información (Back-end) donde se guarda todo el contenido dinámico del sitio.
Tablas: Necesitarás tablas específicas para guardar los datos de los Pilotos (nombre, dorsal), las Escuderías (Mercedes, Ferrari) y las Cuentas de usuario.
Relaciones: Permite que, al consultar un piloto como Fernando Alonso, la base de datos sepa que pertenece a la escudería Alpine y muestre su coche correspondiente.

### 9.3. Trabajar PHP.

Es el lenguaje de programación que hace de "puente" entre la web y la base de datos.
Gestión de Formularios: Cuando un usuario rellena el registro, PHP toma esos datos y los guarda en MySQL.
Consultas Dinámicas: PHP extrae la información de las últimas noticias para que aparezcan automáticamente en la sección de "News".
Seguridad: Se encarga de verificar que el correo y la contraseña en el login sean correctos antes de permitir el acceso al panel de Administración.

</details>

## 🏗️ 10. Implementación de la infraestructura
<details>
<summary>&#8203;</summary> <!-- desplegable vacío -->
	
### 10.1. Configuración un entorno de backup
<details>
  <summary>&#8203;</summary> 

  Lo que hicimos para proteger el proyecto fue establecer un sistema de respaldo dividido en dos niveles:

Backup de la Base de Datos (MySQL):

Programamos exportaciones automáticas de las tablas de Cuentas, Pilotos y Escuderías para evitar perder los datos introducidos en el panel de administración.

Utilizamos comandos como mysqldump para generar archivos .sql que contienen toda la estructura y datos de la web.

Backup de Archivos del Servidor (Apache):

Realizamos copias de la carpeta raíz de la web donde se encuentran los archivos PHP, las hojas de estilo CSS y todas las imágenes de los coches y logotipos de F1.

Esto asegura que, ante un fallo del servidor, podamos restaurar la maquetación y la lógica de programación rápidamente.

Frecuencia y Almacenamiento:

Configuramos copias periódicas (diarias o semanales) para que cualquier cambio nuevo, como una noticia de última hora en la sección de News, quede respaldado.

Los archivos de respaldo se guardan en un directorio separado o en un medio externo para mayor seguridad.
</details>

### 10.2. Instalar y configurar un DNS primario 
<details>
<summary>&#8203;</summary> <!-- desplegable vacío -->

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

Configuración de los adaptadores.
Las dos primeras imagenes corresponden a la interfaz de configuración de VirtualBox:

   - Adaptador 1 --> Está configurado como Adaptador puente (Bridged Adapter) conectado a una
tarjeta Wi-Fi intel. Esto permite que la máquina virtual se comporte como un dispositivo 	  real más en tu red física, obteniendo una IP directamente de tu router.

   - Adaptador 2 --> Esta configurado como Red Interna con el nombre "intnet". Este modo se usa para que la MV (Maquina Virtual) se comunique únicamente con otras MV que estén en esa misma red interna, aislda del internet y de tu red local fisica.
 
<img width="623" height="291" alt="image" src="https://github.com/user-attachments/assets/efb8e8f1-0f84-4eb5-905c-991921efff60" />

<img width="624" height="297" alt="image" src="https://github.com/user-attachments/assets/78b42adf-2ae1-4404-81d8-ccea4adccf6e" />

Estado del sistema en Linux.
La tercera imagen es una terminal donde se ejecutó el comando ip a. Aquí vemos tres interfaces:lo (Loopback): 
La interfaz interna del sistema ($127.0.0.1$).

enp0s3 (Corresponde al Adaptador 1):
	Tiene la dirección IP $192.168.135.35/24$.
	Es la que te da salida a internet o conexión con tu red doméstica (vía Adaptador Puente).
	
enp0s8 (Corresponde al Adaptador 2):
	Tiene la dirección IP $10.10.10.254/24$.
	Esta es la interfaz para la red interna. Al terminar en .254, es muy probable que esta 		máquina esté configurada para actuar como puerta de enlace (gateway) o servidor para otras 	máquinas en esa red "intnet".
	
<img width="625" height="283" alt="image" src="https://github.com/user-attachments/assets/afaff1f3-302c-4e20-b2ac-fea63c7a2859" />


## Pasos a Seguir

Configuración de Netplan: Editar el archivo /etc/netplan/00-installer-config.yaml. 

YAML: Configurar enp0s3 con DHCP y enp0s8 con IP estática 10.10.10.254/24. 

Validación: 

Aplicar con sudo netplan apply

El comando ejecutado aplicamos los cambios con sudo netplan apply. Este comando lee los archivos .yaml en /etc/netplan/ y configura las interfaces de red según lo que esté escrito allí.

<img width="420" height="29" alt="image" src="https://github.com/user-attachments/assets/ca761cbb-a8f5-41d6-afe8-e0cf4f848823" />

Los errores y advertencias

Aquí aparecen tres problemas distintos:

unable to resolve host fernandez1: Esto no es un error de red crítico, sino de configuración del sistema. Indica que el nombre de tu máquina (fernandez1) no está asociado a ninguna IP en el archivo /etc/hosts.

Permissions for ... are too open: Netplan es muy estricto con la seguridad. Te advierte que el archivo de configuración tiene permisos que permiten que otros usuarios lo lean.

Solución: Ejecuta sudo chmod 600 /etc/netplan/*.yaml.

ovsdb-server.service is not running: Es una advertencia sobre Open vSwitch. Si no lo estás usando específicamente para redes virtuales complejas, puedes ignorarla; no impide que la red básica funcione.

<img width="619" height="191" alt="image" src="https://github.com/user-attachments/assets/41b95cdc-d1d3-4b90-972c-fff11fb619d9" />

Verificar con ip a.

A pesar de las advertencias, el comando parece haber funcionado (o mantiene la configuración anterior), ya que ip a muestra que:

enp0s3 sigue teniendo la IP 192.168.135.35.

enp0s8 sigue teniendo la IP 10.10.10.254.

<img width="618" height="277" alt="image" src="https://github.com/user-attachments/assets/c9304531-7f0b-468a-bc27-76915d7a4565" />

Instalación: Ejecutar curl -sSL https://install.pi-hole.net | bash. 

Estás ejecutando el comando de instalación oficial.

El mensaje en rojo: Dice que el script se llamó sin privilegios de root. Sin embargo, el propio instalador detecta que tienes sudo disponible e intenta elevarse solo.

El error recurrente: Aparece de nuevo sudo: unable to resolve host fernandez1. Como te mencioné antes, esto es porque el sistema intenta buscar su propio nombre en el archivo de "agenda" local (/etc/hosts) y no lo encuentra.

Resultado: A pesar del aviso del host, el logo de la frambuesa en ASCII indica que el instalador ha arrancado correctamente y está actualizando la caché de paquetes para empezar la instalación.

<img width="464" height="433" alt="image" src="https://github.com/user-attachments/assets/ce5b2d39-8d8b-42d9-810f-6ab70e6ecd18" />

Contraseña: Establecer clave con sudo pihole setpassword. 

Una vez instalado Pi-hole, has ejecutado sudo pihole setpassword.

Este comando es fundamental para poder entrar en la interfaz web de administración.

El mensaje final [✓] New password set confirma que ya tienes acceso a la administración gráfica.

<img width="548" height="103" alt="image" src="https://github.com/user-attachments/assets/108fff45-cc0a-4f9f-82b9-2c10b394af18" />

Prueba: Ejecutar nslookup y ping google.com.

Has ejecutado un ping google.com con éxito.

¿Qué significa? Tu máquina virtual no solo tiene una IP válida, sino que el enrutamiento hacia internet está funcionando perfectamente.

Detalle técnico: Los tiempos de respuesta (alrededor de 12 ms) son muy buenos, lo que indica que el puente con tu tarjeta Wi-Fi física es estable.

<img width="621" height="202" alt="image" src="https://github.com/user-attachments/assets/94ce301a-c314-4335-b453-4b816f878fe2" />

Resolución de nombres con nslookup

Aquí es donde se pone interesante para tu proyecto de Pi-hole. Estás consultando a qué IP corresponden los dominios ifp.es y google.com.

El Servidor DNS actual: Fíjate que dice Server: 192.168.109.1.

Ojo aquí: Esta IP parece ser la de tu router o el DNS por defecto de tu red.

Si tu objetivo es usar Pi-hole, en el futuro deberías ver aquí la IP de tu propia máquina (la 10.10.10.254 o la 192.168.135.35, dependiendo de desde dónde hagas la consulta).

Respuestas no autoritativas: Es normal, simplemente significa que tu servidor DNS local no es el "dueño" de los registros de Google, sino que ha preguntado a otros servidores superiores y te ha traído la respuesta.

<img width="299" height="177" alt="image" src="https://github.com/user-attachments/assets/9d995c95-9f24-4fea-b6e6-799c74361e80" />

<img width="292" height="166" alt="image" src="https://github.com/user-attachments/assets/75cf54e9-acc8-4459-8c4c-c09163e8d9b9" />

Estado actual de tu laboratorio
Red: Configurada y con salida a internet.

Pi-hole: Instalado y con contraseña establecida.

DNS: Actualmente sigues usando el DNS externo/router.

## Incidencias

Error de sintaxis: Uso accidental de comandos inexistentes como tryip en lugar de try. 

Escribi todo junto: sudo netplan tryip a.

Como puedes ver en la respuesta, el sistema te da un error de "elección inválida" (invalid choice: 'tryip'). Esto sucede porque el comando tryip no existe en Netplan.

Lo que realmente querías hacer eran dos comandos distintos:

sudo netplan try: Se usa para probar una configuración de red. Si no la confirmas en 120 segundos, el sistema vuelve atrás (muy útil para no quedarte sin conexión si te equivocas).

ip a: Es el comando para ver tus direcciones IP.

<img width="409" height="22" alt="image" src="https://github.com/user-attachments/assets/f2b1cedd-f516-473b-808c-0cdc282da257" />

<img width="615" height="66" alt="image" src="https://github.com/user-attachments/assets/13ef5fb2-e434-4300-b8d3-7fd563515d76" />

Permisos: Advertencias de Netplan indicando que los permisos del archivo YAML son "too open" (demasiado abiertos).

</details>

### 10.3. Instalar y configurar un servidor DHCP 

<details>
	
<summary>&#8203;</summary> <!-- desplegable vacío -->

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

### 10.4. Configurar servidor APACHE, PHP y MYSQL
<details>
  <summary>&#8203;</summary> <!-- desplegable vacío -->

### Tecnologías a Utilizar
Servidor: Ubuntu Server / Debian.

Servicio Web: Apache2.

Lenguaje de Scripting: PHP 8.x.

Base de Datos: MySQL / MariaDB.

Herramientas de Diagnóstico: systemctl, mysqladmin, ip a, Navegador Web.

### Introducción al Servicio

¿Qué es?: Un servidor HTTP de código abierto que entrega contenido web (páginas HTML, imágenes, scripts) a los clientes a través del protocolo HTTP/HTTPS.

¿Por qué es necesario?: Es la base para alojar sitios web, aplicaciones empresariales y servicios en red, permitiendo la interacción entre el usuario y el servidor mediante un navegador.

Información oficial:

https://httpd.apache.org/

https://www.php.net/

https://punkymo.gitbook.io/miwiki/servicios/servidores-web

### Detalles de la MV

Configuración de Red: Adaptador en modo Puente.

IP del Servidor: 192.168.135.48.

Componentes: LAMP Stack (Linux, Apache, MySQL, PHP).

### Pasos a Seguir

Instalación del Stack:

Actualizar repositorios: sudo apt update.

Instalar paquetes: sudo apt install apache2 php libapache2-mod-php mariadb-server.

Configuración de la Web PHP:

Crear un archivo de prueba en /var/www/html/info.php.

Añadir contenido para mostrar la configuración del servidor y datos personalizados.

Gestión de Base de Datos:

Acceder a MySQL y crear/listar usuarios: SELECT user FROM mysql.user;.

Verificar el estado del servicio con systemctl status mariadb.

Validación de Versiones:

Comprobar la versión de la administración de SQL: mysqladmin -u root -p version.

Comprobación Final:

Desde un cliente, acceder a http://192.168.135.48/info.php.

### Capturas Necesarias

1. Validación de Red: Captura del comando ip a mostrando la dirección 192.168.135.48.

<img width="601" height="245" alt="image" src="https://github.com/user-attachments/assets/eab013c6-923b-43ac-9922-a3721289a2e4" />

2. Edición de Script: Captura del editor (nano/vim) con el código PHP añadido a la web.

<img width="598" height="87" alt="image" src="https://github.com/user-attachments/assets/29e9ae28-d818-418d-a189-d91173b4f2e7" />

3. Gestión de Usuarios: Captura de la consola de MySQL mostrando la lista de usuarios identificados en el sistema.

<img width="601" height="121" alt="image" src="https://github.com/user-attachments/assets/c7710a0d-e976-4cd6-a51b-3edd78a5602b" />

4. Estado del Servicio: Captura de systemctl status mysql mostrando el servicio activo y en ejecución.

<img width="604" height="165" alt="image" src="https://github.com/user-attachments/assets/7a27f53d-9d79-439e-a241-57b9231f506b" />

5. Versión Administrativa: Captura de la salida del comando mysqladmin version.

<img width="602" height="156" alt="image" src="https://github.com/user-attachments/assets/4dcfc1ba-965d-4590-94db-1c9b4025b747" />

6. Resultado en Navegador: Captura del navegador web mostrando la página de Apache y la info de PHP cargada correctamente desde la IP del servidor.

<img width="491" height="472" alt="image" src="https://github.com/user-attachments/assets/75a5b784-c025-4c5a-9a3d-fa12105a077f" />

### Incidencias

Conflictos de Puerto: Si el puerto 80 está ocupado por otro servicio (como Nginx), Apache no iniciará. Se debe verificar con sudo lsof -i :80.

Permisos de Directorio: Si la web muestra un error "403 Forbidden", es probable que el usuario www-data no tenga permisos de lectura sobre /var/www/html/.

Módulos PHP: Si el navegador descarga el archivo .php en lugar de ejecutarlo, falta habilitar el módulo: sudo a2enmod php*.

</details>

### 10.5. Configurar firewall (pfSense)
<details>
<summary>&#8203;</summary> <!-- desplegable vacío -->
</details>

### 10.6 Configurar TRUENAS

1. Gestión del Almacenamiento
Muestra el panel principal del disco llamado "Deadpool"; está configurado en espejo (mirror) para seguridad y tiene 14 GB disponibles.
<img width="618" height="505" alt="image" src="https://github.com/user-attachments/assets/c189b273-c4e7-4c0f-a6d3-a50cbb4f4a8a" />
<img width="382" height="529" alt="image" src="https://github.com/user-attachments/assets/6595526e-03cc-4ada-8b74-89f2f4b0d46c" />
<img width="475" height="356" alt="image" src="https://github.com/user-attachments/assets/d3c98e21-7046-4a0d-bbee-fdb144953f3b" />

2. Sincronización Automática (Rsync)
Programación de una tarea para enviar copias de la carpeta sportflix a otro servidor (IP .83) cada medianoche de forma comprimida.
<img width="636" height="536" alt="image" src="https://github.com/user-attachments/assets/df5a979c-931d-492a-8836-de6a608d477d" />
<img width="640" height="527" alt="image" src="https://github.com/user-attachments/assets/94ef1b9a-3261-487b-bb86-21e01035f14e" />

Resumen de la tarea anterior; indica que está pendiente y se ejecutará automáticamente en 19 horas.
<img width="759" height="74" alt="image" src="https://github.com/user-attachments/assets/066f577d-03a1-4159-a767-0a996bfa6429" />

3. Control de Usuarios
Listado de las personas que pueden entrar al servidor, incluyendo administradores y usuarios comunes.
<img width="753" height="172" alt="image" src="https://github.com/user-attachments/assets/92fe4996-3206-47d8-b5ec-74ac36b996ae" />

Creación del nuevo usuario "sportlix"; se le da permiso para leer y escribir archivos, pero no puede entrar a la configuración del sistema (shell nologin).
<img width="715" height="479" alt="image" src="https://github.com/user-attachments/assets/4d6a7a29-af79-41c4-b43e-ee20e3c5ab27" />
<img width="720" height="506" alt="image" src="https://github.com/user-attachments/assets/739f30e3-d7dd-4389-8e81-68a76607c074" />
<img width="723" height="435" alt="image" src="https://github.com/user-attachments/assets/6d5dc137-ae0a-4570-8b52-bc457f95eec2" />

Confirmación visual de que el usuario sportlix ya está activo en el sistema.
<img width="756" height="23" alt="image" src="https://github.com/user-attachments/assets/9dcfa841-5393-4fe7-a27e-d32474488877" />

</details>

## 🛡️ 11. Seguridad
<details>
  <summary>&#8203;</summary> <!-- desplegable vacío -->

### 11.1. Plan contigencia
<details>
  <summary>&#8203;</summary> <!-- desplegable vacío -->

1. Identificar riesgos
Primero, analizamos qué cosas podrían salir mal.
● Fallos técnicos
● Pérdida de datos
● Errores humanos
● Desastres naturales 

2. Evaluar los riesgos
Probabilidad:
Fallos técnicos (medio)
Pérdida de datos (alta)
Errores humanos (medio)
Desastres naturales (Baja) 

Impacto:
Fallos técnicos: No sería grave lo único que tardaría tiempo en averiguar el error. 
Pérdida de datos: Sería muy grave en caso que en ese momento no hayamos hecho un backup de ello.
Errores humanos: No sería grave si sabemos cual es el error y en caso que sea lo contrario la única gravedad será saber cual es el problema.
Desastres naturales: El impacto no sería grave en caso de tener una copia.

3. Definir medidas preventivas
Copias de seguridad 
Formación del personal 
Sistemas de seguridad 

4. Diseñar acciones de respuesta
Si se cae el sistema → usar servidor alternativo
Si se pierde información → restaurar backup

5. Asignar responsables
Responsable IT
Responsable de seguridad
Coordinador del plan

6. Establecer recursos necesarios
Herramientas
Software

7. Crear un protocolo de comunicación
Nuestro protocolo de comunicación es comunicarnos ya sea de manera oral en clase o si se modifica algo fuera de clase pues por Whatsapp.

8. Probar el plan
Cuando tengamos todo acabado haremos varias copias de seguridad y simulacros para comprobar que el método es válido.

9. Revisar y actualizar
Cambios tecnológicos
Comprobar nuevos posibles riesgos
Mejoras detectadas

10. Que archivos tenemos que hacer backups
-HTML
-CSS 
-JS
-Base de datos
-Máquinas virtuales
-MYSQL
</details>

### 11.2. Auditoria de seguridad
</details>

## 🎮 12. Control
<details> 
	<summary>&#8203;</summary> <!-- desplegable vacío -->

### 12.1. La programación de las funcionalidades
### 12.2. Evaluar requisito web responsive
</details>

## 🔒 13. Cierre
<details>
	<summary>&#8203;</summary> <!-- desplegable vacío -->

### 13.1. Cloudflare
### 13.2. Revisiones
</details>

## 📝 14.Conclusiones
<details>
	<summary>&#8203;</summary> <!-- desplegable vacío -->
</details>

## 📚 15. Bibliografía
<details>
	<summary>&#8203;</summary> <!-- desplegable vacío -->

Github (https://docs.github.com/es/get-started/start-your-journey/hello-world) , (https://gist.github.com/dasdo/9ff71c5c0efa037441b6) y (https://prestashop.es) 

MySQL (https://www.mysqltutorial.org/) y (https://blog.baehost.com/comandos-basicos-para-mysql/) 

Cloudflare (https://raiolanetworks.com/blog/cloudflare/) y (https://developers.cloudflare.com/cloudflare-one/connections/connect-networks/do-more-with-tunnels/local-management/tunnel-useful-commands/) 

Promox (https://www.nakivo.com/es/blog/top-10-proxmox-cli-commands/) y (https://www.nakivo.com/blog/proxmox-install/)
</details>
