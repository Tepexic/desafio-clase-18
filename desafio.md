# Desafío CRUD MongoDB
## Consigna: 
Utilizando Mongo Shell, crear una base de datos llamada ecommerce que contenga dos colecciones: mensajes y productos.

```
mongo
show dbs
use ecommerce
db.createCollection('messages')
db.createCollection('products')
```

1) Agregar 10 documentos con valores distintos a las colecciones mensajes y productos. El formato de los documentos debe estar en correspondencia con el que venimos utilizando en el entregable con base de datos MariaDB.
  ```
  db.messages.insertMany([
    {
      account: "juan@tienda.com",
      timestamp: "10/24/2021, 3:03:04 PM",
      text: "¡Hola! ¿Que tal?",
    },
    {
      account: "pedro@tienda.com",
      timestamp: "10/24/2021, 3:04:04 PM",
      text: "Muy bien! Y tu?",
    },
    {
      account: "ana@tienda2.com",
      timestamp: "10/24/2021, 3:05:04 PM",
      text: "alguien tiene el precio del aguacate?",
    },
    {
      account: "pedro@tienda.com",
      timestamp: "10/24/2021, 3:05:20 PM",
      text: "Juan es el bueno para frutas y verduras",
    },
    {
      account: "ana@tienda2.com",
      timestamp: "10/24/2021, 3:05:40 PM",
      text: "Juan, me ayudas con el precio? no lo tenemos registrado",
    },
    {
      account: "juan@tienda.com",
      timestamp: "10/24/2021, 3:06:04 PM",
      text: "40 el kilo de Hass",
    },
    {
      account: "juan@tienda.com",
      timestamp: "10/24/2021, 3:06:10 PM",
      text: "10 si lo quieren por pieza",
    },
    {
      account: "ana@tienda2.com",
      timestamp: "10/24/2021, 3:06:20 PM",
      text: "gracias! ya lo doy de alta en el sistema",
    },
    {
      account: "juan@tienda.com",
      timestamp: "10/24/2021, 3:06:30 PM",
      text: "dale, me avisas si necesitas algo mas",
    },
    {
      account: "pedro@tienda.com",
      timestamp: "10/24/2021, 3:07:00 PM",
      text: "Juan, llamame a la extension 8080 por favor",
    },
  ])
  ```

  ```
  db.products.insertMany([
    {
      title: "Cinta de reparación de pantalla de 5x200CM",
      description: "Cinta de reparación de pantalla  para mosquitero metalica de 5x200CM",
      code: 1234567890,
      price: 4922,
      thumbnail: "https://ae01.alicdn.com/kf/H1b13e3760cc74dcd9b7e161256820bbdT/Cinta-de-reparaci-n-de-pantalla-de-5x200CM-parche-autoadhesivo-para-puerta-y-ventana-s-per.jpeg_Q90.jpeg_.webp",
    },
    {
      title: "Interruptor Outemu de 3 pines",
      description: "Interruptor para teclado mecánico, interruptores táctiles y silenciosos, RGB LED SMD, color azul y marrón, Compatible con interruptor MX",
      code: 1234567891,
      price: 3886,
      thumbnail: "https://ae01.alicdn.com/kf/H9013370bd7e64d24983d6cea7fbb4724y/Interruptor-Outemu-de-3-pines-para-teclado-mec-nico-interruptores-t-ctiles-y-silenciosos-RGB-LED.jpg_640x640.jpg",
    },
    {
      title: "Cable de Teclado mecánico personalizado de 1,7 m",
      description: "Cable de Teclado mecánico personalizado azul de 1,7 m",
      code: 1234567892,
      price: 4500,
      thumbnail: "https://ae01.alicdn.com/kf/H777100f369944bb7b003618ae4143030b/Teclado-mec-nico-personalizado-de-1-7-m-cable-usb-c-resorte-en-espiral-mini-interfaz.jpg_Q90.jpg_.webp",
    },
    {
      title: "Cuentas de plata",
      description: "Cuentas de plata para pulsera",
      code: 1234567893,
      price: 3312,
      thumbnail: "https://ae01.alicdn.com/kf/H4a11282f49f049218e6f7a69e31290c2e/Bamoer-Cuentas-de-mu-eco-de-nieve-de-Plata-de-Ley-925-dijes-de-rbol-de.jpg_Q90.jpg_.webp",
    },
    {
      title: "Tira de Luces LED RGB 2835",
      description: "DC5V, 1M, 2M, 3M, 4M, 5M, Cinta Flexible de Diodo, Cable USB, 3 Teclas, Control, Iluminación de Fondo de TV, Pantalla Escritorio",
      code: 1234567894,
      price: 124,
      thumbnail: "https://ae01.alicdn.com/kf/H6a25b775287748008e9d2385c2a382b0u/Tira-de-Luces-LED-RGB-2835-DC5V-1M-2M-3M-4M-5M-Cinta-Flexible-de-Diodo.jpg_Q90.jpg_.webp",
    },
    {
      title: "Cortadora de pelo inalámbrica",
      description: "Cortadora de pelo inalámbrica para hombre, máquina de afeitar eléctrica inalámbrica, para Barbero",
      code: 1234567895,
      price: 1720,
      thumbnail: "https://ae01.alicdn.com/kf/Haa9becf1407741a1b3a270e1ae24d2c9c/Cortadora-de-pelo-inal-mbrica-para-hombre-m-quina-de-afeitar-el-ctrica-inal-mbrica-para.jpg_Q90.jpg_.webp",
    },
    {
      title: "Gafas de ordenador transparentes para hombre y mujer",
      description: "DLIDW2021-Gafas de ordenador transparentes para hombre y mujer, lentes redondas con bloqueo de luz azul, lentes ópticas",
      code: 1234567896,
      price: 210,
      thumbnail: "https://ae01.alicdn.com/kf/H99a721f3ed044aef8d3406b76227eebd3/DLIDW2021-Gafas-de-ordenador-transparentes-para-hombre-y-mujer-lentes-redondas-con-bloqueo-de-luz-azul.jpg_Q90.jpg_.webp",
    },
    {
      title: "Soporte Flexible ajustable para teléfono móvil",
      description: "Soporte Flexible ajustable para teléfono móvil, base de montaje de escritorio para cama, hogar, Smartphone",
      code: 1234567897,
      price: 543,
      thumbnail: "https://ae01.alicdn.com/kf/Hbe996a6a5cbc468da6ca7293e7bfd904t/Soporte-Flexible-ajustable-para-tel-fono-m-vil-base-de-montaje-de-escritorio-para-cama-hogar.jpg_Q90.jpg_.webp",
    },
    {
      title: "Auriculares inalámbricos con Bluetooth",
      description: "Auriculares inalámbricos con Bluetooth 5.0 para deporte, dispositivo de audio con caja de carga, a prueba de agua, con control del volumen, mini TWS, manos libres",
      code: 1234567898,
      price: 4477,
      thumbnail: "https://ae01.alicdn.com/kf/H95aaa054e4e347d189434fe02d881f70W/Auriculares-inal-mbricos-con-Bluetooth-5-0-para-deporte-dispositivo-de-audio-con-caja-de-carga.jpg_Q90.jpg_.webp",
    },
    {
      title: "Tarjeta Micro SD TF",
      description: "Tarjeta Micro SD TF para adaptador de teléfono inteligente, 8, 16, 32, 64, 128 GB",
      code: 1234567899,
      price: 650,
      thumbnail: "https://ae01.alicdn.com/kf/H397f29965dbe4e4a81abd6835e1fce3cS/Tarjeta-Micro-SD-TF-para-adaptador-de-tel-fono-inteligente-8-16-32-64-128-256.jpg_Q90.jpg_.webp",
    },
  ])
  ```

