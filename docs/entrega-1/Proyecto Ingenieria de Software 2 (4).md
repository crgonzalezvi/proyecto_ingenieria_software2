<div align="center">

# Primera Entrega de Proyecto
## Ingeniería de Software II

---

**Presentado a:**
[Jose Albeiro Montes Gil](mailto:joamontesgi@unal.edu.co)

**Presentado por:**
[Cristian Camilo Gonzalez Villa](mailto:crgonzalezvi@unal.edu.co)
Miguel Ángel Ocampo Loaiza

**Universidad Nacional de Colombia**
Facultad de Administración
Departamento de Informática y Computación
Manizales, Caldas

*28 de septiembre de 2026*

</div>

**Sistemas elegidos**

**1\. SAP Business One:** ERP diseñado para pequeñas y medianas empresas (PyMEs) cuyo propósito es centralizar y gestionar las operaciones clave del negocio en una sola plataforma.

Cuentan entre su apartado con las siguientes características principales:

* Finanzas y Contabilidad: Control de flujo de caja, presupuestos y conciliaciones.  
* Ventas y CRM: Gestión de oportunidades, clientes y ciclo de venta.  
* Compras e Inventario: Control de stock, proveedores y trazabilidad de productos.  
* Producción y MRP: Planificación de requerimientos de material y órdenes de fabricación.  
* Cumplimiento Fiscal: Adaptación a la facturación electrónica y normativa local.  
* Analítica e Informes: Dashboards interactivos y reportes en tiempo real.  
* Acceso: Aplicación móvil, versión web y de escritorio (Nube u on-premise).  
* Integración de herramientas propias de SAP como lo es SAP HANA para acelerar operaciones con una base de datos de alto rendimiento.

**Especificaciones técnicas:** 

Se basa en un módelo clásico de tres capas las cuales son:

- **Capa de presentación:** Es la interfaz de usuario (la aplicación de escritorio instalada o sus adaptaciones en la web y móviles).  
- **Capa lógica de negocio:** Servidor centralizado que procesa todas las reglas del negocio, transacciones y peticiones de forma unificada.  
- **Capa de Base de Datos:** Utiliza un motor de base de datos relacional centralizado. Toda la información de finanzas, inventarios, compras y ventas se aloja y se procesa dentro de una misma instancia de base de datos bajo el mismo esquema relacional.

En el sitio web oficial de SAP observamos un sistema que se vende como un sistema modular muy completo, aunque podemos deducir que en realidad es un monolito robusto. Esto lo podemos deducir porque aunque sus módulos parecen separados (inventarios, ventas, contabilidad, etc)  por dentro todo vive y funciona conectado a la misma base de datos y al mismo servidor. Si se necesita actualizar el sistema, hay que actualizar el bloque completo, y si por alguna razón el servidor se satura o se cae, se detiene toda la operación de la empresa.

**2\. Siigo:** Software contable y administrativo en la nube diseñado para micro, pequeñas y medianas empresas (PyMEs) y contadores, enfocado en la automatización operativa y el cumplimiento fiscal. 

Cuentan entre su apartado con las siguientes características principales:

* **Contabilidad Automatizada:** Generación de estados financieros, libros auxiliares y cálculo de impuestos en tiempo real a partir de las ventas y compras.  
* **Control de Inventarios:** Seguimiento de stock, costeo de productos, kardex y alertas de reabastecimiento.  
* **Punto de Venta (POS):** Módulo para tiendas físicas sincronizado en vivo con la contabilidad y el inventario central.  
* **Gestión de Cartera y Proveedores:** Control de cuentas por cobrar, alertas de facturas vencidas y gestión de pagos.  
* **Reportes y Flujo de Caja:** Dashboards para monitorear ventas, egresos y rentabilidad del negocio de forma sencilla.  
* **Plataforma 100% Nube:** Acceso multiusuario desde navegador o app móvil, sin requerir infraestructura física ni servidores.  
* **Agente IA:** Resuelve consultas contables, tributarias, laborales y financieras.

