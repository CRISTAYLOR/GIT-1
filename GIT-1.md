Práctica: Introducción a Git - 40 Ejercicios Básicos

Ejercicio 1: Verificar la Instalación de Git
Antes de comenzar, asegúrate de que Git está instalado en tu sistema.
Instrucciones Detalladas:
	•	Abre una terminal o línea de comandos en tu computadora.
	•	Escribe el comando que te permitirá verificar si Git está instalado y cuál es su versión actual.
	•	Si Git no está instalado, investiga cómo instalarlo en tu sistema operativo (por ejemplo, Windows, macOS o Linux).

Preguntas a responder:
	•	¿Qué comando debes usar para verificar la versión de Git?
		
		Git --version

	•	Si no tienes Git instalado, ¿qué opciones tienes para instalarlo?

	En terminal escribimos :
	Git init
	Luego:
	FORMA DE INSTALARLO POR CONSOLA:
	$ yum install curl-devel expat-devel gettext-devel \
	openssl-devel zlib-devel
	$ apt-get install libcurl4-gnutls-dev libexpat1-dev gettext \
	libz-dev libssl-dev
	LUEGO:
	$ tar -zxf git-2.0.0.tar.gz
	$ cd git-2.0.0
	$ make configure
	$ ./configure --prefix=/usr
	$ make all doc info
	$ sudo make install install-doc install-html install-info
	FINALMENTE: 
	Una vez hecho esto, también puedes obtener Git, a través del propio Git, para futuras actualizaciones:
		•	$ git clone git://git.kernel.org/pub/scm/git/git.git

Ejercicio 2: Crear un Directorio de Trabajo
Crea un directorio donde trabajarás en este proyecto.
Instrucciones Detalladas:
	•	En tu terminal, navega hasta la ubicación donde deseas crear el directorio. Por ejemplo, podrías crearlo en tu carpeta "Documentos".
	•	Usa un comando para crear un nuevo directorio llamado mi-proyecto-git.
	•	Cambia al directorio recién creado para comenzar a trabajar en él.
Preguntas a responder:
	•	¿Qué comando usas para crear un nuevo directorio?

		Echo “texto random” > nombredearchivo.txt
		O
		Git add .\nombredearchivo.txt

	•	¿Cómo puedes cambiar a un directorio específico desde la terminal?

	con este comando:
	Cd ./nombre del directorio

Ejercicio 3: Inicializar un Repositorio Git
Convierte tu directorio de trabajo en un repositorio Git.
Instrucciones Detalladas:
	•	Asegúrate de estar dentro del directorio mi-proyecto-git que creaste en el ejercicio anterior.
	•	Escribe el comando necesario para inicializar Git en este directorio. Esto creará un directorio oculto llamado .git donde Git almacenará toda la información del repositorio.
Preguntas a responder:
	•	¿Qué comando usas para inicializar Git en un directorio?
		
		Git init

	•	¿Cómo puedes confirmar que Git ha sido inicializado correctamente?
		
		Git --version

Ejercicio 4: Comprobar el Estado del Repositorio
Verifica el estado actual de tu repositorio.
Instrucciones Detalladas:
	•	Dentro del directorio mi-proyecto-git, escribe el comando que te mostrará el estado actual del repositorio.
	•	Observa la salida del comando y asegúrate de que no haya archivos pendientes de seguimiento ni cambios no guardados.
Preguntas a responder:
	•	¿Qué comando usas para comprobar el estado del repositorio?
		
		Git status

	•	¿Qué significa cuando Git dice que no hay archivos rastreados?
		
		Luego de un ls hará una lista de lo que contenga, los rastreados son los que se incluyen

Ejercicio 5: Crear un Archivo y Verificar el Estado
Crea un archivo en tu repositorio y verifica cómo cambia el estado del mismo.
Instrucciones Detalladas:
	•	Crea un archivo llamado README.md dentro de tu directorio mi-proyecto-git. Puedes hacerlo directamente desde la terminal o usando un editor de texto.
	•	Vuelve a comprobar el estado del repositorio para ver cómo Git reconoce este nuevo archivo.
