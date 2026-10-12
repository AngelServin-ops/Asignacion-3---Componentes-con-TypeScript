Parte A: Tabla Genérica
¿Por qué esta tabla se puede llamar «genérica»?
R: Porque es independiente de la información que procesa. Actúa de forma agnóstica, ya que solo necesita que le pases una configuración para las columnas (usando clave y titulo) y el conjunto de datos a dibujar, sin atarse a ningún modelo en específico.

¿Qué tendría que cambiar para mostrar alumnos en lugar de productos?
R: Solo necesitas modificar los datos que le inyectas desde afuera. Bastaría con actualizar la propiedad columnas (ej. [{clave: 'matricula', titulo: 'Matrícula'}, {clave: 'nombre', titulo: 'Alumno'}]) y el arreglo asignado a filas. No hay que tocar ni una sola línea del código fuente del componente.

Parte B: Componente <contador-cantidad>
Contrato del componente:

Lo que recibe (Entradas): Acepta las propiedades o atributos valor (el número inicial/actual), así como min y max (los topes mínimo y máximo).
Lo que comunica (Salidas): Dispara un evento personalizado en el DOM nombrado cambio-cantidad. Este evento envía el valor actualizado a través de su propiedad detail (en formato { cantidad: number }).
Lo que gestiona internamente (Estado): Controla y memoriza el valor numérico actual, vigilando que los incrementos y decrementos no sobrepasen los límites permitidos.