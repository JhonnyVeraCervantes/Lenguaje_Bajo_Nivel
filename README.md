# Lenguaje_Bajo_Nivel
<h1> TAMBIÉN LES DEJO MI PÁGINA WEB PARA QUE VEAN MÁS DETALLADO TODA LA INFORMACIÓN </h1>
<h1>EMU8086</h1>
<p>l emu8086 es un emulador del microprocesador 8086 (Intel o AMD compatible) con assembler integrado. A diferencia del entorno de programación en assembler utilizado anteriormente en la cátedra (MASM), este entorno corre sobre Windows y cuenta con una interfaz gráfica muy amigable e intuitiva que facilita el aprendizaje el lenguaje de programación en assembler.</p>
<h2>DESCRIPCIÓN.</h2>
<p> El emulador 8086 fue el primer que se utilizó para impartir un curso de microprocesadores por la universidad de Don Bosco; Este emulador posee una interfaz de usuario muy amistosa que permite familiarizarse con los fundamentos de la programación en lenguaje ensamblador de forma muy intuitiva, aparte de eso brinda una serie de recursos para ejecutar y depurar los programas</p>
<h2>VENTAJAS</h2>
<p>•	Fácil de manipular</p>
<p>•	Interfaz amigable con el usuario.</p>
<p>•	Barras de herramientas que permiten realizar programas más fácilmente.</p>
<h2> DESVENTAJAS</h2>
<p>•	No soportar algunas de las interrupciones más interesantes que posee el sistema operativo.</p>
<p>•	Tampoco puede acceder a los puertos físicos (reales), sino que los emula usando otros programas.</p>
<h2>PANTALLA PRINCIPAL</h2>
<p>Es donde se escribirán los archivos fuentes en lenguaje ensamblador,• Se puede ver una barra de menú de Windows con sus opciones file, edit, etc. pero también vera unas opciones poco usuales como assembler, emulator, etc. propias del emulador. También se ve una serie de botones que le permitirán crear un nuevo archivo (new), abrir un archivo que ya existe (open), abrir un ejemplo (examples), compilar un archivo fuente (compile), emular un archivo ejecutable (emulate) y otras opciones que ir descubriendo a medida que se familiarice con el programa.</p>
<h2>PANTALLA DE COMPILACIÓN</h2>
<p>Al momento de dar compile Mientras se abre una ventana llamada “assembler status” que le informa sobre los resultados del proceso. Si el resultado es exitoso observará un mensaje como el de la figura en caso contrario se muestran los errores generados.</p>
<h2>PANTALLA DEL EMULADOR</h2>
<p>•	File, permite administrar (cargar o salvar) los archivos que va creando o ejecutando
<p>•	Math, da acceso a una calculadora y un convertidor de basas de numeración. 
<p>•	Debug, provee herramientas para depurar programas.
<p>•	View, permite abrir otras ventanas que pueden ser de mucha ayuda al ejecutar o depurar programas.
<p>•	External, permite ejecutar el programa con otras herramientas diferentes del EMU8086.
<p>•	Virtual devices, activa los dispositivos virtuales con que cuenta el programa, dado que se trata de un emulador no se tiene acceso a los puertos físicos de la computadora, por lo que estos son simulados. 
<p>•	 Virtual drive, da opciones para administrar las unidades virtuales de almacenamiento (hdd y fdd virtuales).</p>
<h3>VENTANAS DE CÓDIGO FUENTE</h3>
 <p>Una es la ventana donde se crea el código y la otra ventana es la que aparece al momento de compilar y ejecutar el código</p>


<h2>REGISTROS DE LA CPU</h2>
<p>La CPU x86 tiene 14 registros internos y básicos. Algunos son realmente de 32 bits pero por ahora se utilizará el modo real que es compatible con el procesador 8086 (igualmente accesibles a la parte alta de éstos registros, inclusive en el modo real). Los registros son los siguientes (estos registros son de 16 bits nombrados de la siguiente manera, a excepción del registro de banderas).</p>
<h3>REGISTROS DE USO GENERAL</h3>
<p>•	AX: Acumulador (AL:AH)
<p>•	BX: Registro base (BL:BH)
<p>•	CX: Registro contador (CL:CH)
<p>•	DX: Registro de datos (DL:DH)
<h3>REGISTROS DE SEGMENTO (SOLO SE PUEDEN USAR PARA LOS USOS MENCIONADOS A EXCEPCIÓN DE ES)</h3>
<p>•	DS: Registro del segmento de datos
<p>•	ES: Registro del segmento extra
<p>•	SS: Registro del segmento de pila
<p>•	CS: Registro del segmento de código
<h3>REGISTROS PUNTEROS (TAMBIÉN PUEDEN TENER USO GENERAL)</h3>
<p>•	BP: Registro de apuntadores base
<p>•	SI: Registro índice fuente
<p>•	DI: Registro índice destino
<h3>REGISTROS ESPECIALES (SOLO SE PUEDEN USAR PARA LOS USOS MENCIONADOS)</h3>
<p>•	SP: Registro apuntador de la pila
<p>•	IP: Registro apuntador de la siguiente instrucción
<p>•	F: Registro de banderas (8 bits)
<p>La parte baja del registro AX se llama AL y la parte alta AH. La parte baja del registro BX se llama BL y la parte alta BH, y también ocurre lo mismo con el registro CX y DX.</p>
<h2>BITS DEL REGISTRO DE BANDERAS</h2>
<h3>OVERFLOW</h3>
<p>•	NV (Apagado): No hay desbordamiento
<p>•	OV (Encendido): Si lo hay
<h3>DIRECTION</h3>
<p>•	UP: Hacia adelante
<p>•	DN: Hacia atras
<h3>INTERRUPTS</h3>
<p>•	DI: Desactivadas
<p>•	EI: Activadas
<h3>SIGN</h3>
<p>•	PL: Positivo
<p>•	NG: Negativo
<h3>ZERO</h3>
<p>•	NZ: No es cero
<p>•	ZR: Si lo es
<h3>AUXILARY CARRY</h3>
<p>•	NA: No hay acarreo auxiliar
<p>•	AC: Hay acarreo auxiliar
<h3>PARITY</h3>
<p>•	PO: Impar
<p>•	PE: Paridad par
<h3>CARRY</h3>
<p>•	NC: No hay acarreo
<p>•	CY: Si lo hay