2) Definir las claves de los documentos en relación a los campos de las tablas de esa base. En el caso de los productos, poner valores al campo precio entre los 100 y 5000 pesos(eligiendo valores intermedios, ej: 120, 580, 900, 1280, 1700, 2300, 2860, 3350, 4320, 4990). 

3) Listar todos los documentos en cada colección.
```
db.messages.find().pretty()
db.products.find().pretty()
```

4) Mostrar la cantidad de documentos almacenados en cada una de ellas.
```
db.messages.count()
db.products.count()
```

5) Realizar un CRUD sobre la colección de productos:

    a) Agregar un producto más en la colección de productos 
  ```
    db.products.insertOne({
      title: "Ratón inalámbrico ergonómico",
      description: "Ratón inalámbrico ergonómico para ordenador, periférico óptico con receptor USB, 3 botones, 2,4 Ghz, 1600 DPI, para portátil",
      code: 1234567900,
      price: 450,
      thumbnail: "https://ae01.alicdn.com/kf/H68fc1076b65b4172ad8c622a82df07bff/Rat-n-inal-mbrico-ergon-mico-para-ordenador-perif-rico-ptico-con-receptor-USB-3-botones.jpg_Q90.jpg_.webp"
    })
  ```

    b) Realizar una consulta por nombre de producto específico:
        i) Listar los productos con precio menor a 1000 pesos.
  ```
        db.products.find({price: {$lt: 1000}}).pretty()
  ```

        ii) Listar los productos con precio entre los 1000 a 3000 pesos.
  ```
        db.products.find({$and: [{price: {$gt: 1000}}, {price: {$lt: 3000}}]}).pretty()
  ```

        iii) Listar los productos con precio mayor a 3000 pesos.
  ```
        db.products.find({price: {$gt: 3000}}).pretty()
  ```

        iv) Realizar una consulta que traiga sólo el nombre del tercer producto más barato.
  ```
        db.products.find({}, {title: true}).sort({price: 1}).skip(2).limit(1)
  ```

    c) Hacer una actualización sobre todos los productos, agregando el campo stock a todos ellos con un valor de 100.
  ```
    db.products.updateMany({}, {$set: {stock: 100}})
  ```

    d) Cambiar el stock a cero de los productos con precios mayores a 4000 pesos. 
  ```
    db.products.updateMany({price: {$gt: 4000}}, {$set: {stock: 0}})
  ```
    
    e) Borrar los productos con precio menor a 1000 pesos 
  ```
    db.products.deleteMany({price: {$lt: 1000}})
  ```

6) Crear un usuario 'pepe' clave: 'asd456' que sólo pueda leer la base de datos ecommerce. Verificar que pepe no pueda cambiar la información.
```
db.createUser({
  user: "pepe",
  pwd:  "asd456",
  roles: [
    {
      role: "read",
      db: "ecommerce"
    }
  ]
})
```
NOTA: para poder acceder a la base de datos con ese usuario, tuve que hacer:
```
mongo -u pepe -p asd456 --authenticationDatabase ecommerce
```