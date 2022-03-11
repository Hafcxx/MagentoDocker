# Docker Magento 2 

_Implementación proyecto Magento 2 en entorno Docker_

### 0. Pre-requisitos 📋

0.1 Primero instalar Docker y Docker Compose:

### 1. Clonar repositorio

_Clonar Repositorio._
```
git clone xxxxxx
```
_Una vez clonado el repositorio configurar la terminal en la direccion del repositorio_

```
cd magento
```

### 2. Compilación 🔧
2.0 Cambiar permisos de los archivos bash, ejecutar comando:
```
chmod +x bin/* 
```
2.1 Crear el directorio data, ejecutar comando:
```
bin/create_folder
```
2.2 Completado los puntos anteriores, procedemos con la ejecución del docker-compose.yml de la siguiente manera:
```
bin/build
```
2.3 Para validar que los contenedores esten ejecutados correctamente 
```
docker-compose ps
```
_Todos los contenedores deben estar en status UP_ 

2.4 Instalar dependencias de Magento
```
bin/composer install
```
2.5 Instalar Magento
```
bin/install_magento
```
2.6.1 Crear dominio en el archivo host
_Linux_
```
echo "127.0.0.1 ::1 magento.test" | sudo tee -a /etc/hosts 
```
_Windows_
[Hosts Windows](doc/hosts_windows.md)

2.8 Cree un usuario para el administrador de magento

El siguiente comando le solicitará los siguientes datos _nombre de administrador_, _contraseña_, _email_, _firstname_, _lastname_ que debes ir ingresandolos cada vez que se solicita, en caso de que no ingreses algunos de estos datos NO se ejecutara el comando interno dentro de este script.

```
bin/create_user_magento
```

2.9 Finalmente ingresar a las siguiente rutas:

* [http://magento.test](http://magento.test)
* [http://magento.test/admin](http://magento.test/admin)

## 3. Scripts

Todos los script se encuentran dentro de la carpeta bin
#### Para ver lista de comando ingresar [aqui](doc/script.md)

## 4. Construido con 🛠️

_Menciona las herramientas que utilizaste para crear tu proyecto_

* [Visual Studio Code](https://code.visualstudio.com/) - El framework web usado
* [Docker](https://hub.docker.com/) - Documentación y referencias
* [Docker extension](https://marketplace.visualstudio.com/items?itemName=ms-azuretools.vscode-docker) - Visualización y administración de contenedores
* [WSL Windows 10]()
* [WSL Windows 11]()