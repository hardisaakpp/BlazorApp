# BlazorApp

Una aplicación de demostración desarrollada con **Blazor Server** y **.NET 8** que muestra las funcionalidades principales del framework Blazor de Microsoft.

## ?? Descripción

Esta aplicación sirve como ejemplo de aprendizaje para desarrolladores que quieren familiarizarse con Blazor Server. Incluye varios componentes interactivos que demuestran diferentes características y patrones de desarrollo en Blazor.

## ? Características

- **Blazor Server** con renderizado interactivo del lado del servidor
- **Componentes reutilizables** con parámetros
- **Binding bidireccional** de datos
- **Renderizado asíncrono** con StreamRendering
- **Navegación SPA** (Single Page Application)
- **Responsive design** con Bootstrap
- **Manejo de estado** en componentes

## ?? Páginas y Funcionalidades

### ?? Home (`/`)
Página principal de bienvenida que incluye un componente Counter integrado.

### ?? Counter (`/counter`)
Contador interactivo que demuestra:
- Manejo de eventos con `@onclick`
- Estado de componente
- Parámetros de componente personalizables
- Binding de datos

### ??? Weather (`/weather`)
Simulador del clima que muestra:
- Renderizado asíncrono con `[StreamRendering]`
- Carga de datos simulada
- Presentación de datos en tablas
- Generación de datos aleatorios

### ? Todo (`/todo`)
Lista de tareas interactiva que incluye:
- Agregar nuevas tareas
- Marcar tareas como completadas
- Binding bidireccional (`@bind`)
- Manejo de listas dinámicas
- Renderizado interactivo del servidor

## ??? Tecnologías Utilizadas

- **.NET 8**
- **Blazor Server**
- **Bootstrap 5** para estilos
- **C# 12** con nullable reference types habilitados
- **Implicit usings** habilitados

## ?? Instalación y Configuración

### Prerrequisitos

- [.NET 8 SDK](https://dotnet.microsoft.com/download/dotnet/8.0) o superior
- Visual Studio 2022 (recomendado) o Visual Studio Code

### Pasos de instalación

1. **Clonar el repositorio**
   ```bash
   git clone [URL-del-repositorio]
   cd BlazorApp
   ```

2. **Restaurar dependencias**
   ```bash
   dotnet restore
   ```

3. **Ejecutar la aplicación**
   ```bash
   dotnet run
   ```

4. **Abrir en el navegador**
   
   Navega a `https://localhost:7xxx` o `http://localhost:5xxx` (los puertos se mostrarán en la consola)

## ??? Uso

### Desarrollo
```bash
# Ejecutar en modo desarrollo
dotnet run

# Ejecutar con hot reload
dotnet watch run
```

### Compilación
```bash
# Compilar la aplicación
dotnet build

# Compilar para producción
dotnet publish -c Release
```

## ?? Estructura del Proyecto

```
BlazorApp/
??? Components/
?   ??? Layout/
?   ?   ??? MainLayout.razor      # Layout principal
?   ?   ??? NavMenu.razor         # Menú de navegación
?   ??? Pages/
?   ?   ??? Counter.razor         # Página del contador
?   ?   ??? Error.razor           # Página de error
?   ?   ??? Home.razor            # Página principal
?   ?   ??? Todo.razor            # Lista de tareas
?   ?   ??? Weather.razor         # Pronóstico del tiempo
?   ??? App.razor                 # Componente raíz
?   ??? Routes.razor              # Configuración de rutas
?   ??? _Imports.razor            # Importaciones globales
??? wwwroot/                      # Archivos estáticos
??? TodoItem.cs                   # Modelo de datos
??? Program.cs                    # Configuración de la aplicación
??? BlazorApp.csproj             # Archivo de proyecto
```

## ?? Componentes Principales

### TodoItem.cs
```csharp
public class TodoItem
{
    public string? Title { get; set; }
    public bool IsDone { get; set; } = false;
}
```

Modelo simple para representar una tarea en la lista de tareas pendientes.

## ?? Conceptos de Blazor Demostrados

- **Component Parameters**: Parámetros en el componente Counter
- **Event Handling**: Manejo de clicks y eventos de entrada
- **Data Binding**: Binding unidireccional y bidireccional
- **Conditional Rendering**: Renderizado condicional en Weather
- **Lists and Loops**: Iteración sobre listas en Todo y Weather
- **Server-Side Interactivity**: Renderizado interactivo del servidor
- **Stream Rendering**: Renderizado asíncrono para mejorar la experiencia del usuario

## ?? Contribuir

1. Fork el proyecto
2. Crea una rama para tu característica (`git checkout -b feature/AmazingFeature`)
3. Commit tus cambios (`git commit -m 'Add some AmazingFeature'`)
4. Push a la rama (`git push origin feature/AmazingFeature`)
5. Abre un Pull Request

## ?? Recursos Adicionales

- [Documentación oficial de Blazor](https://docs.microsoft.com/aspnet/core/blazor/)
- [Blazor University](https://blazor-university.com/)
- [Awesome Blazor](https://github.com/AdrienTorris/awesome-blazor)

## ?? Licencia

Este proyecto está bajo la Licencia MIT. Ver el archivo `LICENSE` para más detalles.

---

? Si este proyecto te resulta útil, ¡no olvides darle una estrella!