**Especificaciones técnicas:** Funciona bajo un modelo de software como servicio (SaaS) en la nube, en el cual la infraestructura tecnológica es administrada por el proveedor y los usuarios acceden a la plataforma mediante Internet. Desde el punto de vista funcional, el sistema integra diferentes módulos para gestionar procesos como contabilidad, facturación, inventarios, cartera y punto de venta.

* **Capa de Cliente / Interfaz:** El usuario accede a la plataforma principalmente mediante un navegador web y aplicaciones móviles, sin necesidad de instalar o administrar localmente la infraestructura que soporta el sistema. La interfaz permite interactuar con los diferentes módulos y consultar la información empresarial.  
* **Capa de Lógica de Negocio:** Las operaciones realizadas por los usuarios son procesadas por los servicios de aplicación administrados por Siigo en su infraestructura cloud. En esta capa se ejecutan las reglas de negocio y los procesos relacionados con facturación, contabilidad, inventarios, cartera y demás funcionalidades de la plataforma.  
* **Capa de Datos**: La información generada por los usuarios, como facturas, movimientos de inventario, registros contables y datos financieros, es almacenada y administrada en la infraestructura tecnológica del proveedor. El usuario no administra directamente las bases de datos ni la infraestructura de almacenamiento.

Desde la perspectiva del usuario, Siigo presenta una plataforma centralizada e integrada, ya que los diferentes módulos son proporcionados y administrados por un mismo proveedor y se accede a ellos desde un entorno común. Sin embargo, no es posible afirmar con certeza que su arquitectura interna sea monolítica, debido a que Siigo no publica información técnica suficiente que permita determinar si internamente utiliza un monolito, microservicios o una arquitectura híbrida.

Del mismo modo, el hecho de que Siigo sea una plataforma SaaS administrada centralmente no significa que toda la infraestructura dependa de un único servidor. Al estar implementada en la nube, podría utilizar mecanismos como redundancia, balanceo de carga, replicación y otros recursos destinados a garantizar la disponibilidad y escalabilidad del servicio. Por lo tanto, las características específicas de su arquitectura interna, distribución de servicios y mecanismos de tolerancia a fallos no pueden determinarse únicamente a partir de la información pública disponible.

**Odoo**: Sistema ERP modular de código abierto diseñado para PyMEs y empresas en crecimiento, que permite integrar e interconectar todas las áreas del negocio según sus necesidades.

Características clave:

* Arquitectura Modular: Posibilidad de implementar solo las aplicaciones necesarias (ej. Inventario, Facturación) e ir agregando módulos a medida que la empresa escala.  
* Inventario Avanzado: Control multialmacén con sistema de doble entrada, trazabilidad por lotes/series, escaneo de código de barras y rutas automáticas (Drop-shipping y Cross-docking).  
* Integración de Ventas y E-commerce: Sincronización nativa entre la tienda en línea integrada, Punto de Venta (POS) en tiendas físicas y gestión de presupuestos.  
* Contabilidad y Facturación: Automatización de asientos contables a partir de las compras y ventas, con soporte para facturación electrónica en diversos países.  
* Producción y Compras (MRP): Gestión de listas de materiales, órdenes de trabajo y reglas automáticas de reabastecimiento de stock.  
* Modelo y Acceso: Versiones Community (código abierto) y Enterprise (nube/de pago), con acceso 100% web y desde aplicación móvil.

**Especificaciones técnicas:** Odoo funciona como una plataforma modular desarrollada principalmente en Python y utiliza PostgreSQL para almacenar la información. Su principal característica es que las diferentes aplicaciones del sistema, como Inventario, Ventas, Contabilidad y Compras, pueden instalarse según las necesidades de cada empresa, pero todas hacen parte de la misma plataforma.

* **Capa de Presentación / Cliente:** Los usuarios pueden acceder a Odoo principalmente mediante un navegador web. También cuenta con opciones para utilizar algunas de sus funciones desde dispositivos móviles. Desde esta interfaz, los usuarios pueden consultar y gestionar la información de las diferentes aplicaciones.  
* **Capa de Lógica de Negocio:** En esta parte se encuentran las funciones que permiten realizar las diferentes operaciones del sistema. Los módulos de Odoo se encargan de procesos como ventas, inventarios, compras, contabilidad y producción, pero todos funcionan dentro de la misma plataforma de Odoo.  
* **Capa de Base de Datos:** Odoo utiliza PostgreSQL para almacenar la información. Los diferentes módulos comparten los datos almacenados, lo que permite que, por ejemplo, una venta pueda actualizar el inventario y generar la información correspondiente para contabilidad.

