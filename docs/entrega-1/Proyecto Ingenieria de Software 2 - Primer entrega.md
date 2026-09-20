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

<div style="page-break-after: always;"></div>

## Sistemas elegidos

### 1. SAP Business One

ERP diseñado para pequeñas y medianas empresas (PyMEs) cuyo propósito es centralizar y gestionar las operaciones clave del negocio en una sola plataforma.

Cuentan entre su apartado con las siguientes características principales:

- **Finanzas y Contabilidad:** Control de flujo de caja, presupuestos y conciliaciones.
- **Ventas y CRM:** Gestión de oportunidades, clientes y ciclo de venta.
- **Compras e Inventario:** Control de stock, proveedores y trazabilidad de productos.
- **Producción y MRP:** Planificación de requerimientos de material y órdenes de fabricación.
- **Cumplimiento Fiscal:** Adaptación a la facturación electrónica y normativa local.
- **Analítica e Informes:** Dashboards interactivos y reportes en tiempo real.
- **Acceso:** Aplicación móvil, versión web y de escritorio (Nube u on-premise).
- **Integración** de herramientas propias de SAP como lo es SAP HANA para acelerar operaciones con una base de datos de alto rendimiento.

**Especificaciones técnicas**

Se basa en un modelo clásico de tres capas, las cuales son:

- **Capa de presentación:** Es la interfaz de usuario (la aplicación de escritorio instalada o sus adaptaciones en la web y móviles).
- **Capa lógica de negocio:** Servidor centralizado que procesa todas las reglas del negocio, transacciones y peticiones de forma unificada.
- **Capa de Base de Datos:** Utiliza un motor de base de datos relacional centralizado. Toda la información de finanzas, inventarios, compras y ventas se aloja y se procesa dentro de una misma instancia de base de datos bajo el mismo esquema relacional.

> En el sitio web oficial de SAP observamos un sistema que se vende como un sistema modular muy completo, aunque podemos deducir que en realidad es un monolito robusto. Esto lo podemos deducir porque aunque sus módulos parecen separados (inventarios, ventas, contabilidad, etc.) por dentro todo vive y funciona conectado a la misma base de datos y al mismo servidor. Si se necesita actualizar el sistema, hay que actualizar el bloque completo, y si por alguna razón el servidor se satura o se cae, se detiene toda la operación de la empresa.

---

### 2. Siigo

Software contable y administrativo en la nube diseñado para micro, pequeñas y medianas empresas (PyMEs) y contadores, enfocado en la automatización operativa y el cumplimiento fiscal.

Cuentan entre su apartado con las siguientes características principales:

- **Contabilidad Automatizada:** Generación de estados financieros, libros auxiliares y cálculo de impuestos en tiempo real a partir de las ventas y compras.
- **Control de Inventarios:** Seguimiento de stock, costeo de productos, kardex y alertas de reabastecimiento.
- **Punto de Venta (POS):** Módulo para tiendas físicas sincronizado en vivo con la contabilidad y el inventario central.
- **Gestión de Cartera y Proveedores:** Control de cuentas por cobrar, alertas de facturas vencidas y gestión de pagos.
- **Reportes y Flujo de Caja:** Dashboards para monitorear ventas, egresos y rentabilidad del negocio de forma sencilla.
- **Plataforma 100% Nube:** Acceso multiusuario desde navegador o app móvil, sin requerir infraestructura física ni servidores.
- **Agente IA:** Resuelve consultas contables, tributarias, laborales y financieras.

**Especificaciones técnicas**

Funciona bajo un modelo de software como servicio (SaaS) en la nube, en el cual la infraestructura tecnológica es administrada por el proveedor y los usuarios acceden a la plataforma mediante Internet. Desde el punto de vista funcional, el sistema integra diferentes módulos para gestionar procesos como contabilidad, facturación, inventarios, cartera y punto de venta.

