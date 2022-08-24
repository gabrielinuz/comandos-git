# comandos-git
## Anotación de comandos de GIT, los corchetes < y > solo se usan para definir que algo es condición para ejecutar un comando, no se deben escribir.

### 0.Guardar credenciales:
```git config --global credential.helper store```
  Asegurarse de estar parado en una carpeta que sea un repo cualquiera y luego ejecutar:
```git pull```
Luego de hacer el pull te pedirá tus credenciales (username y password) y estos datos serán guardados en un archivo en el disco (en la ubicación ~/.git-credentials). Esto quiere decir que no te los pedirá mas.


### 1.Clonar el repositorio (descargarlo en nuestra computadora):

```git clone <https://link-con-nombre-del-repositorio>```
  
### 2.Moverse al directorio del repositorio descargado (no es un comando de git, pero siempre nos olvidamos):

```cd <directorio del repositorio descargado>```
  
### 3.Crear una rama, una raminifcación para poder modificar el código y mantener intacta la rama principal:
  
  ```git branch <nombre-de-la-rama>```
  
### 4.Movernos a esa rama para trabajar:
  
  ```git checkout <nombre-de-la-rama>```
  
### 5.Los pasos 4 y 5 se pueden hacer en un solo comando para crear y moverme a la rama en un solo paso:

  ```git checkout -b <nombre-de-la-rama>```
  
### 6.Luego de agregar alguna funcionalidad o editar código, se pueden añadir estos cambios con el siguiente comando:

  ```git add <archivo o archivos modificados se parados por espacio que se deben subir>```
  
  También se puede agregar todo con:
  
  ```git add -A```
  
  ó
  
  ```git add *```
  
### 7.Git commit es como establecer un punto de control en el proceso de desarrollo. Es necesario escribir un mensaje corto para explicar qué hemos desarrollado o modificado en el código fuente. **Importante: Git commit guarda tus cambios únicamente en local, no en el servidor remoto, para eso precisamos usar el comando a continuación.**

  ```git commit -a -m <"mensaje-entre-comillas-que-explique-brevemente-la-corrección-o-funcionalidad-agregada">```
  
### 8.Subir tu commit o commits que hayas hecho al servidor remoto, siempre trabajando con el branch (rama) creado

  ```git push origin <nombre-de-la-rama>```

### 9.Siempre podemos usar el comando git status para saber el estado actual y la información del repositorio:

   ```git status```

### 10.Tomar los cambios del repositorio remoto, pero no aplicarlos (merge)

   ```git fetch <origen> <destino_nombre_de_la_rama>```

### 11.Aplicar los cambios del repositorio remoto tomados con (fetch)

   ```git merge <origen> <destino_nombre_de_la_rama>```

### 12.El comando git pull se utiliza para recibir actualizaciones del repositorio remoto. Es una combinación para aplicar git fetch y git merge en un solo comando.

   ```git pull <origen> <destino_nombre_de_la_rama>``` 
   
   *Por ejemplo: ```git pull origin main```*