Una de las principales ventajas de Odoo es que su código fuente es público en su edición Community, por lo que es posible revisar cómo está construido el sistema. Al analizar su estructura, se puede identificar como un monolito modular, ya que sus diferentes aplicaciones funcionan como módulos dentro de una misma plataforma, en lugar de ser sistemas completamente independientes.

Esta característica permite que las diferentes áreas de la empresa estén muy conectadas entre sí y que la información pueda compartirse fácilmente entre los módulos. Sin embargo, también significa que existe una mayor dependencia entre las diferentes partes del sistema en comparación con una arquitectura basada completamente en servicios independientes.

Es importante aclarar que decir que Odoo es un sistema monolítico no significa que necesariamente funcione en un único servidor físico. Una empresa puede implementar Odoo utilizando diferentes servidores y recursos para mejorar su funcionamiento. El término monolito modular se refiere principalmente a la forma en que están organizadas e integradas las aplicaciones dentro del sistema.

**Comparación entre los 3 sistemas**

Se plantea hacer una comparación desde diferentes puntos que consideramos que con importantes a la hora de usar sistemas de este tipo, los puntos son:

- Perfil de empresa  
- Forma de adquirir el sistema  
- Poder del manejo de inventarios (nuestro interés principal)  
- Personalización  
- Facilidad de uso  
- Arquitectura

| Criterio | SAP Business One | Siigo | Odoo |
| :---- | :---- | :---- | :---- |
| Perfil de Empresa | Está dirigido principalmente a pequeñas y medianas empresas que necesitan manejar diferentes áreas del negocio en un solo sistema. | Está dirigido principalmente a micro, pequeñas y medianas empresas, emprendedores y contadores. | Está dirigido a pequeñas y medianas empresas y también a empresas que necesitan ir agregando nuevas funciones a medida que crecen. |
| Forma de adquirir el sistema | Puede utilizarse en la nube o mediante una instalación propia, dependiendo de la implementación. | Funciona principalmente como un servicio en la nube, por lo que el usuario accede a través de internet. | Cuenta con opciones en la nube y también permite instalar y administrar el sistema por cuenta propia, especialmente con su versión Community. |
| Poder del manejo de inventarios | Permite controlar inventarios, compras, producción. proveedores y trazabilidad de productos. | Permite controlar existencias, movimientos, Kardex, costos y ventas mediantes POS. | Tiene herramientas más amplias para inventarios, como multialmacén, códigos de barras, lotes, series y diferentes rutas de abastecimiento. |
| Personalización | Permite realizar modificaciones y agregar funcionalidades, aunque normalmente se requiere apoyo especializado por parte del equipo técnico. | Es una solución más estandarizada y busca que el usuario pueda utilizar sus funciones sin realizar grandes modificaciones. | Tiene muchas posibilidades de personalización debido a su sistema de módulos y al código abierto de la versión Community. |
| Facilidad de uso | Puede necesitar un periodo de aprendizaje debido a la cantidad de funciones que ofrece | Está orientado a ser sencillo de utilizar, especialmente para procesos contables y administrativos. | Su sistema de aplicaciones facilita la organización, aunque la gran cantidad de opciones puede requerir algo de aprendizaje.. |
| Arquitectura | Utiliza una estructura de varias capas y diferentes componentes integrados. La implementación puede variar dependiendo de cómo sea instalado. | Es un sistema SaaS en la nube. La información disponible públicamente no permite saber con certeza si internamente utiliza una arquitectura monolítica, distribuida o híbrida. | Se puede identificar como un monolito modular, ya que sus diferentes aplicaciones funcionan integradas dentro de una misma plataforma. |

**Análisis**