- **Capa de Cliente / Interfaz:** El usuario accede a la plataforma principalmente mediante un navegador web y aplicaciones móviles, sin necesidad de instalar o administrar localmente la infraestructura que soporta el sistema. La interfaz permite interactuar con los diferentes módulos y consultar la información empresarial.
- **Capa de Lógica de Negocio:** Las operaciones realizadas por los usuarios son procesadas por los servicios de aplicación administrados por Siigo en su infraestructura cloud. En esta capa se ejecutan las reglas de negocio y los procesos relacionados con facturación, contabilidad, inventarios, cartera y demás funcionalidades de la plataforma.
- **Capa de Datos:** La información generada por los usuarios, como facturas, movimientos de inventario, registros contables y datos financieros, es almacenada y administrada en la infraestructura tecnológica del proveedor. El usuario no administra directamente las bases de datos ni la infraestructura de almacenamiento.

Desde la perspectiva del usuario, Siigo presenta una plataforma centralizada e integrada, ya que los diferentes módulos son proporcionados y administrados por un mismo proveedor y se accede a ellos desde un entorno común. Sin embargo, no es posible afirmar con certeza que su arquitectura interna sea monolítica, debido a que Siigo no publica información técnica suficiente que permita determinar si internamente utiliza un monolito, microservicios o una arquitectura híbrida.

Del mismo modo, el hecho de que Siigo sea una plataforma SaaS administrada centralmente no significa que toda la infraestructura dependa de un único servidor. Al estar implementada en la nube, podría utilizar mecanismos como redundancia, balanceo de carga, replicación y otros recursos destinados a garantizar la disponibilidad y escalabilidad del servicio. Por lo tanto, las características específicas de su arquitectura interna, distribución de servicios y mecanismos de tolerancia a fallos no pueden determinarse únicamente a partir de la información pública disponible.

---

### 3. Odoo

Sistema ERP modular de código abierto diseñado para PyMEs y empresas en crecimiento, que permite integrar e interconectar todas las áreas del negocio según sus necesidades.

**Características clave**

- **Arquitectura Modular:** Posibilidad de implementar solo las aplicaciones necesarias (ej. Inventario, Facturación) e ir agregando módulos a medida que la empresa escala.
- **Inventario Avanzado:** Control multialmacén con sistema de doble entrada, trazabilidad por lotes/series, escaneo de código de barras y rutas automáticas (Drop-shipping y Cross-docking).
- **Integración de Ventas y E-commerce:** Sincronización nativa entre la tienda en línea integrada, Punto de Venta (POS) en tiendas físicas y gestión de presupuestos.
- **Contabilidad y Facturación:** Automatización de asientos contables a partir de las compras y ventas, con soporte para facturación electrónica en diversos países.
- **Producción y Compras (MRP):** Gestión de listas de materiales, órdenes de trabajo y reglas automáticas de reabastecimiento de stock.
- **Modelo y Acceso:** Versiones *Community* (código abierto) y *Enterprise* (nube/de pago), con acceso 100% web y desde aplicación móvil.

**Especificaciones técnicas**

Odoo funciona como una plataforma modular desarrollada principalmente en Python y utiliza PostgreSQL para almacenar la información. Su principal característica es que las diferentes aplicaciones del sistema, como Inventario, Ventas, Contabilidad y Compras, pueden instalarse según las necesidades de cada empresa, pero todas hacen parte de la misma plataforma.

- **Capa de Presentación / Cliente:** Los usuarios pueden acceder a Odoo principalmente mediante un navegador web. También cuenta con opciones para utilizar algunas de sus funciones desde dispositivos móviles. Desde esta interfaz, los usuarios pueden consultar y gestionar la información de las diferentes aplicaciones.
- **Capa de Lógica de Negocio:** En esta parte se encuentran las funciones que permiten realizar las diferentes operaciones del sistema. Los módulos de Odoo se encargan de procesos como ventas, inventarios, compras, contabilidad y producción, pero todos funcionan dentro de la misma plataforma de Odoo.
- **Capa de Base de Datos:** Odoo utiliza PostgreSQL para almacenar la información. Los diferentes módulos comparten los datos almacenados, lo que permite que, por ejemplo, una venta pueda actualizar el inventario y generar la información correspondiente para contabilidad.

