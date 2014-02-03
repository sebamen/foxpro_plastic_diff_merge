ENGLISH ################################################################
Visual FoxPro 9.0 Diff and Merge Tool v2.3 for PlasticSCM 5
2013/12/20 -  Created by Fernando D. Bozzo (fdbozzo@gmail.com)
########################################################################

Download at: https://github.com/fdbozzo/foxpro_plastic_diff_merge

WHAT IS THIS TOOL AND HOW TO USE IT?
------------------------------------------------------------------------
This tool is intended to be used with Visual FoxPro 9.0 and PlasticSCM 5.
It facilitates de Diff and Merge operations on VFP 9 binaries, by the use
of a Diff/Merge program interface (foxpro_plasticscm_dm.exe) and a VFP 9
bidirectional binary-text converter (FoxBin2prg.exe)



DIFF CONFIGURATION ON PLASTICSCM:
------------------------------------------------------------------------
- Click on PlasticSCM Preferences icon
- Select "Diff Tools"
- For each binary FoxPro extension* "add" this:
	- External Diff Tool: "<path>\foxpro_plasticscm_dm.exe" "'DIFF' '@sourcefile' '@destinationfile' '@sourcesymbolic' '@destinationsymbolic'"
	- Pattern: .pjx     (use lowercase!)
- Click OK
- Move the added extension to the top of the list, to prioritize it
- Repeat this operation for each supported extension (*Note 1)

*Note 1: Supported extensions are: pjx,vcx,scx,frx,lbx,mnx,dbf,dbc



MERGE CONFIGURATION ON PLASTICSCM:
------------------------------------------------------------------------
- Click on PlasticSCM Preferences icon
- Select "Merge Tools"
- For each binary FoxPro extension* "add" this:
	- External Merge Tool: "<path>\foxpro_plasticscm_dm.exe" "'PRESERVE_WS'"
	- Pattern: .pjx     (use lowercase!)
- Click OK
- Repeat this operation for each Visual FoxPro binary extension (* Note 2)

* Note 2: Visual FoxPro binary extension are: pjx,pjt,vcx,vct,scx,sct,frx,frt,lbx,lbt,mnx,mnt,dbf,fpt,cdx,dbc,dcx,dct



Custom "Open with..." CONFIGURATION:
------------------------------------------------------------------------
- Click on PlasticSCM Preferences icon
- Select "Custom Open with..."
- Click "Add..." and complete the fields:
     Display Name:                FoxBin2Prg
	 Full path to the executable: <Path-To-FoxBin2Prg>\foxbin2prg.exe
- Click OK

*Note 3: We will use this on the GUI as a trick to convert to text or to binary
*Note 4: You can add Notepad++ too, it's useful to see text files directly from Plastic GUI



USE:
------------------------------------------------------------------------
- When using Diff operation you must use "CTRL+D" to use the external tool on the supported extension
  (see previuos "*Note 1"), but my recommendation is to just Diff on text versions, so be careful
  to regenerate text versions when you end editing binaries from FoxPro IDE
  
- When using Merge operation, the idea is to Process all files so the binaries get passed directly
  to the "Pending Changes" window, so you just need to Merge on Text files. If there is remaning
  binary, select them, right-click and select the option to keep the changes on "source" (don't
  mind about it, because later you need to regenerate all binaries anyway)
  
- When Merge ends, you go to "Pending Changes" window, regenerate all binaries by selecting the text
  version, right-click, and "Open / Open with..." FoxBin2Prg (one file at a time, or else Plastic
  will throw all at the same time!)
  
- Finally, checkin and this ends the merging operation  



ABOUT FOXBIN2PRG 2-WAY CONVERTER POR VFP 9:
------------------------------------------------------------------------
Updates of this tool and configuration instructions can be downloaded from the Open Source Project 
FOXBIN2PRG on CodePlex at https://vfpx.codeplex.com/wikipage?title=FoxBin2prg



FINAL NOTE:
------------------------------------------------------------------------
This program is Open Source and "libre", and I don't make any garanties that it fulfills your espectations
or that it will be free of bugs, that I will try to fix if my obligations let me do it.



LICENSE:
------------------------------------------------------------------------
This work is licensed under the Creative Commons Attribution 4.0 International License.
To view a copy of this license, visit http://creativecommons.org/licenses/by/4.0/.




ESPAÑOL ################################################################
Herramienta de Diff y Merge v2.3 en Visual FoxPro 9.0 para PlasticSCM 5
2013/12/20 -  Creado por Fernando D. Bozzo (fdbozzo@gmail.com)
########################################################################

Descargar de: https://github.com/fdbozzo/foxpro_plastic_diff_merge



