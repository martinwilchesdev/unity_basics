# Unity

## Templates

Pemiten iniciar un tipo de juego con el editor configurado para el juego que se quiera crear.

## Editor

- Assets :: Recursos del juego (scripts, texturas, archivos de audio)
- Packages :: Paquetes integrados en el proyecto
- ProjectSettings :: Configuraciones de las distintas partes del proyecto (fisicas, capas, etiquetas y configuraciones de tiempo)

### GameObjects

- Son la parte mas basica de un juego
- Necesitan que se le añadan componentes, con las funciones que se vayan a realizar.
- El componente **transform** es el unico que esta presente en todos los GameObjects, ya que por defecto define la posicion y la orientacion del GameObject en la escena.
- Los componentes de los GameObjects son scripts

### Escena

- Area de contenido del juego
- La escena ya incluye por defecto el GameObject camara, el cual permite visualiza la escena
- La escena varia si el juego es en 2D o en 3D.
    - Camara ortografica: 2D
    - Camara perspectiva: 3D

> Escena -> GameObjects -> Componentes

### Distribución del editor

#### Project

Gestiona los assets y los packages del proyecto.

#### Hierarchy

Muestra las instancias de la escena actual.

#### Inspector

Muestra la informacion detallada de los objetos del juego

#### Escena

Representacion visual del mundo

#### Vista de juego (Game)

Representa la vista del juego por parte del usuario

## Sprites

Los sprites son imagenes de 2 dimensiones que se incluyen en el juego.

### Bitmap

Representacion de una imagen en la tarjeta grafica. Contiene todos los pixeles que definen una imagen con un ancho y un alto determinados.

Cada pixel de la imagen es pintado de un color y dependiendo de los bits cada pixel se puede pintar de distintos colores.
- Si es de un bit, solo podra pintarse de blanco o negro
- Si es de 4 bits de 16 colores

> Las imagenes se denominan texturas.

### Filter Mode

- Bilinear: Se añade un sombreado a la textura para mejorar su visualizacion.
- Point: Se muestran los pixeles de la textura.

#### Sprite Mode

- Single: La imagen cargada contiene una unica textura.
- Multiple: La imagen cargada contiene multiples texturas.

Cuando se cargan imagenes que contienen multiples texturas, se realiza una unica carga en memoria de dicha imagen, posteriormente desde el sprite editor es posible:
- Dividir la imagen en las multiples texturas que contiene.
- Asignar el valor del pivote y de pixeles por unidad para cada textura expecifica.

#### Sprite renderer

Componente que permite visualizar el GameObject en la escena.

- Draw mode: La opcion `Tiled` permite que un sprite sea ubicado en una grilla.
    - Size: Tamaño del sprite repetido en la escena.
    - Tile Mode
