# ArchivosAngular
# UTN FRA 2016

Ejemplo de la carga de archivos usando Angularjs, el modulo Angular File Upload y Bootstrap.

Documentacion de File Upload:
	https://github.com/nervgh/angular-file-upload/wiki/Module-API.
Documentacion de Angularjs:
	https://docs.angularjs.org/api.
Documentacion de Bootstrap:
	http://getbootstrap.com/components/.

# USO BASICO
1- Descargar el modulo File Upload y cargarlo en el index.html.

2- Incluir la dependencia 'angularFileUpload' en mi modulo angular.

3- Inyectar 'FileUploader' en el controlador.

4- Si queremos tener la vista previa de los archivos crear la directiva "ngThumb".

5- Inicializar el uploader: $scope.uploader = new FileUploader({url: 'php/upload.php'}), en mi controlador.

6- Creamos el archivo upload.php que es el que se encarga de cargar los archivos.

7- En el form html crear un input tipo "file" con la directiva nvFileSelect y el uploader:
	<input type="file" nv-file-select uploader="uploader"/>.
	Si quiero usar drag and drop uso las directivas nvFileDrop y nvFileOver.
	Para cargar varios archivos juntos agregar la directiva "multiple":
	<input type="file" nv-file-select uploader="uploader" multiple/>.

8- Para cargar los archivos tenemos dos maneras:
	a- Recorrermos la propiedad uploader.queue, que tiene los archivos a cargar, y usamos los metodos de c/u:
		remove(), upload() y cancel()*.
	b- Utilizamos los metodos del uploader:
		uploadAll(), cancelAll(), uploadItem(item), cancelItem(item)*.
	* Ver en la documentacion todas las propiedades, metodos y callbacks disponibles.
