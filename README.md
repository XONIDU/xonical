# 📅 XONICAL v2.0 - Organizador de Eventos, Proyectos, Congresos y Artículos con IA y Web Scraping

```
╔══════════════════════════════════════════════════════════════════════════════╗
║                           XONICAL v2.0                                       ║
║              Organizador Inteligente con IA y Web Scraping                   ║
║                                                                              ║
║                    Desarrollado por: Darian Alberto                          ║
║                           Camacho Salas                                      ║
║                              (XONIDU)                                        ║
╚══════════════════════════════════════════════════════════════════════════════╝
```

## 🎯 ¿Qué es XONICAL?

**XONICAL** es un sistema web completo para la organización de eventos académicos, proyectos de investigación, congresos y artículos científicos. Integra inteligencia artificial (Gemini) con múltiples API keys y web scraping para automatizar la creación y análisis de contenido.

- **🤖 IA Gemini** con múltiples API keys y rotación automática
- **🌐 Web Scraping** para análisis de convocatorias y URLs
- **📅 Calendario visual** de eventos con vista mensual y diaria
- **📋 Gestión de Eventos, Proyectos, Congresos y Artículos**
- **📱 Acceso mediante código QR** desde cualquier dispositivo
- **📄 Generación de reportes PDF** de todos los módulos

## ✨ Características

- **📅 Calendario visual** de eventos con vista mensual y diaria
- **📋 Gestión de Eventos** con campos: nombre, día, hora, categoría, descripción, ubicación
- **📊 Gestión de Proyectos** de investigación
- **🎯 Gestión de Congresos** académicos
- **📝 Gestión de Artículos** científicos (NUEVO)
- **🤖 IA Gemini** con múltiples API keys y rotación automática
- **🌐 Web Scraping** integrado para análisis de convocatorias y URLs
- **📱 Acceso mediante código QR** desde cualquier dispositivo
- **🔐 Login único** para administradores (acceso público solo lectura)
- **📄 Generación de reportes PDF** de todos los módulos
- **🔍 Buscador global** en toda la plataforma
- **💬 Chat con IA** integrado para consultas
- **⚡ Creación de eventos con IA** a partir de descripciones
- **📎 Gestión de links, participantes y requisitos** para cada entidad

## 📦 Instalación Rápida

```bash
git clone https://github.com/XONIDU/xonical.git
cd xonical
python start.py
```

Abre tu navegador en: **http://localhost:5420**

### Instalación manual (dependencias)

```bash
pip install flask requests qrcode[pil] Pillow beautifulsoup4 weasyprint pandas
```

## Opción 2 – Comando xoninstall (recomendado para futuras herramientas XONI)

Agrega la siguiente función a tu `~/.bashrc` con un solo comando:

```bash
echo 'xoninstall() { if [ -z "$1" ]; then echo "Uso: xoninstall <repo>"; echo "Ej: xoninstall xoniran"; else git clone "https://github.com/XONIDU/$1.git"; fi; }' >> ~/.bashrc && source ~/.bashrc && echo "✅ Listo. Usa: xoninstall xonicli"
```

Luego simplemente escribe:

```bash
xoninstall xonical
cd xonical
pip install -r requisitos.txt
python start.py
```

> **Nota:** Esta función te servirá para instalar cualquier otra herramienta futura de XONIDU (por ejemplo `xoninstall xonical`).

## Opción 3 – Script para Windows (INICIAR_XONICAL.bat)

Guarda el siguiente código como `INICIAR_XONICAL.bat` en la raíz del proyecto:

