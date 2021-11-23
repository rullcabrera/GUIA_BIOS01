author: Raúl Cabrera Garcia
summary: Guia Opciones Seguridad BIOS1
id: BIOS01
categories: codelab,markdown
environments: Web
status: Published
feedback link: [Enlace para dejar un issue en Git Hub](https://github.com/rullcabrera/GUIA_BIOS01/issues)

# Guia BIOS 01 Portátil MSI CX61-2PC

## Página 1
Duration: 0:01:00

### Introducción
Consultaremos las opciones de seguridad que nos ofrece nuestra BIOS.
En mi caso aunque es algo antigua se trata de una BIOS UEFI y no Legacy.
En el apartado **“Security”**, tenemos las siguiente opciones.

![Foto1_BIOS01](img/foto_portatil.jpg)

## Página 2
Duration: 0:02:00

### SECCIÓN CLAVES EN LA BIOS

* **Supervisor Password** → Nos permite asignar una clave a la ahora de acceder a la BIOS.
* **User Password** → En este caso asignamos una clave, que nos pedirá justo cuando arranquemos el equipo, para seguir iniciando el sistema.
![Foto1_BIOS01](img/foto1.jpg)

* **Password check** → Es una opción en la cual podemos indicar cuando queremos que se revise la clave o al arranque o siempre. La diferencia que he podido comprobar es:
    * **Setup**: Te pedirá la clave al entrar a la BIOS.
    * **Always**: Te la pedirá al arrancar o al entrar en la BIOS. Sin necesidad de poner una específica a la ahora de arrancar.
![Foto2_BIOS01](img/foto2.jpg)

Positive
: Asignamos clave Supervisor

![Foto3_BIOS01](img/foto3.jpg)
Nos pedirá confirmación de la clave que hemos puesto.
![Foto4_BIOS01](img/foto4.jpg)

Positive
: Vemos que ahora arriba nos sale **“Supervisor Password: Installed”**

![Foto6_BIOS01](img/foto6.jpg)
Guardamos cambios y reiniciamos.
![Foto5_BIOS01](img/foto5.jpg)
Y ya al reiniciar nuestro equipo. Y para ejecutar la BIOS, nos pedirá la clave que acabamos  de asignar.
![Foto14_BIOS01](img/foto14.jpg)

## Página 3
Duration: 0:02:00

Ahora, haremos lo mismo pero con User Password.
![Foto7_BIOS01](img/foto7.jpg)
Nos volverá a pedir que confirmemos la clave que queremos.
![Foto8_BIOS01](img/foto8.jpg)

Positive
: Y ahora es **“User Password: installed”**.

![Foto9_BIOS01](img/foto9.jpg)
Guardaremos cambios, y al reiniciar está vez nos pedirán una clave justo al arrancar el equipo.

## Página 4
Duration: 00:03:00

### SECCIÓN SECURE BOOT

* **Secure Boot**: Es el arranque seguro que metió *Microsoft*, para de alguna manera impedir que se ejecute posible *“código malicioso”* y asegurar que lo que se ejecuta es de *“autores conocidos”*. Esto acarreó problemas a la hora de instalar Windows con otros sistemas.

> A día de hoy ya es más “amigable”, con otros sistemas.
> Por ejemplo Ubuntu de Linux.

* Tenemos la opción:
    * **Secure Boot Control**: Habilitado/Deshabilitado.
![Foto10_BIOS01](img/foto10.jpg)
    * **Secure Boot Mode**: Standar/Custom
![Foto12_BIOS01](img/foto12.jpg)

Positive
: El modo **“Custom”**, lo que te permite, es gestionar las claves del arranque seguro.

* Luego a su vez tiene 2 opciones más:
    * **Factory Default Key Provisioning**: Enabled/Disabled. Habilitaremos o no. Las claves, que permiten el proceso de autenticar previamente los módulos que se vayan a poder ejecutarse (*firmware drivers, UEFI bootloaders, UEFI applications*).
    * **Install All Factory Default Keys**: Para instalar las claves por defecto.
![Foto13_BIOS01](img/foto13.jpg)

## Página 5
Duration: 00:01:00

### SECCIÓN BOOT

* **Boot Order** (Orden de arranque):
    * Aquí podremos personalizar el orden en el que queremos que se arranque nuestro equipo. Tenemos a modo de compatibilidades dos tipos de modos de selección en el orden de arranque:
    * **UEFI o Legacy**: En mi caso tengo puesto el modo *"UEFI"*. Y el orden se muestra en la imagen.
![Foto11_BIOS01](img/foto11.jpg)

Negative
: Y en el caso de está BIOS al no tener muchas opciones respecto a evitar arranques desde fuera. Podríamos o deshabilitar *Wake On LAN* y eliminar las entradas innecesarias de dispositivos que no queremos que arranque. Así evitaríamos que se pudiera arrancar el equipo si estuviera conectado en Red. O en el caso de que el equipo se encuentre en alguno de los supuestos que no permitiera arrancar desde esos dispositivos, Eliminado del *“Boot Order”* la entrada.