Preguntas a responder:
	•	¿Qué comando usas para crear un archivo nuevo desde la terminal?
		
		echo > archivo.txt
	•	¿Qué diferencia observas en el estado del repositorio después de crear el archivo?
		
		Que demora un muy poco tiempo 
		y que me permite luego listar para comprobar que lo creó


Ejercicio 6: Añadir un Archivo al Área de Preparación
Prepara el archivo README.md para ser guardado en el próximo commit.
Instrucciones Detalladas:
	•	Usa el comando adecuado para añadir el archivo README.md al área de preparación (staging area).
	•	Vuelve a comprobar el estado del repositorio para confirmar que el archivo ha sido añadido correctamente.
Preguntas a responder:
	•	¿Qué comando usas para añadir un archivo al área de preparación?
	
		Git add README.md
		Luego lo confirmo con
		Git status

	•	¿Qué significa añadir un archivo al área de preparación?
		
		Que nos guarda ese archivo en el repositorio

Ejercicio 7: Realizar un Commit
Guarda los cambios realizados en el repositorio mediante un commit.
Instrucciones Detalladas:
	•	Escribe el comando necesario para realizar un commit. Al hacerlo, incluye un mensaje claro que describa lo que has hecho. Por ejemplo: "Añadido archivo README.md".
	•	Después del commit, verifica nuevamente el estado del repositorio para asegurarte de que no quedan cambios pendientes.
Preguntas a responder:
	•	¿Qué comando usas para realizar un commit? 
		
		Uso: Git commit "Añadido archivo"

	•	¿Por qué es importante incluir un mensaje claro en cada commit?
		
		Para confirmar que he realizado todo correctamente

Ejercicio 8: Ver el Historial de Commits
Consulta el historial de commits realizados en tu repositorio.
Instrucciones Detalladas:
	•	Escribe el comando que te permitirá ver el historial de commits realizados en tu repositorio.
	•	Observa la salida del comando y asegúrate de que puedas identificar el commit que acabas de realizar.
Preguntas a responder:
	•	¿Qué comando usas para ver el historial de commits?
		
		Usamos Git log

	•	¿Qué información muestra el historial de commits?
		
		En donde está ubicado, el autor y la fecha completa de realización

Ejercicio 9: Crear una Nueva Rama
Crea una nueva rama para trabajar en una característica específica.
Instrucciones Detalladas:
	•	Usa el comando adecuado para crear una nueva rama llamada nueva-caracteristica.
	•	No te preocupes por moverte a esta rama todavía; solo crea la rama por ahora.
Preguntas a responder:
	•	¿Qué comando usas para crear una nueva rama en Git?
		
		Git Branch nueva-caracteristica

	•	¿Qué diferencia hay entre crear una rama y moverte a ella? 
	
		Que se usa otro comando
		Git checkout nueva-caracteristica

Ejercicio 10: Listar Todas las Ramas
Enumera todas las ramas existentes en tu repositorio.
Instrucciones Detalladas:
	•	Escribe el comando que te permitirá listar todas las ramas disponibles en tu repositorio.
	•	Observa la salida del comando y asegúrate de que puedes identificar tanto la rama principal (main o master) como la rama que acabas de crear.
Preguntas a responder:
	•	¿Qué comando usas para listar todas las ramas en Git?
		
		Git Branch -a

	•	¿Cómo puedes identificar en qué rama estás trabajando actualmente?
		
		Solo con escribir: git Branch, marcará con un * la que estéis usando

Ejercicio 11: Cambiar a una Rama Existente
Mueve tu trabajo a la rama nueva-caracteristica que creaste en el ejercicio anterior.
Instrucciones Detalladas:
	•	Usa el comando adecuado para cambiar a la rama nueva-caracteristica.
	•	Verifica que estás trabajando en la rama correcta usando un comando que te muestre en qué rama estás actualmente.