¿QUÉ ES ESTA HERRAMIENTA Y CÓMO SE USA?
------------------------------------------------------------------------
Esta herramienta está pensada para usarse con Visual FoxPro 9 y PlasticSCM 5.
Facilita las operaciones de Diff y Merge sobre binarios VFP 9, mediante el uso
de una programa interfaz de Diff/Merge (foxpro_plasticscm_dm.exe) y un conversor
de binarios-texto bidireccional (FoxBin2prg.exe)



CONFIGURACIÓN DE DIFF EN PLASTICSCM:
------------------------------------------------------------------------
- Clickear en el icono de Preferencias de PlasticSCM
- Seleccionar "Herramientas Diff"
- Para cada extensión* binaria FoxPro "agregar" esto:
	- Herramienta Diff externa: "<path>\foxpro_plasticscm_dm.exe" "'DIFF' '@sourcefile' '@destinationfile' '@sourcesymbolic' '@destinationsymbolic'"
	- Pattern: .pjx     (¡usar misúsculas!)
- Clickear OK
- Mover la extension agregada al inicio de la lista, para priorizarla
- Repetir esta operación para cada extensión binaria soportada (*Nota 1)

*Nota 1: Las extensiones soportadas son: pjx,vcx,scx,frx,lbx,mnx,dbf,dbc



CONFIGURACIÓN DE MERGE EN PLASTICSCM:
------------------------------------------------------------------------
- Clickear en el icono de Preferencias de PlasticSCM
- Seleccionar "Herramientas Merge"
- Para cada extensión* binaria FoxPro "agregar" esto:
	- Herramienta Merge externa: "<path>\foxpro_plasticscm_dm.exe" "'PRESERVE_WS'"
	- Pattern: .pjx     (¡usar misúsculas!)
- Clickear OK
- Mover la extension agregada al inicio de la lista, para priorizarla
- Repetir esta operación para cada extensión binaria soportada (*Nota 2)

*Nota 2: Visual FoxPro binary extension are: pjx,pjt,vcx,vct,scx,sct,frx,frt,lbx,lbt,mnx,mnt,dbf,fpt,cdx,dbc,dcx,dct



CONFIGURACIÓN DE Custom "Open with...":
------------------------------------------------------------------------
- Click on PlasticSCM Preferences icon
- Select "Custom Open with..."
- Click "Add..." and complete the fields:
     Display Name:                FoxBin2Prg
	 Full path to the executable: <Path-To-FoxBin2Prg>\foxbin2prg.exe
- Click OK

*Nota 3: Usaremos esto desde la interfaz como truco para convertir a texto o a binario
*Nota 4: También puede agregar Notepad++, es útil para ver archivos de texto desde la interfaz de Plastic



USO:
------------------------------------------------------------------------
- Cuando se haga una operación de Diff, debe pulsar "CTRL+D" para usar la herramienta externa con las
  extensiones soportadas (ver la "*Nota 1" previa), pero mi recomendación es usar Diff solo en las
  versiones texto, por lo que tenga cuidado de regenerar las versiones texto cuando termine de editar
  los binarios en el IDE de FoxPro

- Cuando se haga la operación de Merge, la idea es procesar todos los archivos para que los binarios
  pasen directamente a la ventana de "Cambios Pendientes", de forma que solo necesite mergear sobre
  las versiones texto. Si quedaran binarios, selecciónelos, use click-derecho sobre ellos y elija
  mantener los cambios en el "origen" (no se preocupe de este, porque de todas formas luego los
  volverá a regenerar a todos)

- Cuando el Merge termine, vaya a la ventana de "Cambios Pendientes", regenere todos los binarios
  seleccionando las versiones texto, haga click-derecho sobre los mismos y elija "Abrir / Abrir con..." FoxBin2Prg
  (¡de a uno, que si no Plastic los lanzará todos a la vez!)

- Finalmente, haga el checkin y con esto termina la operación de merge

  

SOBRE EL CONVERSOR DE DOBLE-VIA FOXBIN2PRG PARA VFP 9:
------------------------------------------------------------------------
Las actualizaciones e instrucciones de configuración de esta herramienta pueden ser descargadas
del Proyecto Open Source FOXBIN2PRG en CodePlex, en https://vfpx.codeplex.com/wikipage?title=foxbin2prg_es



NOTA FINAL:
------------------------------------------------------------------------
Este programa es Open Source y "libre", y como tal no ofrezco garantías de que cumpla con sus espectativas
o de que está libre de fallos, que intentaré solucionar si me reporta y mis obligaciones me lo permiten.



LICENCIA:
------------------------------------------------------------------------
Esta obra está sujeta a la licencia Reconocimiento-CompartirIgual 4.0 Internacional de Creative Commons.
Para ver una copia de esta licencia, visite http://creativecommons.org/licenses/by-sa/4.0/deed.es_ES.
