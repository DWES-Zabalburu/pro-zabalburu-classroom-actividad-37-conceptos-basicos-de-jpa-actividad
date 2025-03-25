## Instrucciones

Nos piden crear una aplicación para gestionar un sistema de noticias en la empresa mediante JPA. De cada Noticia se debe guardar la siguiente información:
 

- `id`: Debe ser autogenerado por el sistema y además ser el campo clave de la tabla correspondiente

- `titular` : Obligatorio y único (VARCHAR2 de 120)

- `fecha` : Obligatoria

- `sinopsis` : Una descripción de la noticia

- `URL` : La URL de la noticia si la hay

 
Se pide:

- Configurar la aplicacion para que use JPA (con la opción de actualizar automáticamente la estructura de la BBDD) y almacene la información en la tabla `noti` de la BBDD.

- Diseñar una aplicación con un menú con las siguientes opciones:

 
                   Gestión de Noticias
                   1. Nueva Noticia
                   2. Quitar Noticia
                   3. Buscar Noticias
                   4. Ver Todas las Noticias
                   5. Salir
                   Opción [1-5]:
 

### Nueva Noticia

- Se pedirá el `titular`, la `fecha` (dd/mm/aaaa), la `sinopsis` y la `URL` de la noticia y se creará una entidad `Noticia` con dicha información.

- La cadena de fecha se intentará convertir en una fecha mediante un `DateFormat` de formato corto (`parse`)

- Si hay errores, se asignará la fecha del día

- Se persistirá la noticia en la BBDD

- Se preguntará al usuario si quiere introducir otra noticia

 

### Quitar Noticia

- Se pedirá el `título` de la noticia y se buscará en la BBDD

- Si la **noticia no existe**, se dará un mensaje de **error**

- Si existe
  
  - Se mostrarán el resto de los campos de la noticia para pedir confirmación al usuario para su eliminación
  
  - Si confirma se eliminará la noticia

 

### Buscar Noticias

- Se pedirá el texto a buscar y se **buscarán todas las noticias que incluyan dicho texto en su `título`** (podéis usar el operador `Like` exactamente igual que en Oracle)

- Si hay alguna noticia se mostrarán en una tabla en un `JOptionPane`

- Si no la hay, se dará un mensaje indicándolas

 

### Ver todas las Noticias

- Se mostrarán todas las noticias **ordenadas en descendente** por `fecha`.




