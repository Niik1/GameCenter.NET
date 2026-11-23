# 🎮 GameCenter.NET - Sistema de Gestión Comercial e Inventario

[![.NET Framework](https://img.shields.io/badge/.NET%20Framework-4.7.2-512BD4?style=flat&logo=dotnet&logoColor=white)](https://dotnet.microsoft.com/)
[![Language](https://img.shields.io/badge/Language-C%23-239120?style=flat&logo=c-sharp&logoColor=white)](https://learn.microsoft.com/dotnet/csharp/)
[![Database](https://img.shields.io/badge/Database-SQL%20Server-CC292B?style=flat&logo=microsoftsqlserver&logoColor=white)](https://www.microsoft.com/sql-server)
[![UI](https://img.shields.io/badge/UI-Windows%20Forms-0078D7?style=flat&logo=windows&logoColor=white)](https://learn.microsoft.com/dotnet/desktop/winforms/)
[![License](https://img.shields.io/badge/License-MIT-green.svg)](LICENSE)

Sistema de escritorio integral desarrollado para la administración, control de inventario, ventas y compras de una tienda especializada en videojuegos y tecnología (**GameCenter**).

---

## 📐 Arquitectura del Proyecto

El sistema está diseñado bajo el patrón de **Arquitectura en N-Capas (N-Tier)** para garantizar la separación de responsabilidades, escalabilidad y mantenibilidad:

```
├── ProyectoGameCenter (Capa de Presentación)
│   ├── Formularios WinForms (Dashboard MDI, Módulos con Flat UI)
│   ├── Controles de Usuario personalizados
│   └── Configuración de inicio (Program.cs)
│
├── LogicaNegocio (Capa de Negocio - BLL)
│   └── Validaciones y orquestación de operaciones de negocio (Singleton)
│
├── AccesoDatos (Capa de Datos - DAL)
│   └── Ejecución de Stored Procedures vía ADO.NET (Conexion.cs)
│
└── Entidades (Modelos / DTOs)
    └── Clases y estructuras de datos compartidas entre todas las capas
```

---

## 🚀 Funcionalidades y Módulos

### 🔐 Seguridad y Acceso
- Autenticación con ventana personalizada de inicio de sesión (`FrmLogin`).
- Panel principal responsivo con menú lateral desplegable.

### 👥 Clientes
- **Cliente Natural:** Registro y administración con validación de DNI y datos personales.
- **Cliente Jurídico:** Gestión empresarial mediante RUC, razón social y contacto.

### 📦 Catálogo e Inventario
- Mantenimiento de **Categorías** y **Marcas**.
- Catálogo de **Productos** con control de precios y control de stock mínimo.

### 🛒 Compras y Proveedores
- Directorio y gestión de **Proveedores**.
- Emisión y seguimiento de **Órdenes de Compra** con detalle de productos ingresados.

### 💰 Ventas y Finanzas
- Registro de **Órdenes de Venta** en mostrador.
- Configuración de **Métodos de Pago**.
- Generación de **Cronograma de Pagos** para ventas financiadas o a crédito.

### 🚚 Logística y Despacho
- Emisión de **Notas de Salida** para control de mercadería despachada de almacén.

---

## 🛠️ Requisitos Previos

- **Visual Studio 2019 / 2022** con la carga de trabajo *Desarrollo de escritorio de .NET*.
- **.NET Framework 4.7.2 Developer Pack**.
- **Microsoft SQL Server 2017** o superior (LocalDB / Express / Developer).
- **SQL Server Management Studio (SSMS)**.

---

## 📄 Licencia

Este proyecto se distribuye bajo la Licencia MIT. Consulta el archivo `LICENSE` para más detalles.
