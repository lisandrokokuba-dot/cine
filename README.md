# 🎭 Academia Cinematográfica

> Sistema Integral de Administración Fílmica | Proyecto Django Avanzado

[![Python](https://img.shields.io/badge/Python-3.13-blue.svg)](https://python.org)
[![Django](https://img.shields.io/badge/Django-5.x-green.svg)](https://djangoproject.com)
[![Bootstrap](https://img.shields.io/badge/Bootstrap-Latest-purple.svg)](https://getbootstrap.com)
[![SQLite](https://img.shields.io/badge/Database-SQLite-orange.svg)](https://sqlite.org)

## 📖 Descripción del Proyecto

**Academia Cinematográfica** es una plataforma web robusta desarrollada con el framework Django de Python. Este sistema permite la administración completa de un catálogo cinematográfico, incluyendo películas, directores y géneros. Implementa las mejores prácticas de desarrollo web con arquitectura MVC, autenticación segura y una interfaz intuitiva.

### 🎯 Objetivo Académico
Proyecto desarrollado como parte del curso de Python de **Coderhouse**, demostrando dominio en:
- Desarrollo web con Django
- Patrones de diseño MVC
- Gestión de bases de datos relacionales
- Implementación de sistemas CRUD
- Autenticación y autorización de usuarios

## ⚡ Características Principales

### 🔍 **Motor de Búsqueda Inteligente**
- Sistema de búsqueda avanzada para localizar películas por título
- Filtros dinámicos y resultados en tiempo real
- Interfaz de búsqueda intuitiva y responsiva

### 📊 **Gestión Completa de Contenido**
- **Películas**: Crear, leer, actualizar y eliminar registros
- **Directores**: Administración completa de perfiles de directores
- **Géneros**: Categorización y gestión de géneros cinematográficos
- Relaciones entre entidades optimizadas

### 🔐 **Sistema de Autenticación Robusto**
- Registro y login de usuarios
- Permisos diferenciados por rol
- Panel administrativo protegido
- Gestión segura de sesiones

### 🎨 **Interfaz Moderna y Responsiva**
- Diseño adaptativo con Bootstrap Framework
- Herencia de plantillas optimizada (`base.html`)
- Experiencia de usuario fluida en todos los dispositivos
- Navegación intuitiva entre vistas

### 📝 **Formularios Dinámicos**
- Formularios personalizados con validación en tiempo real
- Manejo de errores elegante
- Campos dinámicos según el contexto
- Integración con modelos Django

## 🛠️ Stack Tecnológico

| Tecnología | Versión | Propósito |
|------------|---------|-----------|
| **Python** | 3.13 | Lenguaje de programación principal |
| **Django** | 5.x | Framework web backend |
| **HTML5** | Latest | Estructura y semántica web |
| **CSS3** | Latest | Estilos y diseño visual |
| **Bootstrap** | Latest | Framework CSS responsivo |
| **SQLite** | 3.x | Base de datos integrada |
| **Git** | Latest | Control de versiones |

## 🎬 Demostración en Vivo

**🎥 [Ver Video Explicativo Completo](https://www.youtube.com/watch?v=oKaojq4eJsk)**

Explora todas las funcionalidades del sistema en este tutorial interactivo que muestra:
- Navegación completa por la plataforma
- Funcionalidades CRUD en acción
- Sistema de búsqueda y filtros
- Panel de administración
- Experiencia de usuario completa

## 🚀 Guía de Instalación

### Prerrequisitos
- Python 3.13 o superior
- pip (gestor de paquetes de Python)
- Git

### Paso 1: Clonar el Repositorio
```bash
git clone https://github.com/lisandrokokuba-dot/cine.git
cd cine
```

### Paso 2: Crear Entorno Virtual (Recomendado)
```bash
python -m venv academia_cinema
source academia_cinema/bin/activate  # En Windows: academia_cinema\Scripts\activate
```

### Paso 3: Instalar Dependencias
```bash
pip install -r requirements.txt
```

### Paso 4: Configurar Base de Datos
```bash
python manage.py migrate
```

### Paso 5: Crear Usuario Administrador
```bash
python manage.py createsuperuser
```

### Paso 6: Iniciar Servidor de Desarrollo
```bash
python manage.py runserver
```

### 🌐 Acceso al Sistema

| Componente | URL | Descripción |
|------------|-----|-------------|
| **Aplicación Principal** | http://127.0.0.1:8000/ | Interfaz principal del usuario |
| **Panel Administrativo** | http://127.0.0.1:8000/admin/ | Panel de administración Django |

## 📁 Arquitectura del Proyecto

```
Core/
├── 📂 static/                    # Archivos estáticos
│   └── 🎯 favicon.ico           # Icono de la aplicación
├── 📂 media/                     # Archivos multimedia
│   ├── 📂 peliculas/            # Imágenes de películas
│   └── 📂 avatars/              # Avatares de usuarios
├── 📂 templates/Core/            # Plantillas HTML
│   ├── 📂 registration/         # Plantillas de autenticación
│   │   ├── 🔐 login.html       # Formulario de login
│   │   ├── 📝 signup.html      # Formulario de registro
│   │   └── 🚪 logged_out.html  # Página de logout
│   ├── ➕ agregar_director.html  # Formulario nuevo director
│   ├── ➕ agregar_genero.html    # Formulario nuevo género
│   ├── ➕ agregar_pelicula.html  # Formulario nueva película
│   ├── 📄 detalle_pelicula.html # Vista detalle película
│   ├── ✏️ editar_pelicula.html  # Formulario edición
│   ├── 🗑️ eliminar_pelicula.html # Confirmación eliminación
│   ├── 🎨 base.html             # Plantilla base
│   ├── 🔍 buscar.html           # Página de búsqueda
│   ├── 🎬 buscar_pelicula.html  # Resultados búsqueda
│   ├── 🏠 home.html             # Página principal
│   └── 🎭 inicio.html           # Página de bienvenida
├── 📋 admin.py                   # Configuración admin Django
├── 📱 apps.py                    # Configuración de la app
├── 📝 forms.py                   # Formularios personalizados
├── 🗃️ models.py                 # Modelos de datos
├── 📡 signals.py                 # Señales Django
├── 🧪 tests.py                   # Tests unitarios
├── 🌐 urls.py                    # Configuración de URLs
└── 👀 views.py                   # Lógica de vistas
```

## 🎯 Funcionalidades Detalladas

### 🎬 Gestión de Películas
- **Crear**: Añadir nuevas películas con información completa
- **Listar**: Visualizar catálogo completo con paginación
- **Buscar**: Motor de búsqueda por título y filtros
- **Editar**: Modificar información existente (usuarios autenticados)
- **Eliminar**: Borrado seguro con confirmación

### 🎭 Administración de Directores
- **Perfiles completos**: Información biográfica y filmografía
- **Relaciones**: Vinculación automática con películas
- **Búsqueda**: Localizar directores por nombre

### 🎪 Categorización por Géneros
- **Gestión de géneros**: Crear y administrar categorías
- **Filtrado**: Búsqueda de películas por género
- **Estadísticas**: Visualizar distribución por categorías

## 🔧 Configuración Avanzada

### Variables de Entorno (Opcional)
```bash
# Crear archivo .env en la raíz del proyecto
SECRET_KEY=tu_clave_secreta_aqui
DEBUG=True
ALLOWED_HOSTS=localhost,127.0.0.1
```

### Configuración de Base de Datos Personalizada
```python
# En settings.py para usar PostgreSQL (opcional)
DATABASES = {
    'default': {
        'ENGINE': 'django.db.backends.postgresql',
        'NAME': 'academia_cinema',
        'USER': 'tu_usuario',
        'PASSWORD': 'tu_password',
        'HOST': 'localhost',
        'PORT': '5432',
    }
}
```

## 🧪 Testing

### Ejecutar Tests
```bash
python manage.py test
```

### Coverage (Opcional)
```bash
pip install coverage
coverage run --source='.' manage.py test
coverage report
```

## 📦 Deployment

### Preparación para Producción
```bash
# Instalar dependencias adicionales
pip install gunicorn whitenoise

# Configurar archivos estáticos
python manage.py collectstatic

# Variables de entorno para producción
DEBUG=False
ALLOWED_HOSTS=tu-dominio.com
```

## 🤝 Contribuciones

Este es un proyecto académico, pero las contribuciones son bienvenidas:

1. Fork del repositorio
2. Crear rama feature (`git checkout -b feature/nueva-funcionalidad`)
3. Commit cambios (`git commit -am 'Agregar nueva funcionalidad'`)
4. Push a la rama (`git push origin feature/nueva-funcionalidad`)
5. Crear Pull Request

## 📚 Recursos Adicionales

- [Documentación Django](https://docs.djangoproject.com/)
- [Bootstrap Documentation](https://getbootstrap.com/docs/)
- [Python Best Practices](https://docs.python.org/3/tutorial/)
- [Git Guidelines](https://git-scm.com/doc)

## 📄 Licencia

Este proyecto está bajo la Licencia MIT - ver el archivo [LICENSE](LICENSE) para más detalles.

## 🏆 Reconocimientos

- **Coderhouse**: Por la excelente formación en desarrollo Python
- **Django Community**: Por el framework robusto y documentación
- **Bootstrap Team**: Por el framework CSS que facilita el desarrollo

## 👨‍💻 Autor

Lisandro Akira Kokuba

---

### 📊 Estadísticas del Proyecto

![Líneas de Código](https://img.shields.io/badge/Líneas_de_Código-2000+-blue)
![Commits](https://img.shields.io/badge/Commits-50+-green)
![Funcionalidades](https://img.shields.io/badge/Funcionalidades-15+-purple)

### 🎯 Objetivos de Aprendizaje Alcanzados

- ✅ Desarrollo web full-stack con Django
- ✅ Implementación de patrones MVC
- ✅ Gestión de bases de datos relacionales
- ✅ Autenticación y autorización de usuarios
- ✅ Desarrollo de interfaces responsivas
- ✅ Integración de frameworks CSS
- ✅ Control de versiones con Git
- ✅ Documentación de proyectos

---

*¡Gracias por explorar Academia Cinematográfica! 🎬*