Preguntas a responder:
	•	¿Qué comando usas para cambiar de rama?
		
		Git checkout “nombre de la rama” y git branch

	•	¿Cómo puedes confirmar en qué rama estás trabajando?
		
		Git Branch -a, 
		en la que esté trabajando estará seleccionada con un * y será la primera en la lista y también el comando:  git branch

Ejercicio 12: Crear y Cambiar a una Nueva Rama en un Solo Paso
Crea una nueva rama llamada mejoras-ui y cambia a ella inmediatamente.
Instrucciones Detalladas:
	•	Usa un comando que permita crear y cambiar a una nueva rama en un solo paso.
	•	Verifica que ahora estás trabajando en la rama mejoras-ui.
Preguntas a responder:
	•	¿Qué comando permite crear y cambiar a una nueva rama en un solo paso?
		
		Git switch -c mejoras-ui

	•	¿Cuál es la ventaja de usar este comando?
		
		Creas y cambias de rama en una sola línea

Ejercicio 13: Añadir Archivos al Área de Preparación con un Comando Abreviado
Prepara todos los archivos nuevos o modificados en tu directorio para ser guardados.
Instrucciones Detalladas:
	•	Modifica o crea un archivo nuevo en tu directorio.
	•	Usa un comando abreviado para añadir todos los cambios (nuevos, modificados o eliminados) al área de preparación.
Preguntas a responder:
	•	¿Qué comando abreviado puedes usar para añadir todos los cambios al área de preparación?
		
		Git add

	•	¿Qué ventajas tiene usar este comando en lugar de añadir archivos individualmente?

		Es más práctico y directamente crea el file necesario

Ejercicio 14: Realizar un Commit con un Mensaje Descriptivo
Guarda los cambios realizados en la rama mejoras-ui mediante un commit.
Instrucciones Detalladas:
	•	Escribe un mensaje claro que describa los cambios realizados. Por ejemplo: "Actualización inicial de la interfaz de usuario".
	•	Verifica que el commit fue realizado correctamente comprobando el historial de commits.
Preguntas a responder:
	•	¿Qué comando usas para realizar un commit?
		
		Git commit "texto"

	•	¿Por qué es importante escribir mensajes descriptivos en los commits?
		
		Para confirmar que los archivos fueron creados correctamente y que se ha realizado el cometido

Ejercicio 15: Fusionar Ramas
Fusiona los cambios realizados en la rama mejoras-ui con la rama principal (main o master).
Instrucciones Detalladas:
	•	Cambia a la rama principal (main o master).
	•	Usa el comando adecuado para fusionar los cambios de la rama mejoras-ui en la rama principal.
Preguntas a responder:
	•	¿Qué comando usas para fusionar ramas en Git?
		
		git merge mejoras-ui

	•	¿Qué sucede si hay conflictos durante la fusión?
		
		No fusionan y genrra un mensaje de qu3 se debe solucionar


Ejercicio 16: Resolver Conflictos entre Ramas
Introduce un conflicto intencional al modificar el mismo archivo en dos ramas diferentes y resuélvelo.
Instrucciones Detalladas:
	•	Crea una nueva rama llamada conflicto-test.
	•	Modifica un archivo en ambas ramas (main y conflicto-test) de manera que introduzcas un conflicto.
	•	Intenta fusionar la rama conflicto-test con la rama principal y resuelve el conflicto manualmente.
Preguntas a responder:
	•	¿Qué ocurre cuando Git detecta un conflicto durante la fusión? 
		
		genera yn m3nsaj3 que informa las diferencias con signos agregados mayor, menor e igual

	•	¿Cómo puedes resolver un conflicto en Git?
	
		se deben igualar los archivos en en conflicto y luego guardarlos, luego de esot te permitira fusionar las ramas

Ejercicio 17: Crear un Archivo .gitignore
Crea un archivo .gitignore para excluir ciertos tipos de archivos de ser rastreados por Git.
Instrucciones Detalladas:
	•	Crea un archivo llamado .gitignore en la raíz de tu repositorio.
	•	Agrega entradas para ignorar archivos como *.log, *.tmp y cualquier otro tipo de archivo temporal o irrelevante.