Una de las principales ventajas de Odoo es que su código fuente es público en su edición Community, por lo que es posible revisar cómo está construido el sistema. Al analizar su estructura, se puede identificar como un **monolito modular**, ya que sus diferentes aplicaciones funcionan como módulos dentro de una misma plataforma, en lugar de ser sistemas completamente independientes.

Esta característica permite que las diferentes áreas de la empresa estén muy conectadas entre sí y que la información pueda compartirse fácilmente entre los módulos. Sin embargo, también significa que existe una mayor dependencia entre las diferentes partes del sistema en comparación con una arquitectura basada completamente en servicios independientes.

> Es importante aclarar que decir que Odoo es un sistema monolítico no significa que necesariamente funcione en un único servidor físico. Una empresa puede implementar Odoo utilizando diferentes servidores y recursos para mejorar su funcionamiento. El término monolito modular se refiere principalmente a la forma en que están organizadas e integradas las aplicaciones dentro del sistema.

---

## Comparación entre los 3 sistemas

Se plantea hacer una comparación desde diferentes puntos que consideramos que son importantes a la hora de usar sistemas de este tipo, los puntos son:

- Perfil de empresa
- Forma de adquirir el sistema
- Poder del manejo de inventarios (nuestro interés principal)
- Personalización
- Facilidad de uso
- Arquitectura

| Criterio | SAP Business One | Siigo | Odoo |
|---|---|---|---|
| **Perfil de Empresa** | Está dirigido principalmente a pequeñas y medianas empresas que necesitan manejar diferentes áreas del negocio en un solo sistema. | Está dirigido principalmente a micro, pequeñas y medianas empresas, emprendedores y contadores. | Está dirigido a pequeñas y medianas empresas y también a empresas que necesitan ir agregando nuevas funciones a medida que crecen. |
| **Forma de adquirir el sistema** | Puede utilizarse en la nube o mediante una instalación propia, dependiendo de la implementación. | Funciona principalmente como un servicio en la nube, por lo que el usuario accede a través de internet. | Cuenta con opciones en la nube y también permite instalar y administrar el sistema por cuenta propia, especialmente con su versión Community. |
| **Poder del manejo de inventarios** | Permite controlar inventarios, compras, producción, proveedores y trazabilidad de productos. | Permite controlar existencias, movimientos, Kardex, costos y ventas mediante POS. | Tiene herramientas más amplias para inventarios, como multialmacén, códigos de barras, lotes, series y diferentes rutas de abastecimiento. |
| **Personalización** | Permite realizar modificaciones y agregar funcionalidades, aunque normalmente se requiere apoyo especializado por parte del equipo técnico. | Es una solución más estandarizada y busca que el usuario pueda utilizar sus funciones sin realizar grandes modificaciones. | Tiene muchas posibilidades de personalización debido a su sistema de módulos y al código abierto de la versión Community. |
| **Facilidad de uso** | Puede necesitar un periodo de aprendizaje debido a la cantidad de funciones que ofrece. | Está orientado a ser sencillo de utilizar, especialmente para procesos contables y administrativos. | Su sistema de aplicaciones facilita la organización, aunque la gran cantidad de opciones puede requerir algo de aprendizaje. |
| **Arquitectura** | Utiliza una estructura de varias capas y diferentes componentes integrados. La implementación puede variar dependiendo de cómo sea instalado. | Es un sistema SaaS en la nube. La información disponible públicamente no permite saber con certeza si internamente utiliza una arquitectura monolítica, distribuida o híbrida. | Se puede identificar como un monolito modular, ya que sus diferentes aplicaciones funcionan integradas dentro de una misma plataforma. |

---

## Análisis

Luego de observar esta comparación, podemos decir que existen soluciones muy robustas en el mercado para la gestión de inventarios, que además de cumplir con los requerimientos básicos, se expanden hacia otras áreas y permiten una integración sólida dentro de las organizaciones. Sin embargo, las diferencias en aspectos como la facilidad de uso, la personalización y la adaptación a las necesidades de cada empresa muestran que aún existen oportunidades para desarrollar soluciones más equilibradas y adaptables. Permitiendo optimizar la curva del aprendizaje, optimizando así este tiempo valioso para la organización que lo desea implementar.

