ENGLISH ################################################################
Visual FoxPro 9.0 Diff and Merge Tool v2.0 for PlasticSCM 5
02/01/2014 -  Created by Fernando D. Bozzo (fdbozzo@gmail.com)
########################################################################

Download at: https://drive.google.com/folderview?id=0B_qHXcWqGDY-Wi1fWEg5ajFZb0k&usp=sharing

WHAT IS THIS TOOL AND HOW TO USE IT?
--------------------------------------------
This tool is intended to be used with Visual FoxPro 9.0 and PlasticSCM 5.
It facilitates de Diff and Merge operations on VFP 9 binaries, by the use
of a Diff/Merge program interface (foxpro_plasticscm_dm.exe) and a VFP 9
bidirectional binary-text converter (FoxBin2prg.exe)


DIFF CONFIGURATION ON PLASTICSCM:
--------------------------------------------
- Click on PlasticSCM Preferences icon
- Select "Diff Tools"
- For each binary FoxPro extension* "add" this:
	- External Diff Tool: "<path>\foxpro_plasticscm_dm.exe" "'DIFF' '@sourcefile' '@destinationfile' '@sourcesymbolic' '@destinationsymbolic'"
	- Pattern: .pjx
- Click OK
- Move the added extension to the top of the list, to prioritize it
- Repeat this operation for each supported extension

*Note: Supported extensions are: PJX,VCX,SCX,FRX,LBX,DBF,DBC,MNX


MERGE CONFIGURATION ON PLASTICSCM:
--------------------------------------------
- Click on PlasticSCM Preferences icon
- Select "Merge Tools"
- For each binary FoxPro extension* "add" this:
	- External Merge Tool: "<path>\foxpro_plasticscm_dm.exe" "'MERGE'  '@sourcefile' '@destinationfile' '@sourcesymbolic' '@destinationsymbolic' '@basefile' '@basesymbolic' '@output'"
	- Pattern: .pjx
- Click OK
- Repeat this operation for each supported extension

*Note: Supported extensions are: PJX,VCX,SCX,FRX,LBX,DBF,DBC,MNX


USE:
--------------------------------------------
- When using Diff operation you must use "CTRL+D" to use the external tool on the supported extension
- When using Merge operation you must accept the PJT "destination" (or secondary extension in accordance
  of the binary selected: VCT,SCT,FRT,LBT,etc) and the Merge automatically recognizes the configured
  extensions and displays them for doing the Merge operation.


ABOUT FOXBIN2PRG 2-WAY CONVERTER POR VFP 9:
--------------------------------------------
Updates of this tool and configuration instructions can be downloaded from the Open Source Project 
FOXBIN2PRG on CodePlex at https://vfpx.codeplex.com/wikipage?title=FoxBin2prg


FINAL NOTE:
--------------------------------------------
This program is Open Source and "libre", and I don't make any garanties that it fulfills your espectations
or that it will be free of bugs, that I will try to fix if my obligations let me do it.


LICENSE:
--------------------------------------------
This work is licensed under the Creative Commons Attribution 4.0 International License.
To view a copy of this license, visit http://creativecommons.org/licenses/by/4.0/.



ESPAÑOL ################################################################
Herramienta de Diff y Merge v2.0 en Visual FoxPro 9.0 para PlasticSCM 5
02/01/2014 -  Creado por Fernando D. Bozzo (fdbozzo@gmail.com)
########################################################################

Descargar de: https://drive.google.com/folderview?id=0B_qHXcWqGDY-Wi1fWEg5ajFZb0k&usp=sharing


¿QUÉ ES ESTA HERRAMIENTA Y CÓMO SE USA?
--------------------------------------------
Esta herramienta está pensada para usarse con Visual FoxPro 9 y PlasticSCM 5.
Facilita las operaciones de Diff y Merge sobre binarios VFP 9, mediante el uso
de una programa interfaz de Diff/Merge (foxpro_plasticscm_dm.exe) y un conversor
de binarios-texto bidireccional (FoxBin2prg.exe)


CONFIGURACIÓN DE DIFF EN PLASTICSCM:
--------------------------------------------
- Clickear en el icono de Preferencias de PlasticSCM
- Seleccionar "Herramientas Diff"
- Para cada extensión* binaria FoxPro "agregar" esto:
	- Herramienta Diff externa: "<path>\foxpro_plasticscm_dm.exe" "'DIFF' '@sourcefile' '@destinationfile' '@sourcesymbolic' '@destinationsymbolic'"
	- Pattern: .pjx
- Clickear OK
- Mover la extension agregada al inicio de la lista, para priorizarla
- Repetir esta operación para cada extensión binaria soportada

*Nota: Las extensiones soportadas son: PJX,VCX,SCX,FRX,LBX,DBF,DBC,MNX


CONFIGURACIÓN DE MERGE EN PLASTICSCM:
--------------------------------------------
- Clickear en el icono de Preferencias de PlasticSCM
- Seleccionar "Herramientas Merge"
- Para cada extensión* binaria FoxPro "agregar" esto:
	- Herramienta Merge externa: "<path>\foxpro_plasticscm_dm.exe" "'DIFF' '@sourcefile' '@destinationfile' '@sourcesymbolic' '@destinationsymbolic'"
	- Pattern: .pjx
- Clickear OK
- Mover la extension agregada al inicio de la lista, para priorizarla
- Repetir esta operación para cada extensión binaria soportada

*Nota: Las extensiones soportadas son: PJX,VCX,SCX,FRX,LBX,DBF,DBC,MNX


USE:
--------------------------------------------
- Cuando se haga una operación de Diff, debe pulsar "CTRL+D" para usar la herramienta externa con las
  extensiones soportadas
- Cuando se haga una operación de Merge debe aceptar el PJT "destino" (o extensión secundaria de acuerdo
  al binario seleccionado: VCT,SCT,FRT,LBT,etc) y el Merge automaticamente reconoce las extensiones
  configuradas y las muestra para realizar la operación de Merge.


SOBRE EL CONVERSOR DE DOBLE-VIA FOXBIN2PRG PARA VFP 9:
--------------------------------------------
Las actualizaciones e instrucciones de configuración de esta herramienta pueden ser descargadas
del Proyecto Open Source FOXBIN2PRG en CodePlex, en https://vfpx.codeplex.com/wikipage?title=foxbin2prg_es


NOTA FINAL:
--------------------------------------------
Este programa es Open Source y "libre", y como tal no ofrezco garantías de que cumpla con sus espectativas
o de que está libre de fallos, que intentaré solucionar si me reporta y mis obligaciones me lo permiten.


LICENCIA:
--------------------------------------------
Esta obra está sujeta a la licencia Reconocimiento-CompartirIgual 4.0 Internacional de Creative Commons.
Para ver una copia de esta licencia, visite http://creativecommons.org/licenses/by-sa/4.0/deed.es_ES.