Preguntas a responder:
	•	¿Qué es un archivo .gitignore y para qué sirve?
		
		es la forma de que no se rastreen archivos que seleccione en las busquedas, y asi optimizarlas

	•	¿Cómo puedes especificar qué tipos de archivos deben ser ignorados?
		
		se pueden especificar por extensuon, por directorio y por clase de archivo

Ejercicio 18: Configurar Git para Ignorar Cambios en un Archivo Específico
Ignora los cambios en un archivo específico sin eliminarlo del repositorio.
Instrucciones Detalladas:
	•	Selecciona un archivo en tu repositorio que no quieras que Git rastree sus cambios.
	•	Usa un comando especial para indicarle a Git que ignore los cambios en ese archivo.
Preguntas a responder:
	•	¿Cómo puedes hacer que Git ignore los cambios en un archivo específico sin eliminarlo del repositorio? 
		
		con la creacion de un archivo de texto ,gitignore

	•	¿En qué situaciones sería útil esta técnica?
		
		cuando hay archivos que son innecesarios de ser rastreados en un repositorio


Ejercicio 19: Clonar un Repositorio Remoto
Clona un repositorio remoto existente en tu computadora local.
Instrucciones Detalladas:
	•	Busca un repositorio público en GitHub o GitLab.
	•	Usa el comando adecuado para clonar el repositorio en tu computadora.
Preguntas a responder:
	•	¿Qué comando usas para clonar un repositorio remoto?
		
		git clone <url>

	•	¿Qué diferencia hay entre clonar un repositorio y crear uno nuevo?
	
		clonar copia un repositorio existente, crear unicia uno nuevo vacio

Ejercicio 20: Conectarte a GitHub con SSH
Configura la autenticación SSH para conectarte a GitHub de forma segura.
Instrucciones Detalladas:
	•	Genera una clave SSH en tu computadora si aún no tienes una.
	•	Copia la clave pública generada y agrégala a tu cuenta de GitHub.
Preguntas a responder:
	•	¿Qué es SSH y por qué es importante para trabajar con Git?
	
		porque es mas seguro, cifra tus datos para protegerlos, 
		ademas permite no tener que poner tu contrasela.para acceder

	•	¿Cómo puedes generar una clave SSH en tu computadora?

		1 abre la terminar
		2 copia el siguiente comando
		ssh-keygen -t ed25519 -C "tu_correo@ejemplo.com"
		3 guarsamos clave y configuramos contraseña
		4 copiamos clave publica usando
		cat ~/.ssh/id_ed25519.pub
		5 agregamos y guardamos la pass
		Ve a GitHub → Settings → SSH and GPG keys → New SSH key.
		Pega la clave y guárda
		6 conformamos poniendo la sigiuente linea
		ssh -T git@github.com

Ejercicio 21: Subir Cambios Locales a GitHub
Sube tus cambios locales al repositorio remoto en GitHub.
Instrucciones Detalladas:
	•	Crea un repositorio vacío en GitHub.
	•	Asocia tu repositorio local con el remoto usando el comando adecuado.
	•	Sube tus cambios locales al repositorio remoto.
Preguntas a responder:
	•	¿Qué comando usas para asociar un repositorio local con uno remoto?
		
		git remote add origin <URL_DEL_REPOSITORIO>

	•	¿Qué comando usas para subir cambios locales a un repositorio remoto?
		
		git push -u origin "nombre de rama"


Ejercicio 22: Actualizar tu Repositorio Local desde GitHub
Descarga los últimos cambios del repositorio remoto en GitHub.
Instrucciones Detalladas:
	•	Supón que alguien más ha realizado cambios en el repositorio remoto.
	•	Usa el comando adecuado para actualizar tu repositorio local con los cambios remotos.
