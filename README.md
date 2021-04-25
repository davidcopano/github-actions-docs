# Github Actions Docs

Documentación propia de Github Actions.

| Acción | Pasos para realizar la acción |
| ------------- | ------------- |
| Subir release a Github | 1) En el archivo `.github\workflows\<NOMBRE_ARCHIVO>.yml` añadir lo siguiente (entre las claves `name` y `jobs`): <br> ![on push tags](on-push-tags.png?raw=true "on push tags")<br> Ejemplo completo: <br> ![publish release](publish-release.png?raw=true "publish release") <br>2) Crear el tag con este comando (reemplazar las X con la versión que sea): `git tag vX.X.X`<br> 3) Hacer commit de todos los cambios que vayan a incluirse en el tag. <br> 4) Subir el tag creado con el siguiente comando: `git push --tags` <br> La acción del archivo .yml se ejecutará una vez se cree el tag y se suba al repositorio (pasos 2, 3 y 4) |