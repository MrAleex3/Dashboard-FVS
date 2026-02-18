# FVS Monitor

**FVS Monitor** es una solucion de alto rendimiento para el monitoreo en tiempo real de estaciones de prueba industriales. Diseñado para leer logs generados por equipos de manufactura, procesarlos concurrentemente y presentar estadisticas de rendimiento (Yield, Top Fallas) en una interfaz web moderna.

![Python](https://img.shields.io/badge/Python-3.9%2B-blue)
![Flask](https://img.shields.io/badge/Framework-Flask-green)
![Server](https://img.shields.io/badge/Server-Waitress-red)
![Status](https://img.shields.io/badge/Status-Production-success)

## 🚀 Funcionalidades

-   **Monitoreo en Tiempo Real:** Actualizacion automatica cada 3 segundos.
-   **Alto Rendimiento (Multi-Hilo):** Utiliza `ThreadPoolExecutor` (20 hilos) y servidor WSGI `Waitress` para manejar multiples rutas de logs y usuarios simultaneos.
-   **Lectura "Snapshot" Segura:** Implementa un sistema de copias temporales para leer archivos que estan siendo escritos activamente por otros procesos.
-   **Trazabilidad Historica:** Buscador integrado para rastrear el historial de un numero de serie en los ultimos 7 días.
-   **Estadísticas de Calidad:**
    -   Calculo automatico de Yield (Pass/Fail).
    -   Top 10 de fallas mas recurrentes.
    -   Deteccion de "Racha de Fallas" consecutivas.
-   **Interfaz** Tema oscuro, notificaciones "Toast" para alertas.

## 📷 Interfaz
<img width="1343" height="624" alt="image" src="https://github.com/user-attachments/assets/a341b43c-41d9-4e8a-b332-4130fa7e2b7d" />

<img width="1233" height="539" alt="image" src="https://github.com/user-attachments/assets/914579ad-9832-413f-85a2-be80fe91a271" />


## 🧰 Requisitos

- Windows 10 o superior.
- Acceso a las rutas de red establecidas en `modelo.ini`.


## 📂 Estructura del Proyecto

```text
fvs-monitor/
├── server.exe          # servidor y worker
├── rutas.ini           # Configuracion de carpetas a monitorear
├── requirements.txt    # Dependencias del proyecto
├── static/             # Archivos CSS y JS locales
│   ├── css/
│   └── js/
└── logs/               # Carpeta para logs
```

## Autor

**Jose Alejandro**  
Foxconn México · Proyecto personal para portafolio