Luego de observar esta comparación, podemos decir que existen soluciones muy robustas en el mercado para la gestión de inventarios, que además de cumplir con los requerimientos básicos, se expanden hacia otras áreas y permiten una integración sólida dentro de las organizaciones. Sin embargo, las diferencias en aspectos como la facilidad de uso, la personalización y la adaptación a las necesidades de cada empresa muestran que aún existen oportunidades para desarrollar soluciones más equilibradas y adaptables. Permitiendo optimizar la curva del aprendizaje optimizando esto tiempo valioso para la organización que lo desea implementar.

**Definición del problema y alcance del sistema a construir.**

Las micro, pequeñas y medianas empresas (PyMEs) suelen enfrentarse a desafíos operativos críticos en la gestión de sus inventarios, un área de vital importancia para su sostenibilidad financiera. En muchos casos, los negocios operan con procesos manuales, hojas de cálculo aisladas o herramientas genéricas que no se sincronizan en tiempo real con las ventas o las compras.

Esta desconexión genera problemas recurrentes como:

* Desfases entre el stock físico y el registrado en el sistema o el papel.  
* Dificultad para identificar alertas tempranas de reabastecimiento, lo que provoca pérdida de ventas por agotados o exceso de capital inmovilizado en mercancía de bajo rotación.  
* Sobrecarga operativa y errores humanos al duplicar registros entre diferentes áreas (por ejemplo, registrar una venta en caja y tener que actualizar el inventario manualmente).

Si bien existen soluciones robustas en el mercado como SAP Business One u Odoo, o plataformas cerradas como Siigo, estas alternativas a menudo presentan barreras significativas: costos de implementación elevados, curvas de aprendizaje complejas o una rigidez que impide adaptarlas a la dinámica específica de un negocio regional en crecimiento. Por lo tanto, existe la necesidad de desarrollar una solución orientada a equilibrar la funcionalidad esencial de control de inventarios con una  

**Alcance del Sistema (SisInv)**

El sistema **SisInv** se desarrollará como una solución informática orientada a modernizar y optimizar el control de mercancías para PyMEs, resolviendo los problemas de sobrecarga y complejidad operativa de los software tradicionales. Para cumplir con los requerimientos académicos del proyecto de aula, el alcance se divide en dos componentes principales: funcional y técnico.

### **2.1 Alcance Funcional** 

El sistema cubrirá los procesos core de la gestión de inventarios, implementando de forma equilibrada, práctica y robusta los siguientes módulos:

* **Gestión de Productos y Categorías:** Permite registrar, consultar, actualizar y dar de baja productos con atributos clave (código, nombre, descripción, categoría, precio y proveedor asociado), estructurados mediante categorías y subcategorías.  
* **Control de Inventarios y Bodegas:** Registro de movimientos de inventario (entradas, salidas, ajustes y traslados) para mantener actualizado el saldo disponible de cada producto según la ubicación o almacén físico.  
* **Gestión de Proveedores y Órdenes de Compra:** Administración básica de proveedores y la capacidad de generar y consultar órdenes de compra para recibir mercancía de forma controlada.  
* **Alertas de Stock Mínimo:** Notificaciones en la interfaz cuando el nivel de inventario de un producto se encuentre por debajo de un umbral mínimo configurable.  
* **Gestión de Usuarios y Autenticación:** Sistema de inicio de sesión seguro con control de acceso basado en roles diferenciados (por ejemplo, administrador y operador de bodega).

### **2.2 Alcance Técnico y Arquitectónico**

A nivel de ingeniería, el desarrollo se apegará estrictamente a los estándares solicitados para la infraestructura del sistema:

* **Arquitectura de Microservicios:** El software estará compuesto por servicios independientes y débilmente acoplados, divididos por dominios de negocio específicos (como productos, inventario, proveedores y usuarios), comunicados mediante API REST.  
* **Persistencia Políglota / Independiente:** Cada microservicio administrará su propia base de datos de manera aislada, evitando el acceso directo entre bases de datos de diferentes servicios.  
* **API Gateway Propio:** Todas las peticiones externas dirigidas al sistema pasarán obligatoriamente por un Gateway desarrollado de manera nativa por el equipo, sin hacer uso de soluciones de terceros como Kong.  
* **Contenerización y Orquestación:** Todos los microservicios se empaquetarán individualmente en contenedores Docker y se gestionarán mediante un entorno orquestado con Kubernetes.  
* **Pruebas de Rendimiento:** Ejecución de pruebas de carga, estrés y concurrencia sobre los endpoints definidos para evaluar métricas clave como tiempo de respuesta y tasa de error.