```batch
@echo off
title XONICAL 2026 - Organizador con IA y Web Scraping
color 0A

:: ============================================================
:: SOLICITAR PERMISOS DE ADMINISTRADOR
:: ============================================================
net session >nul 2>&1
if %errorlevel% neq 0 (
    echo Solicitando permisos de administrador...
    echo.
    echo Set UAC = CreateObject^("Shell.Application"^) > "%temp%\getadmin.vbs"
    echo UAC.ShellExecute "%~s0", "", "", "runas", 1 >> "%temp%\getadmin.vbs"
    "%temp%\getadmin.vbs"
    del "%temp%\getadmin.vbs"
    exit /B
)

:: ============================================================
:: EJECUTAR start.py CON PERMISOS DE ADMINISTRADOR
:: ============================================================
cls
echo ============================================================
echo           XONICAL 2026 - Organizador con IA
echo              (Modo Administrador)
echo ============================================================
echo.
echo [OK] Permisos de administrador obtenidos
echo.
echo Iniciando XONICAL...
echo.
echo [INFO] Sistema de organizacion de Eventos, Proyectos, Congresos y Articulos
echo [INFO] Con IA Gemini y Web Scraping integrado
echo [INFO] Accede a: http://localhost:5420
echo [INFO] Admin: http://localhost:5420/login
echo [INFO] QR: http://localhost:5420/qr
echo.
echo Presiona Ctrl+C para detener el servidor
echo ============================================================
echo.

python start.py

pause
```

### Ejecución en Windows:

1. Haz doble clic en `INICIAR_XONICAL.bat`
2. Acepta los permisos de administrador si se solicitan
3. El servidor se iniciará en **http://localhost:5420**

## 💻 Uso

### 1. Configuración inicial

Al ejecutar por primera vez, se te pedirá configurar:

- **Nombre de la organización** (ej: XONICAL)
- **Contraseña de administrador**

### 2. Credenciales por defecto

| Rol | Usuario/Organización | Contraseña |
|-----|---------------------|------------|
| Admin | XONICAL | admin123 |

> **Importante:** Cambia la contraseña por defecto después de la primera configuración.

### 3. Acceder al sistema

```
Local:    http://localhost:5420
Admin:    http://localhost:5420/login
QR:       http://localhost:5420/qr
```

### 4. Módulos principales

#### 📅 Calendario
- Vista mensual con eventos
- Navegación entre meses
- Días con eventos resaltados
- Vista detallada por día

#### 📋 Eventos
- Creación manual o con IA
- Campos: nombre, fecha, hora, categoría, descripción, ubicación
- Gestión de links de convocatoria
- Participantes y requisitos

#### 📊 Proyectos
- Seguimiento de proyectos de investigación
- Responsables, fechas, estado
- Participantes y requisitos

#### 🎯 Congresos
- Organización de congresos académicos
- Fechas, lugar, organizador
- Participantes y requisitos

#### 📝 Artículos
- Gestión de publicaciones científicas
- Autores, revista, DOI, palabras clave
- Resumen y enlace a PDF
- Autores detallados con ORCID

### 5. 🤖 IA Gemini

- Múltiples API keys con rotación automática
- Chat interactivo con contexto
- Creación automática de eventos
- Generación de artículos desde descripciones o URLs

#### Crear evento con IA:
1. Ve a Eventos → Nuevo Evento → "Generar con IA"
2. Describe el evento (ej: "Conferencia sobre IA el 15 de mayo")
3. La IA extrae automáticamente: nombre, fecha, hora, categoría, etc.
4. Revisa y guarda

#### Generar artículo con IA:
1. Ve a Artículos → Nuevo Artículo → "Generar con IA"
2. Opción A: Describe el artículo
3. Opción B: Ingresa una URL para web scraping
4. La IA genera la estructura completa

### 6. 🌐 Web Scraping

El sistema puede analizar cualquier URL y extraer:
- Título de la página
- Metadatos (descripción)
- Texto principal
- Fechas encontradas
- Emails
- Teléfonos
- Enlaces (clasificados por tipo)

**Tipos de análisis:**
- **Básico:** Solo contenido HTML
- **Completo:** Extrae fechas, emails, teléfonos
- **Convocatoria:** Enfocado en fechas límite y requisitos

### 7. 📄 Reportes PDF

Genera reportes profesionales de:
- Eventos
- Proyectos
- Congresos
- Artículos
- Calendario mensual

## 📁 Estructura del Proyecto

