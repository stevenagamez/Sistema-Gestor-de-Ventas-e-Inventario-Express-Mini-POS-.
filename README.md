Sistema Gestor de Ventas e Inventario Express (Mini-POS)
Información del estudiante

Nombre: Steven Andres Agamez Orozco
Programa: Ingeniería en Sistemas
Tecnología: C# / .NET 8

Descripción del proyecto

Este proyecto consiste en una aplicación de consola desarrollada en C# con .NET 8, creada como solución al Reto Final de la Unidad 1 de Fundamentos de C#.

El sistema permite gestionar productos, controlar el inventario, registrar ventas y consultar un reporte de caja y estadísticas de la sesión.

La información se maneja en memoria utilizando listas (List<T>), de acuerdo con los temas trabajados durante la Unidad 1.

Funcionalidades principales
Registrar nuevos productos.
Consultar el inventario completo.
Validar nombres de productos repetidos.
Mostrar alertas cuando el stock sea menor a 5 unidades.
Registrar ventas.
Validar que exista stock suficiente.
Aplicar descuento del 10% para clientes frecuentes.
Calcular IVA del 19%.
Actualizar automáticamente el stock después de una venta.
Generar un ticket de venta.
Consultar el total de ventas realizadas.
Consultar el dinero acumulado en caja.
Calcular el promedio de dinero por venta.
Mostrar el producto con mayor cantidad de unidades vendidas.
Tecnologías utilizadas
Lenguaje: C#
Framework: .NET 8
Tipo de aplicación: Aplicación de consola
Colecciones: List<T>

El proyecto utiliza los conceptos correspondientes a la Unidad 1, como variables, tipos de datos, condiciones, ciclos, switch, listas, métodos estáticos y manejo seguro de entradas.

Requisitos

Para ejecutar el proyecto se necesita:

Visual Studio 2022 con soporte para .NET 8, o
.NET 8 SDK instalado en el computador.
Estructura del proyecto
GestorVentasUnidad1/
│
├── GestorVentasUnidad1.sln
├── GestorVentasUnidad1.csproj
├── Program.cs
├── README.md
└── .gitignore
Cómo ejecutar el proyecto
Opción 1: Ejecutar desde Visual Studio
Descargar o clonar este repositorio.
Abrir Visual Studio.
Seleccionar Open a project or solution.
Abrir el archivo:
GestorVentasUnidad1.sln
Esperar a que Visual Studio cargue el proyecto.
Ejecutar el programa presionando:
Ctrl + F5

También se puede ejecutar utilizando el botón de inicio de Visual Studio.

Opción 2: Ejecutar desde la terminal

Primero clonar el repositorio:

git clone URL_DEL_REPOSITORIO

Después ingresar a la carpeta:

cd GestorVentasUnidad1

Ejecutar el proyecto:

dotnet run
Verificar que el proyecto compile

Antes de realizar la entrega se recomienda comprobar que el proyecto compile correctamente.

Ejecutar:

dotnet build

Si la compilación es correcta, se puede ejecutar con:

dotnet run
Menú principal

Al iniciar el programa se muestra el siguiente menú:

====================================================
   SISTEMA GESTOR DE VENTAS E INVENTARIO (MINI-POS)
====================================================
1. Registrar nuevo producto en inventario
2. Consultar inventario completo
3. Registrar una venta
4. Ver reporte de caja y estadísticas diarias
5. Salir
====================================================
Seleccione una opción (1-5):
Proceso de registro de productos

El sistema solicita:

Nombre del producto.
Precio unitario.
Stock inicial.

El nombre no puede estar vacío y no se permiten productos con el mismo nombre.

Proceso de venta

Para realizar una venta se selecciona el producto y la cantidad.

El sistema verifica que la cantidad solicitada no supere el stock disponible.

Los cálculos utilizados son:

Subtotal = Precio × Cantidad

Descuento = 10% del Subtotal

IVA = (Subtotal - Descuento) × 19%

Total a pagar = Subtotal - Descuento + IVA

Después de completar la venta, el sistema descuenta automáticamente las unidades vendidas del inventario.

Reporte de caja

El reporte muestra:

Total de ventas realizadas
Total acumulado ingresado a caja
Promedio de dinero por venta
Producto con mayor cantidad de unidades vendidas
Métodos principales

El proyecto implementa los cuatro métodos estáticos solicitados en la actividad:

static int LeerEntero(string mensaje, int min, int max)

Permite leer y validar números enteros.

static decimal LeerDecimal(string mensaje, decimal min)

Permite leer y validar números decimales.

static decimal CalcularFactura(
    decimal precio,
    int cantidad,
    bool tieneDescuento,
    out decimal montoIva,
    out decimal montoDescuento)

Realiza los cálculos de subtotal, descuento, IVA y total.

static void ImprimirEncabezado(string titulo)

Se utiliza para mostrar los encabezados de las diferentes secciones del programa.

Ejemplo de prueba

Una prueba básica del programa puede realizarse de la siguiente manera:

1. Registrar producto
   Nombre: Café Colombiano 500g
   Precio: 18000
   Stock: 10

2. Consultar inventario

3. Registrar venta
   Producto: Café Colombiano 500g
   Cantidad: 2
   Cliente frecuente: S

4. Consultar reporte

Después de realizar la venta de 2 unidades, el stock del producto debe quedar en:

Stock: 8
Control de errores

El programa valida entradas incorrectas mediante métodos como:

int.TryParse()

y

decimal.TryParse()

De esta manera se evita que entradas no válidas interrumpan la ejecución del programa.

Repositorio

Este proyecto está preparado para ser publicado en un repositorio de GitHub.

Se recomienda verificar el proyecto mediante:

dotnet build

y posteriormente:

dotnet run

antes de realizar la entrega.

Autor: Steven Andres Agamez Orozco
Programa: Ingeniería en Sistemas