<h2>DIRECCIONAMIENTOS</h2>
<p>Dado que es necesario transferir datos, existen los siguientes tipos de direccionamiento:</p>
<p>•	Valor de un registro Ejemplo: MOV AX, DX
<p>•	Constante Ejemplo: MOV BX, 1AB
<p>•	Valor apuntado por una constante Ejemplo: MOV AX, [1000]
<p>•	Apuntado por un registro de segmento y uno de offset (Solo puede ser BX, BP, DI o SI) Ejemplo: MOV CX, ES:[DI]
<p>•	Apuntado por DS y la suma de BX con una constante o apuntado por SS y la suma de BP con una constante Ejemplo: MOV DX, DS:[BP+1000]
<p>•	Apuntado por DS y la suma de DI o SI con una constante Ejemplo: MOV BX, DS:[SI+6F9]
<p>•	Apuntado por DS y la suma de BX y SI o BX y DI con una constante o apuntado por SS y la suma de BP y SI o BP y DI con una constante
Ejemplos
<p>MOV AX, DS:[BX][SI]+1FB9
<p>MOV DX, SS:[BP][DI]+C9F8


<h2> ESTE ES EL ENLACE PARA DESCARGARLO:</h2>
https://emu8086.waxoo.com/
<p>Después de instalarlo, realizar la instalación de una manera normal</p>
<p> 1.	Clic derecho
<p> 2.	Instalar
<p> 3.	Next
<p> 4.	Siguiente 
<p> 5.	Siguiente hasta que se instale

<p>Una vez instalado, le damos clic derecho al programa y lo ejecutamos.
<p>Nos va a pedir que ingresemos una cuenta
  
                Licensee Name: Craked-By-Team-AgressioN!!
                Registration Key: KDLSR2ERKRG4U8PDP4UA
 
 <p>Clic en “OK” </p>
<p>Una vez ingresados, comenzamos a programar.</p>


<h1> PROGRAMAS CON SUS CODIGOS </h1>

<h2>OPERACIONES BASICAS</h2>

 
          ; PROGRAMA PIDE 2 NUMEROS
          ; REALIZA OPERACIONES BASICAS
          .model small
          .stack 64
          .data  
          Num1 db 0
          Num2 db 0
          Suma db 0
          Resta db 0
          Multiplicacion db 0
          Division db 0

          Solicitud1 db 13,10,'Ingrese Primer Numero',13,10,'$'
          Solicitud2 db 13,10,'Ingrese Segundo Numero',13,10,'$'

          Msuma db 13,10 , 'La Suma de los numeros es:  $'
          Mresta db 13,10 , 'La Restae los numeros es:  $'
          Mmultiplicacion db 13,10 , 'La Multiplicacion de los numeros es:  $'
          Mdivision db 13,10 , 'La Division de los numeros es:  $'

          .code
              inicio:
              mov ax, @data
              mov ds, ax

              mov ah, 9
              lea dx, Solicitud1
              int 21h
              mov ah, 1
              int 21h
              sub al, 30h
              mov Num1, al  


              mov ah, 9
              lea dx, Solicitud2
              int 21h
              mov ah, 1
              int 21h
              sub al, 30h
              mov Num2, al

              ;Iniciar con las Operaciones

              mov al, Num1
              add al, Num2
              mov Suma, al


              mov al, Num1
              sub al, Num2
              mov Resta,al


              mov al,Num1
              mul Num2
              mov Multiplicacion, al


              mov al, Num1
              div Num2
              mov Division, al     



             mov ah,9
             lea dx, Msuma
             int 21h
             mov dl, Suma
             add dl, 30h
             mov ah, 2
             int 21h


             mov ah,9
             lea dx, Mresta
             int 21h
             mov dl, Resta
             add dl, 30h
             mov ah, 2
             int 21h    


             mov ah,9
             lea dx, Mmultiplicacion
             int 21h
             mov dl, Multiplicacion
             add dl, 30h
             mov ah, 2
             int 21h

              mov ah,9
             lea dx, Mdivision
             int 21h
             mov dl, Division 
             add dl, 30h
             mov ah, 2
             int 21h  


              .exit
           ret 


<p>DAMOS CLIC EN “EMULATE”, CLIC EN “RUN”</p>
<p>Y NOS APARECERA EL RESULTADO</p>  

<h2>HOLA MUNDO</h2>

<p>CODIGO:</p>

          .model small 
          .data 
              saludo db "HOLA MUNDO CARLOS","$"
          .code 
          programa: 
              mov ax,seg saludo 
              mov ds,ax 
              mov ah,09h 
              lea dx,saludo 
              int 21h 
                mov ax,4c00h 
              int 21h 

          end programa
          
          
<p> GRACIAS POR LEER MI ARTICULO ARRIBA TE DEJO MI PAGINA WEB SOBRE EL ARTICULO ANDA Y VISITALA </p>          

