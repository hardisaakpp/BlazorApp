# BlazorApp

Una aplicaci�n de demostraci�n desarrollada con **Blazor Server** y **.NET 8** que muestra las funcionalidades principales del framework Blazor de Microsoft.

## ?? Descripci�n

Esta aplicaci�n sirve como ejemplo de aprendizaje para desarrolladores que quieren familiarizarse con Blazor Server. Incluye varios componentes interactivos que demuestran diferentes caracter�sticas y patrones de desarrollo en Blazor.

## ? Caracter�sticas

- **Blazor Server** con renderizado interactivo del lado del servidor
- **Componentes reutilizables** con par�metros
- **Binding bidireccional** de datos
- **Renderizado as�ncrono** con StreamRendering
- **Navegaci�n SPA** (Single Page Application)
- **Responsive design** con Bootstrap
- **Manejo de estado** en componentes

## ?? P�ginas y Funcionalidades

### ?? Home (`/`)
P�gina principal de bienvenida que incluye un componente Counter integrado.

### ?? Counter (`/counter`)
Contador interactivo que demuestra:
- Manejo de eventos con `@onclick`
- Estado de componente
- Par�metros de componente personalizables
- Binding de datos

### ??? Weather (`/weather`)
Simulador del clima que muestra:
- Renderizado as�ncrono con `[StreamRendering]`
- Carga de datos simulada
- Presentaci�n de datos en tablas
- Generaci�n de datos aleatorios

### ? Todo (`/todo`)
Lista de tareas interactiva que incluye:
- Agregar nuevas tareas
- Marcar tareas como completadas
- Binding bidireccional (`@bind`)
- Manejo de listas din�micas
- Renderizado interactivo del servidor

## ??? Tecnolog�as Utilizadas

- **.NET 8**
- **Blazor Server**
- **Bootstrap 5** para estilos
- **C# 12** con nullable reference types habilitados
- **Implicit usings** habilitados

## ?? Instalaci�n y Configuraci�n

### Prerrequisitos

- [.NET 8 SDK](https://dotnet.microsoft.com/download/dotnet/8.0) o superior
- Visual Studio 2022 (recomendado) o Visual Studio Code

### Pasos de instalaci�n

1. **Clonar el repositorio**
   ```bash
   git clone [URL-del-repositorio]
   cd BlazorApp
   ```

2. **Restaurar dependencias**
   ```bash
   dotnet restore
   ```

3. **Ejecutar la aplicaci�n**
   ```bash
   dotnet run
   ```

4. **Abrir en el navegador**
   
   Navega a `https://localhost:7xxx` o `http://localhost:5xxx` (los puertos se mostrar�n en la consola)

## ??? Uso

### Desarrollo
```bash
# Ejecutar en modo desarrollo
dotnet run

# Ejecutar con hot reload
dotnet watch run
```

### Compilaci�n
```bash
# Compilar la aplicaci�n
dotnet build

# Compilar para producci�n
dotnet publish -c Release
```

## ?? Estructura del Proyecto

```
BlazorApp/
??? Components/
?   ??? Layout/
?   ?   ??? MainLayout.razor      # Layout principal
?   ?   ??? NavMenu.razor         # Men� de navegaci�n
?   ??? Pages/
?   ?   ??? Counter.razor         # P�gina del contador
?   ?   ??? Error.razor           # P�gina de error
?   ?   ??? Home.razor            # P�gina principal
?   ?   ??? Todo.razor            # Lista de tareas
?   ?   ??? Weather.razor         # Pron�stico del tiempo
?   ??? App.razor                 # Componente ra�z
?   ??? Routes.razor              # Configuraci�n de rutas
?   ??? _Imports.razor            # Importaciones globales
??? wwwroot/                      # Archivos est�ticos
??? TodoItem.cs                   # Modelo de datos
??? Program.cs                    # Configuraci�n de la aplicaci�n
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

- **Component Parameters**: Par�metros en el componente Counter
- **Event Handling**: Manejo de clicks y eventos de entrada
- **Data Binding**: Binding unidireccional y bidireccional
- **Conditional Rendering**: Renderizado condicional en Weather
- **Lists and Loops**: Iteraci�n sobre listas en Todo y Weather
- **Server-Side Interactivity**: Renderizado interactivo del servidor
- **Stream Rendering**: Renderizado as�ncrono para mejorar la experiencia del usuario

## ?? Contribuir

1. Fork el proyecto
2. Crea una rama para tu caracter�stica (`git checkout -b feature/AmazingFeature`)
3. Commit tus cambios (`git commit -m 'Add some AmazingFeature'`)
4. Push a la rama (`git push origin feature/AmazingFeature`)
5. Abre un Pull Request

## ?? Recursos Adicionales

- [Documentaci�n oficial de Blazor](https://docs.microsoft.com/aspnet/core/blazor/)
- [Blazor University](https://blazor-university.com/)
- [Awesome Blazor](https://github.com/AdrienTorris/awesome-blazor)

## ?? Licencia

Este proyecto est� bajo la Licencia MIT. Ver el archivo `LICENSE` para m�s detalles.

---

? Si este proyecto te resulta �til, �no olvides darle una estrella!