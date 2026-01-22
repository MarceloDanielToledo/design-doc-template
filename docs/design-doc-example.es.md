
# Sistema de Gestión de Stock

## Autores

- [@MarceloDanielToledo](https://github.com/MarceloDanielToledo)

## Contexto

Actualmente, la fábrica de productos enfrenta limitaciones significativas debido a su obsoleto sistema de gestión de stock. Este sistema no solo es rígido y difícil de adaptar, sino que también funciona únicamente en una versión antigua de Windows y no se integra bien con los procesos actuales de la fábrica. Estas deficiencias están causando ineficiencias en la gestión de inventario, como desabastecimientos frecuentes, exceso de inventario y visibilidad limitada del flujo de materiales, lo que impacta negativamente en las operaciones diarias y aumenta los costos.

Es necesario implementar un nuevo sistema de gestión de stock que aborde las necesidades actuales y futuras de la fábrica. Este sistema debe ser flexible y multiplataforma, accesible desde cualquier dispositivo con un navegador web. Proporcionará datos en tiempo real, integraciones fluidas con otros sistemas y la capacidad de personalizar funciones según las necesidades específicas de la fábrica, facilitando así una mejor toma de decisiones.

Este sistema beneficiará a los gerentes de producción, al personal del almacén y al equipo de compras al proporcionarles una herramienta más moderna y eficiente que apoyará el crecimiento y la evolución de la fábrica.

## Objetivos

- Mejorar la accesibilidad y flexibilidad: Facilitar el acceso al sistema desde cualquier dispositivo con un navegador web.

- Integrar con otros sistemas: Asegurar una sincronización fluida con el módulo de compras y otros sistemas existentes.

- Facilitar la toma de decisiones: Proporcionar informes y análisis predictivos para una mejor planificación.

- Optimizar métricas de gestión: Mejorar los tiempos de respuesta y la eficiencia operativa en la gestión de inventario.

## No Objetivos

- No se desarrollarán funcionalidades fuera del alcance de la gestión de stock.

- El sistema no abordará la actualización o reemplazo del hardware existente en la fábrica, centrándose únicamente en el software de gestión de stock.

- No se crearán características adicionales no relacionadas con la gestión de stock, como nuevas funcionalidades para otros departamentos o procesos no definidos en el alcance.

- La capacitación se limitará a la formación básica de usuarios para el nuevo sistema; no se incluirán programas de capacitación extensos ni soporte para otros procesos comerciales.

## Hitos

**Definición de Requisitos** - 30/08/24

- Reunión para definir y acordar los requisitos del sistema con el cliente.

**Diseño y Prototipo** - 15/09/24

- Presentación del diseño inicial y prototipo para obtener comentarios del cliente.

**Desarrollo de Funcionalidades Clave** - 15/10/24

- Entrega de las funcionalidades principales del sistema.

**Integración y Pruebas** - 15/11/24

- Integración del sistema con otros módulos y pruebas. Reunión para revisar los resultados con el cliente.

**Despliegue y Capacitación** - 01/12/24

- Implementación del sistema y capacitación básica de usuarios.

**Revisión Final y Ajustes** - 15/12/24

- Revisión final con el cliente para realizar ajustes basados en los comentarios.


## Solución Existente

La fábrica utiliza actualmente un sistema de gestión de stock desarrollado en FoxPro. Este sistema obsoleto es limitado en términos de funcionalidad y flexibilidad, lo que dificulta su adaptación a las necesidades modernas de la fábrica. Los usuarios interactúan con el sistema a través de una interfaz gráfica que permite operaciones básicas como registrar entradas y salidas de inventario, generar informes y ver el estado del stock.

Sin embargo, el sistema tiene varias deficiencias, incluyendo una integración limitada con otros procesos de la fábrica, falta de soporte para actualizaciones y personalizaciones, y problemas de compatibilidad con versiones más nuevas del sistema operativo. Esta situación ha llevado a una gestión de inventario ineficiente y a una necesidad creciente de una solución más moderna y adaptable.


## Solución Propuesta

La solución propuesta para el nuevo sistema de gestión de stock es una aplicación web basada en Blazor WebAssembly. Esta elección permite una plataforma moderna y flexible, accesible desde cualquier dispositivo con un navegador web.

### Descripción General

El sistema será una aplicación Blazor WebAssembly utilizando SignalR. Esto permite una experiencia de usuario rica y dinámica con una interfaz moderna que facilita la gestión de inventario en tiempo real. La aplicación se conectará a una API backend para manejar todas las operaciones relacionadas con los datos de inventario.

### Arquitectura del Sistema

- **Interfaz de Usuario (UI)**: La aplicación web se desarrollará utilizando Blazor WebAssembly, permitiendo una interfaz fluida y receptiva. Los usuarios podrán acceder al sistema desde cualquier dispositivo con un navegador, ya sea en una computadora de escritorio, tableta o teléfono móvil.

- **API Backend**: La aplicación se conectará a una API RESTful que manejará todas las operaciones del sistema, incluyendo la gestión de inventario, generación de informes y sincronización con otros módulos de la fábrica. Esta API se construirá con .NET, proporcionando robustez y escalabilidad.

- **Base de Datos**: La información del inventario se almacenará en una base de datos centralizada, permitiendo consultas eficientes y almacenamiento seguro de datos. La base de datos se diseñará para integrarse fácilmente con la API y soportar las operaciones del sistema.

- **Autenticación y Seguridad**: La aplicación incluirá mecanismos de autenticación y autorización para asegurar que solo los usuarios autorizados puedan acceder y modificar los datos de inventario. Se implementarán medidas de seguridad para proteger la integridad y confidencialidad de los datos.


### Flujo de Trabajo

- **Inicio de Sesión**: Los usuarios acceden al sistema a través de una página de inicio de sesión segura. Una vez autenticados, son dirigidos a la página principal donde pueden ver y gestionar el inventario.
- **Gestión de Inventario**: Los usuarios pueden registrar nuevas entradas y salidas de inventario, ajustar niveles de stock y generar informes. La interfaz proporcionará una vista clara y actualizada de los niveles de inventario y alertas sobre posibles problemas.
- **Generación de Informes**: El sistema permitirá la generación de informes detallados sobre el estado del inventario, incluyendo historial de movimientos y análisis de tendencias. Los informes se pueden exportar en varios formatos para su revisión y análisis.
- **Sincronización con Otros Sistemas**: La aplicación se integrará con otros módulos de la fábrica, como el sistema de compras, para asegurar que los datos de inventario estén siempre actualizados y sincronizados.


## Soluciones Alternativas

### Solución de Terceros

Consideramos la opción de adquirir un sistema de gestión de stock de un proveedor externo. Estas soluciones suelen ofrecer funcionalidades avanzadas y soporte continuo. Ejemplos incluyen sistemas como SAP Business One o NetSuite.

**Pros**:

- Implementación más rápida debido a la disponibilidad inmediata del software.
- Soporte continuo y actualizaciones proporcionadas por el proveedor.
- Funcionalidades probadas y confiables.

**Contras**:

- Alto costo por licencias y suscripción.
- Menos flexibilidad para personalizar según las necesidades específicas de la fábrica.
- Puede requerir una integración compleja con los sistemas existentes.


### Solución de Código Abierto

Evaluamos el uso de soluciones de gestión de inventario de código abierto, como Odoo o ERPNext. Estas plataformas ofrecen una base robusta que se puede adaptar y extender según las necesidades.

**Pros**:

- Costos iniciales reducidos o nulos.
- Flexibilidad para personalizar y adaptar el software.
- Comunidad activa que puede proporcionar soporte y mejoras.

**Contras**:

- Requiere conocimientos técnicos para la personalización y mantenimiento.
- Soporte limitado en comparación con soluciones comerciales.
- Posible necesidad de desarrollo adicional para integrar con otros sistemas.

### Desarrollo Interno

Desarrollar una solución interna personalizada, como la propuesta de aplicación Blazor WebAssembly, adaptada a las necesidades específicas de la fábrica.

**Pros**:

- Alineación completa con los requisitos y procesos de la fábrica.
- Flexibilidad para modificar y escalar el sistema según sea necesario.
- Control total sobre el diseño y las funcionalidades.

**Contras**:

- Mayor tiempo de desarrollo.
- Requiere recursos internos para el desarrollo y mantenimiento.
- Mayor inversión inicial en comparación con soluciones preexistentes.


## Pruebas, Monitoreo y Alertas

**Pruebas**

La solución se someterá a pruebas unitarias, de integración y de extremo a extremo (E2E) para asegurar su correcto funcionamiento antes del despliegue. Esto incluirá pruebas de usabilidad para verificar que los usuarios puedan interactuar con el sistema sin problemas, y pruebas de integración para asegurar que todas las funciones operen correctamente con otros sistemas. También se realizarán pruebas de rendimiento para asegurar que el sistema maneje el volumen de datos esperado sin retrasos.

**Monitoreo**

Una vez implementado, el sistema será monitoreado continuamente para asegurar estabilidad y rendimiento. Se utilizarán herramientas de monitoreo para supervisar el estado del sistema, el uso de recursos y los tiempos de respuesta. Esto ayudará a detectar y resolver problemas antes de que afecten a los usuarios.

**Alertas**

Se configurarán alertas automáticas para notificar al equipo de soporte sobre cualquier anomalía o falla en el sistema, como problemas de rendimiento, errores críticos o interrupciones del sistema. Las alertas ayudarán a responder rápidamente a cualquier incidente y minimizar el impacto en las operaciones de la fábrica.


## Impacto en Otros Equipos

**Impacto en Soporte y Operaciones:**
El nuevo sistema requerirá más atención del equipo de operaciones inicialmente, ya que será crucial asegurar que todo funcione correctamente durante la transición. Sin embargo, una vez que el sistema esté en funcionamiento, el número de problemas debería ser menor en comparación con el sistema antiguo.

**Costo:**
Crear e implementar el nuevo sistema incurrirá en costos, especialmente inicialmente. Sin embargo, a largo plazo, debería ahorrar dinero porque será más fácil de administrar y mantendrá el inventario mejor controlado.

**Velocidad del Sistema:**
Como aplicación web, el nuevo sistema podría funcionar un poco más lento en áreas con mala conectividad a internet. Aún así, está diseñado para asegurar que esta diferencia no sea muy notable.

**Seguridad:**
Al ser una aplicación web, puede estar expuesta a nuevos riesgos de seguridad, como intentos de acceso no autorizado. Por lo tanto, se tomarán medidas para asegurar la protección de datos y que solo el personal autorizado pueda acceder a ellos.

**Posibles Inconvenientes:**
Los usuarios pueden necesitar tiempo para acostumbrarse al nuevo sistema, lo que podría causar algunas molestias iniciales. Además, durante la transición, podrían surgir algunos problemas temporales en las operaciones si no se planifican adecuadamente.

**Comunicación con Clientes:**
El equipo de soporte necesitará explicar claramente a los clientes por qué se está realizando el cambio y cómo les beneficiará. También será importante proporcionar asistencia y capacitación para hacer que la transición sea lo más suave posible.


## Preguntas Abiertas

**Integración con Sistemas Existentes**

¿Qué nivel de compatibilidad se requiere con los sistemas actuales de la fábrica? ¿Deberíamos considerar una migración completa o una integración gradual?

**Capacitación de Usuarios**

¿Cuál es la mejor manera de capacitar a los usuarios en el nuevo sistema? ¿Son suficientes los tutoriales en línea o será necesaria una capacitación presencial?

**Escalabilidad Futura**

¿Cómo deberíamos planificar la escalabilidad del sistema para futuras expansiones de la fábrica? ¿Hay áreas críticas que requieran más atención desde el principio?

**Opciones de Personalización**

¿Hasta qué punto debe ser personalizable el sistema para adaptarse a los cambios en los procesos de la fábrica? ¿Es mejor ofrecer un conjunto básico de opciones o permitir una personalización más extensa?

**Gestión de Datos Históricos**

¿Cómo manejaremos la transición de datos históricos del sistema antiguo al nuevo? ¿Es necesario importar todos los datos o solo los relevantes para las operaciones actuales?


## Alcance Detallado y Cronograma

### Alcance Detallado:

**Fase 1: Análisis de Requisitos y Planificación (Fecha: 1ra semana)**

- Reuniones con las partes interesadas para definir requisitos específicos del sistema.
- Preparación del documento final de requisitos.

**Fase 2: Diseño del Sistema (Fecha: 2da-3ra semana)**

- Diseño de la arquitectura del sistema, incluyendo flujos de datos y estructura de la base de datos.
- Creación de maquetas para la interfaz de usuario.

**Fase 3: Desarrollo Inicial (Fecha: 4ta-8ta semana)**

- Implementación de la estructura básica del sistema.
- Desarrollo de funcionalidades críticas, como gestión de inventario y seguimiento de stock.

**Fase 4: Integración y Pruebas (Fecha: 9na-11va semana)**

- Integración con sistemas existentes.
- Realización de pruebas unitarias y de integración para asegurar la calidad del sistema.

**Fase 5: Implementación Piloto (Fecha: 12va semana)**

- Despliegue inicial en un entorno controlado.
- Recolección de comentarios y ajustes basados en la experiencia del usuario.

**Fase 6: Despliegue Completo y Capacitación (Fecha: 13va-14va semana)**

- Despliegue del sistema en toda la fábrica.
- Capacitación de usuarios finales para asegurar una transición fluida.
