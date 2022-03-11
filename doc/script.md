## 3. Scripts

Todos los script se encuentran dentro de la carpeta bin
#### Los siguientes comando son ejemplos de ejecución

* create_folder: Permite Crear las carpetas necesesarias para el inicio del proyecto (Solo usar la primera vez)
```
bin/create_folder
```
* install_magento: Ejecuta el script de instalacion de magento (Solo usar la primera vez)
```
bin/install_magento
```
* build: Ejecuta el script de docker-compose y levanta los contenedores
```
bin/build
```
* composer: Permite ejecutar todas las instrucciones de composer
```
bin/composer --version
```
* create_user_magento: Crea usuario administrador de magento (revisar punto 2.8)
```
bin/create_user_magento 
```
* magento: Permite ejecutar todas las instrucciones de magento por separado
```
bin/magento cache:clear
```
* full_magento: Ejecuta el script completo de magento
```
bin/full_magento
```
* indexer: Ejecuta el script de limpieza de indices de magento
```
bin/indexer
```
* mode_magento: Ejecuta el script para cambiar de modos de magento (Developer, Default, Production)
```
bin/mode_magento
```
* restart: Reinicia los contenedores
```
bin/restart
```
* start: Inicia los contenedores
```
bin/start
```
* stop: Detiene los contenedores
```
bin/stop
```
* rabbitmq: Permite habilitar el servicio de RabbitMQ en magento
```
bin/rabbitmq
```
* redis_enable: Permite habilitar el servicio de Redis en magento
```
bin/redis_enable
```
* redis_fpc: Permite habilitar Redis para FPC de magento
```
bin/redis_fpc
```
* redis_session: Permite habilitar Redis para sessiones de magento
```
bin/redis_session
```