Preguntas a responder:
	•	¿Qué comando usas para descargar cambios del repositorio remoto?
		
		git fetch 
		o
		git pull origin <rama>

	•	¿Qué pasa si hay conflictos al sincronizar los cambios?

		Git marcará los archivos en conflicto y te pedirá resolverlos manualmente.
		Edita los archivos afectados y elige qué cambios conservar.
		Una vez resuelto el conflicto, escribe
		git add .
		git commit -m "Resolviendo conflictos de fusión"


Ejercicio 23: Crear una Rama en GitHub
Crea una nueva rama en tu repositorio remoto en GitHub.
Instrucciones Detalladas:
	•	Crea una nueva rama local llamada feature-nueva.
	•	Sube esta rama al repositorio remoto en GitHub.
Preguntas a responder:
	•	¿Cómo puedes subir una rama local a un repositorio remoto?
		
		git push -u origin feature-nueva

	•	¿Cómo puedes verificar que la rama ha sido creada correctamente en GitHub?

		Una de las formas es 
		git branch -r

Ejercicio 24: Eliminar una Rama Local
Elimina una rama local que ya no necesitas.
Instrucciones Detalladas:
	•	Selecciona una rama local que ya no uses.
	•	Usa el comando adecuado para eliminarla.
Preguntas a responder:
	•	¿Qué comando usas para eliminar una rama local?
		
		git branch -d nombre-de-la-rama

	•	¿Es posible recuperar una rama eliminada?
		
		si, este es el modo:	
		git reflog
		Luego crearla de nuevo
		git checkout -b nombre-de-la-rama hash-del-commit

Ejercicio 25: Eliminar una Rama Remota
Elimina una rama remota que ya no necesitas.
Instrucciones Detalladas:
	•	Selecciona una rama remota que ya no uses.
	•	Usa el comando adecuado para eliminarla desde el repositorio remoto.
Preguntas a responder:
	•	¿Cómo puedes eliminar una rama remota?
		
		con 
		git push origin --delete nombre-de-la-rama

	•	¿Qué precauciones debes tomar antes de eliminar una rama remota?
	
	1- que no tenga cambios propios o de otros, comandos:
	git log origin/nombre-de-la-rama
	2- avisar al equipo
	3- hacer un backup
	Sugerencia:
	git checkout nombre-de-la-rama
	git branch backup-nombre-de-la-rama

Ejercicio 26: Crear una Pull Request en GitHub
Solicita que tus cambios en una rama sean revisados y fusionados en la rama principal.
Instrucciones Detalladas:
	•	Trabaja en una rama nueva y realiza algunos cambios.
	•	Sube tus cambios al repositorio remoto.
	•	Crea una pull request en GitHub para solicitar la fusión de tu rama con la rama principal.
Preguntas a responder:
	•	¿Qué es una pull request y para qué sirve?
	
		Una Pull Request (PR) es una solicitud para fusionar (merge) los cambios de una rama a otra (generalmente la principal). Sirve para:
		1-Revisar el código antes de fusionarlo.
		2-Permitir comentarios y correcciones de otros desarrolladores.
		3-Mantener un historial claro de cambios en el proyecto.

	•	¿Qué información debes incluir en una pull request?
		
		1-Título claro y descriptivo
		2-Descripción detallada de los cambios
		3-Instrucciones adicionales (si es necesario)
		4-Relación con otros problemas o tareas
		5-Capturas de pantalla o GIFs (si es relevante)
		6-Checklist de tareas pendientes (opcional)

Ejercicio 27: Revisar y Comentar una Pull Request
Revisa una pull request existente y deja comentarios sobre los cambios propuestos.
Instrucciones Detalladas:
	•	Encuentra una pull request en tu repositorio de GitHub.
	•	Lee los cambios propuestos y deja comentarios relevantes.
Preguntas a responder:
	•	¿Cómo puedes revisar una pull request en GitHub?

		Ir a la pestaña Pull Requests en el repositorio.
		Seleccionar la PR y revisar los cambios en la pestaña Files changed.
		
	•	¿Qué tipo de comentarios son útiles en una revisión?

		Dejar comentarios línea por línea o en la conversación general.
		Usar "Review changes" para aprobar, comentar o solicitar cambios.

