<h1 align="center">Pool de Conexiones</h1>
<p>Técnica utilizada en el desarrollo de software para mejorar el rendimiento y la eficiencia de las aplicaciones que interactúan con bases de datos u otros recursos que requieren conexiones establecidas.</p>
<p>En lugar de abrir y cerrar una nueva conexión cada vez que se necesita interactuar con la base de datos, el <b>pool de conexiones</b> mantiene un conjunto (o <b>"pool"</b>) de conexiones preestablecidas disponibles para su uso. Cuando una aplicación necesita conectarse a la base de datos, en lugar de crear una nueva conexión desde cero, toma una conexión del pool disponible. Una vez que la aplicación ha terminado de usar esa conexión, la devuelve al pool en lugar de cerrarla.</p>
<p>Esto tiene varias ventajas:</p>

-    <b>Mejora el rendimiento</b>: Abrir y cerrar conexiones es una operación costosa en términos de recursos de red y tiempo de CPU. Al reutilizar las conexiones existentes en el pool, se reduce la sobrecarga de abrir y cerrar conexiones, lo que mejora el rendimiento general de la aplicación.
-    <b>Optimiza el uso de recursos</b>: Limitar el número de conexiones abiertas simultáneamente ayuda a evitar la saturación de recursos del sistema. Esto es especialmente útil en entornos donde el número de conexiones permitidas a la base de datos es limitado.
-    <b>Escalabilidad</b>: Un pool de conexiones puede gestionar dinámicamente el tamaño del pool según la carga de trabajo de la aplicación. Por ejemplo, puede aumentar el número de conexiones disponibles durante períodos de alta demanda y reducirlo cuando la demanda disminuye, lo que permite una mejor escalabilidad de la aplicación.
