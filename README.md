# XONICAL - Agente IA para Optimización de Horarios Universitarios

```
================================================================================
                          XONICAL v3.0
              Agente Inteligente para Horarios Universitarios
              Integración con MisProfesores.com
              
                    Desarrollado por: XONIDU
                  Darian Alberto Camacho Salas
                  Oscar Rodolfo Barragan Perez
================================================================================
```

## 🎯 ¿Qué es XONICAL?

**XONICAL** es un agente de IA especializado en la optimización de horarios universitarios. Su misión es guiar al estudiante paso a paso para crear el horario perfecto, combinando:

1. **Datos extraídos de PDFs** de horarios oficiales
2. **Análisis de calificaciones** de profesores desde **MisProfesores.com**
3. **Preferencias personalizadas** del usuario
4. **Reglas de optimización** inteligente

---

## 🤖 Accede al Agente XONICAL

Puedes interactuar con XONICAL directamente a través del siguiente enlace:

🔗 **[XONICAL en DeepSeek](https://chat.deepseek.com/share/vzxt5qu3ivpsuup6e5)**

¡Solo copia el prompt y comienza a generar tu horario!

---

## ✨ Características Principales

- 🔍 **Búsqueda automática** de profesores en MisProfesores.com
- 📊 **Análisis detallado** de perfiles de profesores (calificación, dificultad, recomendación)
- 📅 **Generación de 5 opciones** de horario optimizado
- ⚙️ **Configuración de preferencias** (jerarquía, traslapes, horarios fijos)
- 🧪 **Gestión de laboratorios** en el horario
- 📂 **Exportación a Excel/CSV** en formatos estándar o específicos por universidad
- 🔄 **Modificaciones y reajustes** en tiempo real
- 📋 **Reportes en PDF** del horario generado

---

## 📋 Requisitos

- Acceso a un modelo de IA (DeepSeek, Claude, Gemini, etc.)
- Conexión a internet (para búsquedas en MisProfesores.com)
- PDF de horarios oficial de tu universidad (opcional)

---

## 🚀 Cómo Usar XONICAL

### Paso 1: Acceder al Agente

Visita el enlace compartido: **[XONICAL en DeepSeek](https://chat.deepseek.com/share/vzxt5qu3ivpsuup6e5)**

O copia el contenido de `prompt_xonical.txt` y pégalo en tu modelo de IA preferido.

### Paso 2: Iniciar Conversación

El agente comenzará a guiarte paso a paso:

```
¡Hola! Soy XONICAL, tu asistente inteligente para crear horarios universitarios. 
Estoy potenciado por IA y puedo analizar calificaciones de MisProfesores.com 
para darte el mejor horario posible. ¿Cómo te llamas?
```

### Paso 3: Proporcionar Información

Responde a las preguntas del agente sobre:

- Tu nombre, universidad y semestre
- PDF de horarios o ingreso manual
- Materias que deseas cursar
- Preferencias de horario (jerarquía, traslapes, etc.)

### Paso 4: Analizar Profesores

El agente buscará automáticamente a tus profesores en MisProfesores.com y te mostrará:

- Calificación General (0-10)
- Nivel de Dificultad (0-10)
- Tasa de Recomendación (%)
- Etiquetas clave
- Comentarios de estudiantes

### Paso 5: Seleccionar Horario

El agente generará 5 opciones de horario optimizado. Tú seleccionas la que mejor se adapte a tus necesidades.

### Paso 6: Exportar

Descarga tu horario en Excel/CSV en el formato que necesites.

---

## 🔍 Protocolo de Búsqueda en MisProfesores.com

XONICAL utiliza un protocolo estricto para buscar profesores:

### Formato de Búsqueda
```
"[NOMBRE_COMPLETO_DEL_PROFESOR] [UNIVERSIDAD] MisProfesores.com"
```

### Regla de Oro
**SIEMPRE se elige el PRIMER resultado de búsqueda** que aparezca en MisProfesores.com.

---

## 📊 Formato de Análisis de Profesores

```
## ESTADISTICAS DE [NOMBRE PROFESOR] - [UNIVERSIDAD]

### METRICAS GENERALES
| Metrica | Puntuacion / Porcentaje |
|---------|------------------------|
| Calidad General | [X.X]/10 |
| Nivel de Dificultad | [X.X]/10 |
| Tasa de Recomendacion | [XX]% |
| Total de Evaluaciones | [X] |

### INFORMACION INSTITUCIONAL
- Universidad: [Nombre]
- Departamento/Facultad: [Nombre]
- Ciudad: [Ciudad]
- Materias principales: [Lista]

### ETIQUETAS CLAVE
| Etiqueta | Votos |
|----------|-------|
| [Etiqueta 1] | [X] |
| [Etiqueta 2] | [X] |
| [Etiqueta 3] | [X] |

### ANALISIS DE COMENTARIOS
#### Opiniones Positivas
- "[Comentario 1]"
- "[Comentario 2]"

#### Opiniones Negativas
- "[Comentario 1]"
- "[Comentario 2]"

### RESUMEN DEL PERFIL
[Analisis completo del estilo de enseñanza, ventajas, desventajas y recomendacion]

### EVALUACION DEL AGENTE
| Criterio | Evaluacion |
|----------|------------|
| Aprenderas bien? | SI/NO/DUDOSO |
| Es facil pasar? | SI/NO/DUDOSO |
| Recomendado? | SI/NO/DUDOSO |
| Motivo: | [Texto breve] |
```

---

## 📂 Formato de Exportación

### Estructura Estándar (Excel/CSV)
```
| Clave | Materia | Grupo | Profesor | Calificacion | Dificultad | Dia | Hora Inicio | Hora Fin | Aula | Creditos | Tipo |
```

### Adaptación por Universidad
- **UDG:** Formato SIIAU
- **UNAM:** Formato DGAE
- **ITESO:** Formato específico
- **TEC:** Formato Tec
- **Otra:** El agente preguntará y adaptará

---

## ⚙️ Preferencias Configurables

### Jerarquía de Prioridades (1-8)
1. Profesor con mejor calificación en MisProfesores.com
2. Profesor con menor nivel de dificultad
3. Profesor que mejor enseña según comentarios
4. Horario compacto (menos días presenciales)
5. Horario con espacios libres estratégicos
6. Horario balanceado (dificultad distribuida)
7. Cercanía entre aulas
8. Conservar grupos con amigos/compañeros

### Reglas de Traslapes
- Permitir o no traslapes
- Número máximo de traslapes (0-3)
- Traslapes en materias obligatorias (Si/No)
- Traslapes en materias optativas (Si/No)

### Horarios Fijos
- Días y horas ocupados
- Día libre preferido
- Preferencia de horario (mañana/tarde/noche)
- Límite de horas por día

---

## 🛠️ Comandos Especiales

| Comando | Descripción |
|---------|-------------|
| `/ayuda` | Mostrar comandos disponibles |
| `/profesor [nombre]` | Buscar un profesor específico |
| `/materias` | Ver lista de materias seleccionadas |
| `/preferencias` | Ver configuración actual |
| `/reiniciar` | Empezar de nuevo |
| `/exportar [formato]` | Exportar horario (excel/csv/pdf) |
| `/salir` | Terminar sesión |

---

## 📊 Clasificación de Profesores

### Por Calidad
| Categoría | Calificación |
|-----------|--------------|
| EXCELENTE | >= 8.5 |
| BUENO | 7.5 - 8.4 |
| REGULAR | 6.5 - 7.4 |
| MALO | < 6.5 |

### Por Dificultad
| Categoría | Dificultad | Recomendación |
|-----------|------------|---------------|
| BARCO | <= 3.0 | < 60% |
| EQUILIBRADO | 3.1 - 6.0 | 60-80% |
| EXIGENTE | > 6.0 | > 80% |

---

## 📁 Estructura del Proyecto

```
xonical/
├── README.md                 # Este archivo
└── prompt_xonical.txt        # Prompt completo del agente XONICAL
```

---

## 📌 Reglas de Conducta del Agente

### ✅ DEBE HACER
- Siempre preguntar antes de generar el horario final
- Mostrar las 5 mejores opciones con estadísticas
- Permitir modificaciones y reajustes
- Ofrecer exportación en múltiples formatos
- Guardar historial para futuras referencias
- Elegir SIEMPRE el primer resultado de MisProfesores.com
- Extraer TODOS los datos disponibles del perfil

### ❌ NO DEBE HACER
- Inventar datos que no estén en el perfil
- Omitir información negativa de profesores
- Recomendar profesores sin datos suficientes
- Generar horarios sin confirmar preferencias
- Ignorar las reglas de traslapes del usuario

---

## 🤖 Plataformas Soportadas

- **DeepSeek** (Enlace directo: [XONICAL en DeepSeek](https://chat.deepseek.com/share/vzxt5qu3ivpsuup6e5))
- **Claude**
- **Gemini**
- Cualquier modelo de IA que acepte prompts extensos

---

## 👨‍💻 Créditos

**Desarrollador:** Darian Alberto Camacho Salas  
**Alias:** XONIDU  
**Contacto:** xonidu@gmail.com  
**Versión:** 3.0 - Integración con MisProfesores.com  
**Fecha:** 2026  

```
================================================================================
           "La organización inteligente es el primer paso hacia el éxito"
           
                      © 2026 XONIDU - Todos los derechos reservados
================================================================================
```

---

## 📜 Licencia

Este software es de uso libre para fines educativos y académicos.  
Para uso comercial, contactar al desarrollador.

---

**¡Gracias por usar XONICAL!** 🎓