mayor accesibilidad, adaptabilidad y facilidad de uso.

**Arquitectura Monolítica vs. Microservicios**

Para definir la arquitectura de SisInv, se comparan dos alternativas principales: una arquitectura monolítica y una arquitectura basada en microservicios. La comparación se realiza teniendo en cuenta las necesidades funcionales y técnicas establecidas para el sistema, especialmente la gestión de inventarios, la escalabilidad, el mantenimiento, el aislamiento de datos y la posibilidad de desplegar los diferentes componentes de manera independiente. 

| Criterio | Monolítica | Microservicios |
| :---- | :---- | :---- |
| **Modularidad** | Los módulos forman parte de una misma aplicación. | Cada dominio funciona como un servicio independiente. |
| **Escalabilidad** | Se escala toda la aplicación. | Se puede escalar únicamente el servicio que lo necesite. |
| **Despliegue** | Los cambios pueden requerir desplegar todo el sistema. | Cada servicio puede desplegarse independientemente. |
| **Fallos** | Un problema puede afectar a toda la aplicación. | Los fallos pueden aislarse en un servicio. |
| **Base de datos** | Generalmente compartida. | Cada servicio administra su propia base de datos. |
| **Complejidad** | Menor complejidad inicial. | Mayor complejidad de comunicación y administración. |
| **Kubernetes** | Puede utilizarse, pero no aprovecha completamente sus ventajas. | Se adapta al despliegue y escalamiento independiente de servicios. |

Para SisInv se selecciona la arquitectura de microservicios porque permite separar el sistema en dominios como usuarios, productos, inventario y proveedores, facilitando su mantenimiento, escalabilidad y evolución independiente.

**Definición de los microservicios del sistema**   
A partir de los procesos principales de SisInv, se identifican los siguientes dominios o bounded contexts. Cada uno representa una responsabilidad específica del sistema y tendrá su propia lógica y base de datos.

| Microservicio / Dominio | Responsabilidades principales |
| :---- | :---- |
| **Usuarios y Autenticación** | Registro, inicio de sesión, gestión de usuarios y control de roles y permisos. |
| **Productos** | Crear, consultar, actualizar y dar de baja productos, categorías y subcategorías. |
| **Inventario** | Gestionar existencias, entradas, salidas, ajustes, traslados y stock mínimo por bodega. |
| **Proveedores** | Registrar y administrar proveedores asociados a los productos. |
| **Órdenes de Compra** | Crear, consultar y gestionar órdenes de compra y recepción de mercancía. |
| **API Gateway** | Punto de entrada al sistema. Recibe las peticiones externas y las dirige al microservicio correspondiente. |

**Relación entre los dominios**

Los microservicios estarán desacoplados y se comunicarán mediante API REST. Por ejemplo, una orden de compra puede requerir información del microservicio de productos y, al recibir mercancía, generar una operación en el microservicio de inventario.

Cada microservicio será responsable de sus propios datos, evitando que un servicio acceda directamente a la base de datos de otro. El API Gateway será el punto de entrada para las solicitudes realizadas por los clientes.

**Mecanismo de comunicación entre microservicios**

Para SisInv se utilizará principalmente una comunicación síncrona mediante API REST, debido a que los procesos del sistema requieren respuestas inmediatas. Por ejemplo, el microservicio de órdenes de compra puede consultar al servicio de productos para validar la información antes de registrar una orden.

La comunicación seguirá el siguiente esquema:

Cliente → API Gateway → Microservicio 

Para esta primera versión no se implementará mensajería asíncrona, ya que aumentaría la complejidad del sistema. Sin embargo, podría incorporarse posteriormente para procesos que no requieran una respuesta inmediata, como notificaciones o generación de reportes.

**Requerimientos Funcionales (RF)**

