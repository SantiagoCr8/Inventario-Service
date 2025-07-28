# Inventario-Service

![Build Status](https://img.shields.io/badge/build-passing-brightgreen)  
![License](https://img.shields.io/badge/license-MIT-blue)

## Descripción
Es un microservio que ayuda a la gestion de inventario

## Prerequisitos
¿Qué necesitas instalado en tu máquina?
```bash
- Java 17
- Maven 3.8+
```
Entra a este repositorio https://github.com/SantiagoCr8/Producto-Servise.git y has el proceso de instalacion

## Instalacion
Crea una carpeta donde se va ha guardar el proyecto y habre un cmd dentro de la ruta

Copia los siguietes comandos en el cmd y ejecutelos
```bash
git clone https://github.com/SantiagoCr8/Inventario-Service.git
cd Inventario-Service
mvn clean package -DskipTests
```
## Ejecucion
Cuando termine de ejecutar verifica que el servicio de Producto-Servise este funcionando y despues ejecute el siguiente comando para correr el servicio
```bash
java -jar target/inventario-service-0.0.1-SNAPSHOT.jar --spring.profiles.active=local
```

## Funcionamento

El servicio corre el puerto 8080 se crearon 3 enpoint para le microservicio

### Buscar inventario
Se encarga de traer el stock de un productio especifico

puedes ingresar con la siguiete URL http://localhost:8080/inventario/buscar/{id} y cambias el {id} por el id del producto que quieres verificar

### Actualizar inventario
Se encarga de actulizar el stock de un producto especifico

puedes ingresar con la siguiete URL http://localhost:8080/inventario/actualizar y se debe enviar un json con los siguientes atributos
```bash
    {
        "id":1,
        "cantidad":1000,
        "productId":1
    }
```

### Comprar producto
Es encargada de hacer comprar de produtos

puedes ingresar con la siguiete URL http://localhost:8080/inventario/comprar/crear y se debe enviar un json con los siguientes atributos
```bash
    {
        "id":1,
        "cantidad"2,
        "productId":1
    }
```

## Test
El microservio ya tiene pruebas unitarias 
## Excepciones 
EL microservio ya cuenta con un manejo de ejecpcion y son manejadas con condigos HTTP