Ejercicio 28: Fusión Automática de una Pull Request
Fusiona automáticamente una pull request que no tiene conflictos.
Instrucciones Detalladas:
	•	Encuentra una pull request sin conflictos en tu repositorio.
	•	Usa la interfaz de GitHub para fusionarla automáticamente con la rama principal.
Preguntas a responder:
	•	¿Cuándo puedes fusionar una pull request automáticamente? 

		Puedes fusionar una PR automáticamente si:
		1-No hay conflictos entre la rama de la PR y la rama principal.
		2-Las pruebas y validaciones (si las hay) han pasado correctamente.
		3-Tienes permisos para fusionar cambios en el repositorio.

	•	¿Qué sucede después de fusionar una pull request?

		Los cambios de la PR se integran en la rama principal (usualmente main o master).
		GitHub marca la PR como "Merged" (Fusionada).
		Otros colaboradores pueden actualizar sus ramas locales con git pull origin main.

Ejercicio 29: Descartar Cambios Locales
Descarta accidentalmente cambios locales que no quieres guardar.
Instrucciones Detalladas:
	•	Modifica un archivo local sin añadirlo al área de preparación.
	•	Usa el comando adecuado para descartar estos cambios y restaurar el archivo a su estado anterior.
Preguntas a responder:
	•	¿Qué comando usas para descartar cambios locales?

		1-para un solo archivo
		git restore nombre-del-archivo
		2-para todos
		git restore .

	•	¿Cuándo es útil descartar cambios locales?
		1-Cuando cometiste un error y quieres recuperar el archivo original.
		2-Si hiciste pruebas y quieres revertirlas antes de hacer un commit.
		3-Si descargaste cambios remotos (git pull) y quieres descartar modificaciones locales antes de actualizar.

Ejercicio 30: Restaurar un Commit Anterior
Restaura tu repositorio a un commit anterior.
Instrucciones Detalladas:
	•	Identifica un commit anterior en el historial de commits.
	•	Usa el comando adecuado para restaurar tu repositorio a ese commit específico.
Preguntas a responder:
	•	¿Qué comando usas para restaurar un commit anterior?

		1-uso para ver la lista
		git log --oneline
		2-luego
		git reset --hard <commit-hash>
		puedo elegir entre:
		--soft: Mantiene los archivos modificados en staging.
		--mixed: Mantiene los archivos modificados sin incluirlos en staging.
		--hard: Borra todos los cambios posteriores a ese commit.
		3-finalmente si necesito dehacer cambios uso
		git revert <commit-hash>


	•	¿Qué precauciones debes tomar al restaurar un commit anterior?
	
		1-Si uso git reset --hard, perderás los cambios posteriores a menos que los guardes antes.

		2-Si ya he subido cambios a un repositorio remoto, usar reset puede generar problemas para otros colaboradores. En este caso, es mejor usar git revert.

		3-Si trabajo en una rama compartida, consulta con el equipo antes de realizar cambios destructivos.

		4-Guardo tu trabajo antes de hacer un reset con un branch temporal o un stash:
		git branch backup-antes-de-reset
		git stash

		5-Creo un TAG asociado (si es necesario):
		Usa el siguiente comando para crear un tag anotado (recomendado):
		git tag -a v1.0 123abcd -m "Versión 1.0 - Estable"

			Si solo necesito un tag ligero (sin descripción), usa:
			git tag v1.0 123abcd

		6-Verificar si se creo el TAG
		
		a-Listar:
		git tag
		
		b-Ver detalles del TAG:
		git show v1.0

Ejercicio 31: Crear un Tag para Marcar una Versión
Crea un tag para marcar una versión específica de tu proyecto.
Instrucciones Detalladas:
	•	Elige un commit en el historial de tu repositorio que quieras marcar como una versión importante (por ejemplo, v1.0).
	•	Usa el comando adecuado para crear un tag asociado a ese commit.
	•	Verifica que el tag ha sido creado correctamente.
