# Mi configuración de emacs

Este es mi configuración de emacs, el init.el esta documentado a parte hay 
un poco mas de información en el fichero init.org.

Hay 2 rumores sobre el editor:

- Es la navaja suiza de los editores de codigo.
- Tiene tantos complementos que es casi un sistemo operativo, solo le 
faltaria el kernel. 

A dia de hoy llevando almenos 3 años usandolo es tan basto de opciones
y ligero en carga en RAM que doy fe que esos 2 rumores son verdad.

# Modos de emacs

Emacs dispone de 2 modos: modo mayor y modo menor
- Mayor: Solo puede haber un modo mayor activado por buffer, se encarga de
		 tratar el fichero de segun del lenguaje de programación se use.
		 Por ejemplo: .java activa el modo java-mode, 
		              .rs activa el modo rust-mode/rustic,
					  .cpp/.hpp activa el mode c++-mode,
					  .c/.h activa el mode c-mode, 
					  .erl activa el modo erlang-mode,
					  .js activa el modo javascript-mode,
					  .el activa el modo emacs-lisp-mode y
					  .css activa el modo css-mode

- Menor: Se puede activar tantos modos que se quiera o tenerlos desactivados,
		 su finalidad es complementarse con los modos mayores. Por ejemplo:
		 hl-line resalta la linea actual,
		 yasnippet viene a ser el gestor de plantillas,
		 projectile viene a ser un geestor de proyectos y
		 company viene a ser el autocompletado.
		 
Modos mayores por defecto: 
- java-mode
- c++-mode
- c-mode
- javascript-mode
- emacs-lisp-mode
- css-mode

Modos mayores instalados en mi configuración:
- rustic/rust-mode
- erlang-mode

# Atajos de teclado que mas uso

__Acalaraciones__: 
No es importante aprender usar toodo los atajos de teclado, sino 
modificarlos que se ajusten a tu flujo de trabajo habitual.

Control o Ctrl se lee con C-, Alt se lee con M-, Windows/Super se lee 
como s-

Cerrar emacs: C-x C-c
Abrir un fichero, carpeta o crear fichero: C-x C-f
Guardar: C-x C-s
Cuardar como: C-x C-w
Dividir ventana horizontalmente: C-x 2
Dividir ventana verticalmente: C-x 3
Cerrar todas la ventanas menos el actual: C-x 1
Cerrar la ventanas actual: C-x 0
Cambiar a la siguiente ventana: C-x o
Cambiar de buffer: C-x b nombre del buffer
Listar todos lo buffers: C-x C-b
Cerrar un buffer: C-x k nombre del buffer
Cancelar un comando o salir de ello: C-x g o ESC ESC ESC
Inicio de linea: inicio/home
Final de linea: fin/end
Inicio de ventana: C-inicio
Final de ventana: C-fin
Buscar: C-s
Reemplazar: M-%
Mover el cursor entre lineas en blanco: C-[arriba y abajo]
Mover el cursor entre palabras: C-[izquierda y derecha]
Mover el cursor a un linea concreta: M-g g
Seleccionar texto: Shift-Flechas de dirección
Seleccionar todo: C-x h, C-Shift-end o C-Shift-inicio
Edicion multilinea: C-x SPC y se combina con retroceso/backspace o 
	                                          M-x string-rectangle
Copiar: M-w, si esta activado CUA keys C-c
Cortar: C-w, si esta activado CUA keys C-x
Pegar: C-y, si esta activado CUA keys C-v
Deshacer: C-x u
Executar funciones/plugins: M-x
Executar una funcionalidad varias veces: C-u X, 
	X es el numero de veces a ejecutar
Empezar a grabar una macro: F3
Acabar de grabar una macro: F4
Executar una macro: C-x e
Pantalla completa: F11
Barra de menu: F10
Lanzar un comando a la terminal: M-!

# Comandos para emacs

Hay una lista enorme de comandos para emacs, estos son los que mas uso.

- dired (Explorador de archivos)
- eshell (Shell de emacs)
- package-list-packakges(Gestor de paquetes)
- Los modos mayores y menores
- string-rectangle(Insercion de texto en multiple lineas)
- magit (El controlador de versiones, hay que tener instalado 
	y configurado git)

# Mas detalles y trucos

- -nw: indicamos que emacs se ejecute en terminal
- -mm: indicamos que emacs se maximize la ventana
- -fs: indicamos que emacs se ocupe toda la pantalla
- --debug-ini: indicamos que emacs depure el script init.el o .emacs.el
- Solo usa un nucleo de la CPU
- También funiona en terminal
- Podemos poner o quitar el numero de linea del fichero que con eso podemos
desplazarnos con M-g g en caso de usar la numerologia absouta o C-x u 
Numero-de-veces-a-ejecutar Interacccion en caso de usar la numerologia relativa
- Quieres usar emacs con los atajos de teclados o hacer que emacs sea un 
editor modal como vim, instalate el plugin evil
- En el gestor de paquetes de emacs, puedes instalarte un paquete de temas para 
el editor, doom-themes tiene un kit muy variado.
- Cuando ejecutes el comando packages-list-packages si tienes configurado los 
repositorios y que se refresquen, podras actualizar los paquetes que tengas 
instalados.
- Puedes instalarte firefox y obs-studio en el emacs.
- Te trae un lector de pdfs
- Puedes ejecutar vim dentro de emacs? Si, abres una terminal(eshell, shell,
ansi-term o term) y despues ejecutas vim, el resultado según como puede 
ser algo que dejar de desear pero funciona.
- Existe un plugin que hace que emacs funcione como gestor de ventanas 
tipo tiling
- Tiene org-mode un modo para organizarte tus ideas/proyectos
- Los ficheros .org los puedes leerlos en emacs y en github.
- Cuando hagas C-x C-f y quieras editar un fichero remoto, borra toda la 
linea pon /ssh:usuario@dominio:~/ruta/del/fichero auntenticandote cogerá
la información remota y lo pasara emacs podras hacer ediciones sin usar la
terminal.

Con todo esto que sepais que esta editado con emacs y subido a mi cuenta
de github al repositorio de configuración de emacs con magit