* **RF01 — Gestión de productos:** El sistema debe permitir crear, consultar, actualizar y dar de baja productos dentro del microservicio de productos, incluyendo atributos como código único, nombre, descripción, categoría, unidad de medida, precio y proveedor asociado, sincronizando la información vía API REST con el dominio de inventario.  
* **RF02 — Gestión de categorías:** El sistema debe permitir crear, consultar, actualizar y eliminar categorías y subcategorías de productos.  
* **RF03 — Gestión de proveedores:** El sistema debe permitir registrar, consultar, actualizar y eliminar proveedores, y asociarlos a uno o varios productos.  
* **RF04 — Control de stock:** El sistema debe permitir registrar de forma transaccional movimientos de inventario (entradas, salidas, ajustes y traslados) y mantener actualizado el saldo disponible de cada producto en cada bodega o almacén de manera aislada.  
* **RF05 — Gestión de almacenes o bodegas:** El sistema debe permitir administrar múltiples ubicaciones físicas de almacenamiento y consultar el stock de un producto por ubicación.  
* **RF06 — Órdenes de compra:** El sistema debe permitir generar, consultar y actualizar el estado de órdenes de compra a proveedores, permitiendo recibir mercancía contra dichas órdenes para afectar automáticamente el inventario.  
* **RF07 — Gestión de usuarios y roles:** El sistema debe permitir el registro, consulta, actualización y asignación de usuarios, delimitando permisos estrictos para los dos roles clave del proyecto (Administrador y Operador de Bodega).  
* **RF08 — Autenticación de usuarios:** El sistema debe permitir inicio de sesión, cierre de sesión, recuperación de contraseña y cambio de contraseña.  
* **RF09 — Alertas de stock:** El sistema debe notificar en la interfaz de usuario cuando el nivel de stock disponible de un producto esté por debajo de un umbral mínimo configurable por bodega.  
* **RF10 — Trazabilidad y auditoría:** El sistema debe registrar quién, cuándo y qué movimiento se realizó sobre el inventario, generando un historial o Kardex auditable por producto.  
* **RF11 — Reportes:** El sistema debe generar reportes básicos de inventario (existencias actuales, valorización del inventario, productos con mayor y menor rotación).  
* **RF12 — Búsqueda y filtrado:** El sistema debe permitir buscar y filtrar productos por nombre, código, categoría o proveedor.  
* **RF13 — Gestión de devoluciones:** El sistema debe permitir registrar devoluciones de productos tanto de clientes como hacia proveedores, reflejando de forma inmediata el reingreso o salida en el stock.  
* **RF14 — Panel de indicadores (dashboard):** El sistema debe presentar un panel gráfico (dashboard) en tiempo real con indicadores clave del inventario (rotación, quiebres de stock y valor total).  
* **RF15 — Gestión de transferencias entre bodegas:** El sistema debe permitir planificar, ejecutar y confirmar traslados de mercancía entre diferentes bodegas o almacenes físicos, generando el descargo en origen y el ingreso automático en destino.

**Requerimientos No Funcionales (RNF)**

