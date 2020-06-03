# Manual-De-Usuario
Manual de Usario para la tesina Sistema para la detección de manipulación de datos en computadores personales.

# Compilar HEADS
## Pre- Requisito DEBIAN
```apt update
apt install -y \
	build-essential \
	zlib1g-dev uuid-dev libdigest-sha-perl \
	libelf-dev \
	bc \
	bzip2 \
	bison \
	flex \
	git \
	gnupg \
	iasl \
	m4 \
	nasm \
	patch \
	python \
	wget \
	gnat \
	cpio \
	ccache \
	pkg-config \
	cmake \
	libusb-1.0-0-dev \
	pkg-config \
	texinfo \
```
## Compilacion
```cd heads-0.2.1```
```make BOARD=x230-flash```

```make BOARD=x230```

# Instalar HEADS en BIOS CHIP
Seguir el manual oficial de HEADS: http://osresearch.net/Installing-Heads



# Verificaion y Sincronizacion
## Pre Requisitos
* Tener los progamas signing.sh verify.sh en el usb.
## Sincronizar Disco Duro
* En el menu principal ir a Options y despues ir a la penultima opcion llamada "Exit to recovery shell"
* Insertar el USB y correr
``` mount-usb
```
* Insertar la Yubikey
* Despues correr el programa signing.sh
* Le va a pedir el PIN de yubikey que es 12345678 por default.
* En este momento se guardara en el USB el archivo HDD.sig que contiene la firma del disco duro en el momento que se hizo

## Verificar Disco Duro
* En el menu principal ir a Options y despues ir a la penultima opcion llamada "Exit to recovery shell"
* Insertar el USB y correr
``` mount-usb
```
* Despues correr el programa verify.sh
* Despues le va a mostrar si es un Good Signature o Bad Signature dependiendo si hubo un cambio en el disco duro desde la ultima verificaion.