Preguntas a responder:
	•	¿Qué es un tag en Git y para qué sirve?

		Un tag en Git es una referencia a un commit específico, utilizada para marcar versiones importantes en el historial del repositorio, como lanzamientos de software (v1.0, v2.0). A diferencia de las ramas, los tags son inmutables y no avanzan con nuevos commits.

	•	¿Cómo puedes crear un tag asociado a un commit específico?
	
		historial de commits y encontrar el especifico:
		git log --oneline
		
		asi sale:
		a1b2c3d Nueva funcionalidad agregada
		f4e5d6c Corrección de errores
		123abcd Versión estable lista para producción

		Si queremos etiquetar el commit 123abcd como v1.0, tomamos su hash.


Ejercicio 32: Listar Todos los Tags en tu Repositorio
Enumera todos los tags existentes en tu repositorio.
Instrucciones Detalladas:
	•	Escribe el comando que te permitirá listar todos los tags disponibles en tu repositorio.
	•	Observa la salida del comando y asegúrate de que puedas identificar los tags que has creado.
Preguntas a responder:
	•	¿Qué comando usas para listar todos los tags en Git?
		
		git tag

	•	¿Por qué es útil tener tags en un proyecto?

		Marcan versiones importantes: Facilitan la identificación de versiones estables (v1.0, v2.0).
		Facilitan despliegues: Permiten que los equipos de DevOps seleccionen versiones específicas para producción.
		Ayudan en la depuración: Si surge un problema en producción, puedes comparar versiones fácilmente.
		Son inmutables: A diferencia de las ramas, los tags no cambian con nuevos commits, lo que garantiza referencias estables.

Ejercicio 33: Subir Tags al Repositorio Remoto
Sube los tags locales al repositorio remoto en GitHub.
Instrucciones Detalladas:
	•	Selecciona uno o más tags locales que quieras compartir con el repositorio remoto.
	•	Usa el comando adecuado para subir estos tags al repositorio remoto.
Preguntas a responder:
	•	¿Cómo puedes subir tags locales a un repositorio remoto?

		git push origin <tag-name>
		git push --tags

	•	¿Qué pasa si intentas subir un tag que ya existe en el repositorio remoto?
	
		Da un mensaje de error como este! 
		[rejected]        v1.0 -> v1.0 (already exists)


Ejercicio 34: Descargar Tags del Repositorio Remoto
Descarga los tags existentes desde el repositorio remoto.
Instrucciones Detalladas:
	•	Asegúrate de estar conectado al repositorio remoto en GitHub.
	•	Usa el comando adecuado para descargar todos los tags disponibles en el repositorio remoto.
Preguntas a responder:
	•	¿Qué comando usas para descargar tags desde un repositorio remoto?

		git fetch --tags

	•	¿Cuándo sería útil descargar tags desde un repositorio remoto?

		Si otro colaborador ha creado tags nuevos en el repositorio remoto y deseas obtenerlos.
		Antes de realizar un despliegue, para asegurarte de que tienes la última versión etiquetada.
		Si necesitas verificar qué versiones están disponibles en el repositorio antes de hacer un checkout o revertir a una versión anterior.

Ejercicio 35: Revertir un Commit
Revierte un commit específico sin perder los commits posteriores.
Instrucciones Detalladas:
	•	Identifica un commit en el historial que quieras revertir.
	•	Usa el comando adecuado para revertir este commit, creando un nuevo commit que deshaga los cambios realizados.
Preguntas a responder:
	•	¿Qué diferencia hay entre revertir un commit y eliminarlo del historial?
	
		git revert crea un nuevo commit que deshace los cambios, pero mantiene el historial intacto.
		git reset --hard <commit> elimina commits del historial, lo que puede causar problemas si el código ya fue compartido con otros.

	•	¿Por qué es útil usar revert en lugar de simplemente eliminar un commit?

		Mantiene el historial limpio y transparente.
		Evita conflictos con otros colaboradores.
		Es seguro incluso si el commit ya fue subido a un repositorio remoto.

