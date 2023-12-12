#Pasos para iniciar 

1. Crear una carpeta con el nombre del proyecto
2. Agrega el canal Conda-Forge a tu configuración global: //Conda config --add channels conda-forge o //pip install cookiecutter
3. Crea un ambiente virtual que contenga a Coockiecutter: //conda create --name <nombre_ambiente> coockiecutter=1.7.3
4. Activa el ambiente virtual: //conda activate <nombre_ambiente>
5. Definir en dónde estará tu ambiente: // conda env export --from-history --file environment.yml

#Puede trabjar en el entorno base 

#Crear plantilla 
Ir a la terminar en la carpeta donde este cookicutter y utilizar el siguiente comando 

1. cookiecutter . //crea un acarpeta donde esta cookicutter y sigue los pasos de la terminal 

Introducción a Hooks
Los Hooks son sentencias que se van a ejecutar antes o después de generar la plantilla de datos. Por ejemplo, puedes usarlos para verificar el nombre de una carpeta, actualizar git, etc.

Implementación de Hooks
Se crea la carpeta “hooks”, adentro de la carpeta principal de tu proyecto.
Dentro de la carpeta se agregan los archivos “pre_gen_project.py” (lo que se ejecuta antes de generar la plantilla) y “pos_gen_project.py” (lo que se ejecuta después de generar la plantilla).
Por ejemplo, en “pre_gen_project.py” se puede inicializar git o validar nombres y archivos para evitar errores.

En el archivo “pos_gen_project.py” se puede hacer el primer commit en git o mostrar la finalización de la instalación de dependencias.

2. Para crear en otra carpeta desde git utiliza // cookiecutter https://github.com/dparedes616/Cookiecutter