* **RNF01 — Arquitectura:** El sistema debe estar construido bajo una arquitectura de microservicios, con servicios independientes y débilmente acoplados por dominios de negocio, comunicados mediante API REST.  
* **RNF02 — Persistencia independiente:** Cada microservicio debe gestionar su propia base de datos de manera aislada, prohibiendo el acceso directo de un servicio a la base de datos de otro.  
* **RNF03 — Contenerización:** Todos los microservicios y sus dependencias (bases de datos, etc.) deben ejecutarse en contenedores Docker.  
* **RNF04 — Orquestación:** El sistema debe desplegarse y gestionarse obligatoriamente mediante Kubernetes; el uso de Kubernetes no es opcional.  
* **RNF05 — Escalabilidad:** La arquitectura debe permitir escalar de forma independiente y granular los microservicios con mayor carga transaccional, como el de consulta y control de stock.  
* **RNF06 — Rendimiento:** El sistema debe responder a las operaciones de consulta en un tiempo menor a 2 segundos bajo una carga concurrente definida y sustentada por el equipo.  
* **RNF07 — Seguridad:** Las comunicaciones y la autenticación deben protegerse mediante mecanismos estándar (por ejemplo, JWT/OAuth2, cifrado de contraseñas).  
* **RNF08 — Documentación de API:** Cada microservicio debe exponer documentación de su API mediante OpenAPI/Swagger o equivalente.  
* **RNF09 — API Gateway propio:** Todas las peticiones dirigidas al sistema deben pasar obligatoriamente por un API Gateway construido y desarrollado de forma nativa por el equipo; no se permite el uso de Kong ni de soluciones de terceros.  
* **RNF10 — Observabilidad:** El sistema debe contar con un registro (logging) centralizado o consultable por cada microservicio para facilitar la trazabilidad y depuración de errores.  
* **RNF11 — Pruebas de rendimiento:** Cada integrante del equipo debe definir y ejecutar un mínimo de quince (15) pruebas de rendimiento sobre los endpoints que él mismo defina, con sus resultados documentados.  
* **RNF12 — Control de versiones en GitHub:** Todo el proyecto debe alojarse en un repositorio de GitHub por equipo, en el cual debe evidenciarse la actividad (commits, ramas y pull requests) de todos los integrantes.  
* **RNF13 — Mantenibilidad:** El código debe seguir buenas prácticas de diseño de software (bajo acoplamiento, alta cohesión).  
* **RNF14 — Portabilidad:** Gracias a la contenerización, el sistema debe poder desplegarse en cualquier entorno compatible con Docker y Kubernetes sin cambios en el código fuente.  
* **RNF15 — Tecnologías permitidas:** Únicamente pueden emplearse los lenguajes, frameworks, bases de datos y demás herramientas vistas y trabajadas durante las clases del curso.  
* **RNF16 — Uso documentado de IA:** El proceso de desarrollo debe evidenciar, mediante las bitácoras correspondientes, el uso crítico y comprendido de herramientas de inteligencia artificial.  
* **RNF17 — Resiliencia y manejo de fallos:** Los microservicios deben implementar estrategias básicas de tolerancia a fallos y manejo de tiempos de espera (timeouts) para evitar caídas en cascada cuando un servicio dependiente presente intermitencia.

**Bitácora de uso de IA**

| Proyecto | Sistema de Gestión de Inventarios – SisInv Soluciones |
| :---- | :---- |
| **Equipo / Integrantes** | Cristian Camilo González Villa \- Miguel Ángel Ocampo Loaiza |
| **Entrega N.°** | 1 |
| **Periodo cubierto** | 16/09/2026 \- 28/09/2026 |