```
xonical/
├── start.py                 # Lanzador con autoreinicio
├── xonical.py               # Aplicación principal
├── requisitos.txt           # Dependencias
├── README.md                # Documentación
├── INICIAR_XONICAL.bat      # Script para Windows (opcional)
├── keys.txt                 # API keys de Gemini (opcional)
│
├── data/                    # Datos del sistema (CSV)
│   ├── config.csv
│   ├── eventos.csv
│   ├── proyectos.csv
│   ├── congresos.csv
│   ├── articulos.csv
│   ├── participantes.csv
│   ├── requisitos.csv
│   ├── links.csv
│   └── web_scraping.csv
│
├── static/                  # Archivos estáticos
│   └── qrcodes/             # Códigos QR generados
│
└── templates/               # Plantillas HTML
    ├── base.html
    ├── configurar.html
    ├── login.html
    ├── dashboard.html
    ├── calendario.html
    ├── calendario_dia.html
    ├── eventos.html
    ├── evento_detalle.html
    ├── admin_evento_form.html
    ├── proyectos.html
    ├── proyecto_detalle.html
    ├── congresos.html
    ├── congreso_detalle.html
    ├── articulos.html
    ├── articulo_detalle.html
    ├── admin_articulo_form.html
    ├── web_scraping.html
    ├── web_scraping_detalle.html
    ├── ia_chat.html
    ├── qr.html
    ├── buscar.html
    ├── reporte_pdf.html
    ├── reporte_pdf_calendario.html
    ├── 404.html
    └── 500.html
```

## 🔧 Solución de Problemas

| Problema | Solución |
|----------|----------|
| Puerto 5420 en uso | `lsof -ti:5420 \| xargs kill -9` (Linux/Mac) o cambia el puerto en `xonical.py` |
| No hay API keys configuradas | Crea `keys.txt` y agrega tus keys de Gemini (una por línea) |
| WeasyPrint no instalado | `sudo apt-get install python3-pip python3-cffi python3-brotli libpango-1.0-0 libharfbuzz0b libpangoft2-1.0-0` (Linux) |
| Dependencias faltantes | `pip install -r requisitos.txt` |
| Error de web scraping | Verifica conexión a internet o usa modo "básico" |
| QR no se muestra | `pip install qrcode[pil]` |

## 📊 Fuentes de Búsqueda (Web Scraping)

- **Google Books API** – libros académicos
- **Open Library** – biblioteca digital abierta
- **CrossRef** – DOIs y metadatos de artículos
- **arXiv** – preprints de física, matemáticas, informática
- **Wikipedia** – API de búsqueda en español
- **DuckDuckGo** – búsqueda general (último recurso)

## ❌ Lo que XONICAL NO hace

- ❌ No requiere API keys para funcionar (solo para IA Gemini)
- ❌ No exporta a JSON (solo PDF y CSV)
- ❌ No tiene sincronización automática con Google Calendar (próximamente)
- ❌ No es una app móvil nativa (próximamente)

## 📋 Requisitos

```txt
Flask==2.3.3
qrcode[pil]==7.4.2
Pillow==10.1.0
requests==2.31.0
beautifulsoup4==4.12.2
weasyprint==60.1
pandas==2.0.3
```

## 🔌 API Endpoints

| Endpoint | Método | Descripción |
|----------|--------|-------------|
| `/` | GET | Interfaz web principal |
| `/calendario` | GET | Vista del calendario |
| `/eventos` | GET | Lista de eventos |
| `/proyectos` | GET | Lista de proyectos |
| `/congresos` | GET | Lista de congresos |
| `/articulos` | GET | Lista de artículos |
| `/ia` | GET | Chat con IA |
| `/ia/consultar` | POST | Consultar a la IA |
| `/web-scraping` | GET | Interfaz de web scraping |
| `/web-scraping/analizar` | POST | Analizar URL |
| `/reporte/pdf/<tipo>` | GET | Generar reporte PDF |
| `/qr` | GET | Código QR de acceso |
| `/buscar` | GET | Búsqueda global |

## 👤 Créditos

**Desarrollador:** XONIDU (Darian Alberto Camacho Salas)  
**Organización:** XONIDU  

**Tecnologías utilizadas:**  
Flask, Gemini API, BeautifulSoup4, WeasyPrint, QRCode, Pillow, Pandas

## 📜 Licencia

MIT License

---

**Hecho con ❤️ por XONIDU**

**© 2026 XONIDU - Todos los derechos reservados**