Ejercicio 36: Eliminar un Commit del Historial
Elimina un commit específico del historial de tu repositorio.
Instrucciones Detalladas:
	•	Identifica un commit en el historial que quieras eliminar permanentemente.
	•	Usa un comando avanzado para modificar el historial y eliminar este commit.
	•	Ten cuidado, ya que esta operación puede afectar a otros desarrolladores si el repositorio es compartido.
Preguntas a responder:
	•	¿Qué comando puedes usar para eliminar un commit del historial?

		Puedes usar git rebase -i <commit-hash>^ para realizar una rebase interactiva y eliminar un commit del historial.

	•	¿Cuándo es seguro usar este comando en un repositorio compartido?
	
		Nunca es seguro usar este comando si el commit ya ha sido compartido con otros colaboradores en un repositorio remoto.
		Es seguro usarlo solo si el commit que deseas eliminar está en una rama local que no ha sido empujada al repositorio remoto, o si trabajas solo en esa rama y nadie más depende de ella.
		Si decides usar git rebase en un repositorio compartido, necesitarás forzar el push con git push --force, lo que puede sobrescribir el historial para otros colaboradores y causar problemas si no están al tanto.

Ejercicio 37: Comparar Ramas
Compara los cambios entre dos ramas diferentes.
Instrucciones Detalladas:
	•	Selecciona dos ramas en tu repositorio (por ejemplo, main y feature-nueva).
	•	Usa el comando adecuado para comparar los cambios entre estas dos ramas.
Preguntas a responder:
	•	¿Qué comando usas para comparar ramas en Git?

		Usas git diff <rama1>..<rama2> para comparar las diferencias entre dos ramas.

	•	¿Qué información muestra esta comparación?

		Muestra las líneas modificadas, archivos modificados y las diferencias específicas en el contenido de esos archivos entre las dos ramas.

Ejercicio 38: Deshacer Cambios en un Archivo Específico
Deshaz accidentalmente los cambios realizados en un archivo específico sin afectar otros archivos.
Instrucciones Detalladas:
	•	Modifica un archivo en tu repositorio sin añadirlo al área de preparación.
	•	Usa el comando adecuado para restaurar este archivo a su estado anterior sin afectar otros archivos modificados.
Preguntas a responder:
	•	¿Cómo puedes deshacer cambios en un archivo específico?

		Para deshacer los cambios en un archivo específico, usa git checkout -- <archivo>. Este comando restaurará el archivo a su último estado confirmado (commit), sin afectar otros cambios en el repositorio.

	•	¿Qué ventajas tiene esta técnica sobre descartar todos los cambios locales?

		1-Mayor control: Puedes elegir deshacer los cambios solo en un archivo específico, sin perder el trabajo realizado en otros archivos.
		2-Menos riesgos: Evitas descartar cambios que tal vez no quieras perder en otros archivos.
		3-Preservación de trabajo parcial: Permite que continúes trabajando en archivos modificados sin tener que descartar todo el trabajo localmente.

Ejercicio 39: Usar Alias para Simplificar Comandos
Crea un alias para simplificar comandos frecuentes en Git.
Instrucciones Detalladas:
	•	Selecciona un comando Git que uses con frecuencia (por ejemplo, git status).
	•	Crea un alias personalizado para este comando usando el comando de configuración de Git.
	•	Prueba tu nuevo alias para asegurarte de que funciona correctamente.
Preguntas a responder:
	•	¿Qué es un alias en Git y para qué sirve?

		Un alias en Git es un nombre personalizado que se asigna a un comando de Git, permitiendo usar versiones más cortas o más fáciles de recordar de comandos largos.

	•	¿Cómo puedes crear un alias personalizado para un comando Git?

		con el siguiente comando:
		git config --global alias.<alias> <comando>