| Fecha | Integrante | Herramienta de IA | Tarea | Prompt utilizado | Nivel de intervención humana | Resultado /Aprendizaje |
| :---- | :---- | :---- | :---- | :---- | :---- | :---- |
| 16/09/26 | Cristian Camilo González Villa | Gemini  | Buscar los 3 sistemas de gestión de inventarios más usados en latinoamérica  | “Realiza la búsqueda de los 3 sistemas de gestión de inventario más usados en Latinoamérica.” | **Alta**. El fin de esta consulta es comparar con ChatGPT y ver si concuerdan con los resultados arrojados para posteriormente hacer una búsqueda manual en la web y entrar a indagar en cada uno de estos sistemas a profundidad. | \- SAP Business One \- Odoo Inventory \- Zoho Inventory  |
| 16/09/26 | Cristian Camilo Gonzalez Villa | ChatGPT | Buscar los 3 sistemas de gestión de inventarios más usados en latinoamérica  | “Realiza la búsqueda de los 3 sistemas de gestión de inventario más usados en Latinoamérica.” | **Alta**. El fin de esta consulta es comparar con ChatGPT y ver si concuerdan con los resultados arrojados para posteriormente hacer una búsqueda manual en la web y entrar a indagar en cada uno de estos sistemas a profundidad. | \- SAP Business One \- TOTVS Protheus  \- Oracle NetSuite  |
| 19/09/26 | Cristian Camilo Gonzalez Villa | Gemini | Obtener fuentes oficiales en donde se hable del tipo de arquitectura de cada uno de los sistemas elegidos | “Estoy haciendo una labor de investigación en donde estoy revisando los siguientes sistemas de inventarios SAP Business One Siigo Odoo Necesito que me digas la arquitectura de cada uno de ellos y que ademas me traigas las fuentes oficiales en donde se habla de esto.” | **Media:** Me ayudo bastante mostrando la fuente de la información oficial, sin embargo en algunos casos me traía enlaces a blogs que no eran tan certeros con la información. A tal punto de que la IA me aseguraba que Siigo era monolítica, cuando ninguna información pública permite asegurar esto. | Se estructuró la clasificación técnica por modelo de arquitectura y el logro principal fue la extracción y validación de las fuentes oficiales de referencia para cada sistema, más allá de recibir una descripción general de la infraestructura.   |
| 21/09/26 | Miguel Ángel Ocampo Loaiza | ChatGPT | Comparar y justificar la arquitectura de SisInv | Compara arquitectura monolítica y microservicios para un sistema de gestión de inventarios llamado SisInv, utilizando criterios técnicos como modularidad, escalabilidad, despliegue, fallos, bases de datos, complejidad y Kubernetes. Finalmente, justifica la selección de microservicios. | Media. Se revisó la información y se ajustó conforme a los requisitos del proyecto.   | Logré identificar las diferencias entre ambas arquitecturas más claramente y se pude justificar la implementación de microservicios para SisInv. |
| 25/09/26  | Miguel Ángel Ocampo Loaiza | ChatGPT | Identificar los microservicios y sus responsabilidades | Identifica los dominios/bounded contexts y define los microservicios correspondientes (usuarios, productos, inventario/bodegas, proveedores, órdenes de compra y API Gateway). Indica sus responsabilidades breves, bases de datos independientes y comunicación vía API REST.  | **Media.** Se revisó y ajustó la propuesta de acuerdo con el alcance definido para SisInv.  | Identificamos los principales dominios del sistema y se establecieron sus responsabilidades, permitiendo definir una separación clara entre los diferentes microservicios.  |
| 26/09/26 | Cristian Camilo González Villa | Gemini  | Evaluar RF y RNF, además de encontrar posibles sugerencias y ajustes. | Evalúa los RF y los RNF con la lógica del proyecto, sugiere nuevos y muéstrame cuales podrían ser ajustados para lograr un buen proyecto académico. | **Media:** La IA nos dio una base sólida usando de punto de partida los RF y los RNF del documento del proyecto, creó algunas recomendaciones un poco extrañas y términos los cuales no conocemos. Sin embargo, algunas recomendaciones fueron precisas y de gran ayuda para este proceso y optamos por usarlas | Lista de RF y RNF con información extensa y compleja, algunos con sugerencias valiosas. |
| 27/09/26 | Cristian Camilo Gonzalez Villa | Gemini | Crear archivo .md para cargar en github con estructura estética  | Convierte este archivo en formato .md. | **Alta:** Se validó que fuera la misma información y se usó lo dado por la IA | El archivo del entregable en formato .md |

Referencias

[Cuánto cuesta SAP Business One en Colombia](https://www.heinsohn.co/co/blog/cuanto-cuesta-sap-business-one-en-colombia/) 

[Conoce los beneficios que Siigo Nube tiene para ti](https://www.siigo.com/blog/tecnologia-innovacion/beneficios-de-siigo-nube-a-largo-plazo/) 

[Visión general de la arquitectura | Portal de Ayuda SAP](https://help.sap.com/docs/SAP_BUSINESS_ONE/f110a154dd0f4c20bf7f3ebca9eeb794/36a5b88dce7d4d3b8c1abf1ac4e9dd2d.html?utm_source=gemini&locale=en-US) 

[Sahil Mahadwar \- Software developer, founder, and bug fixing ninja.](https://www.sahil.id/articles/odoo-architecture-mvc-explained?utm_source=gemini) 

[Odoo Documentation — Odoo 19.0 documentation](https://www.odoo.com/documentation/19.0/?utm_source=gemini) 

[Conoce qué es Siigo y cómo impulsar tu negocio y profesión](https://www.siigo.com/blog/emprendimiento/que-es-siigo/?utm_source=gemini) 

[Microservices](https://martinfowler.com/articles/microservices.html?utm_source=gemini) 

[image1]: <data:image/png;base64,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>