---

## Bitácora de uso de IA

| | |
|---|---|
| **Proyecto** | Sistema de Gestión de Inventarios – SisInv Soluciones |
| **Equipo / Integrantes** | Cristian Camilo González Villa · Miguel Ángel Ocampo Loaiza |
| **Entrega N.°** | 1 |
| **Periodo cubierto** | 16/09/2026 – 28/09/2026 |

| Fecha | Integrante | Herramienta de IA | Tarea | Prompt utilizado | Nivel de intervención humana | Resultado / Aprendizaje |
|---|---|---|---|---|---|---|
| 16/09/26 | Cristian Camilo González Villa | Gemini | Buscar los 3 sistemas de gestión de inventarios más usados en Latinoamérica | "Realiza la búsqueda de los 3 sistemas de gestión de inventario más usados en Latinoamérica." | **Alta.** El fin de esta consulta es comparar con ChatGPT y ver si concuerdan con los resultados arrojados para posteriormente hacer una búsqueda manual en la web y entrar a indagar en cada uno de estos sistemas a profundidad. | - SAP Business One<br>- Odoo Inventory<br>- Zoho Inventory |
| 16/09/26 | Cristian Camilo Gonzalez Villa | ChatGPT | Buscar los 3 sistemas de gestión de inventarios más usados en Latinoamérica | "Realiza la búsqueda de los 3 sistemas de gestión de inventario más usados en Latinoamérica." | **Alta.** El fin de esta consulta es comparar con ChatGPT y ver si concuerdan con los resultados arrojados para posteriormente hacer una búsqueda manual en la web y entrar a indagar en cada uno de estos sistemas a profundidad. | - SAP Business One<br>- TOTVS Protheus<br>- Oracle NetSuite |
| 19/09/26 | Cristian Camilo Gonzalez Villa | Gemini | Obtener fuentes oficiales en donde se hable del tipo de arquitectura de cada uno de los sistemas elegidos | "Estoy haciendo una labor de investigación en donde estoy revisando los siguientes sistemas de inventarios SAP Business One, Siigo, Odoo. Necesito que me digas la arquitectura de cada uno de ellos y que además me traigas las fuentes oficiales en donde se habla de esto." | **Media.** Me ayudó bastante mostrando la fuente de la información oficial, sin embargo en algunos casos me traía enlaces a blogs que no eran tan certeros con la información. A tal punto de que la IA me aseguraba que Siigo era monolítica, cuando ninguna información pública permite asegurar esto. | Se estructuró la clasificación técnica por modelo de arquitectura y el logro principal fue la extracción y validación de las fuentes oficiales de referencia para cada sistema, más allá de recibir una descripción general de la infraestructura. |

---

## Referencias

1. [Cuánto cuesta SAP Business One en Colombia](https://www.heinsohn.co/co/blog/cuanto-cuesta-sap-business-one-en-colombia/)
2. [Conoce los beneficios que Siigo Nube tiene para ti](https://www.siigo.com/blog/tecnologia-innovacion/beneficios-de-siigo-nube-a-largo-plazo/)
3. [Visión general de la arquitectura | Portal de Ayuda SAP](https://help.sap.com/docs/SAP_BUSINESS_ONE/f110a154dd0f4c20bf7f3ebca9eeb794/36a5b88dce7d4d3b8c1abf1ac4e9dd2d.html?utm_source=gemini&locale=en-US)
4. [Sahil Mahadwar - Software developer, founder, and bug fixing ninja.](https://www.sahil.id/articles/odoo-architecture-mvc-explained?utm_source=gemini)
5. [Odoo Documentation — Odoo 19.0 documentation](https://www.odoo.com/documentation/19.0/?utm_source=gemini)
6. [Conoce qué es Siigo y cómo impulsar tu negocio y profesión](https://www.siigo.com/blog/emprendimiento/que-es-siigo/?utm_source=gemini)
