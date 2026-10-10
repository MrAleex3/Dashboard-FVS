# FVS Monitor

Aplicación web para el monitoreo en tiempo real de estaciones de prueba industriales. Lee los logs generados por los equipos de manufactura, los procesa de forma concurrente y presenta estadísticas de rendimiento en una interfaz web.

![Python](https://img.shields.io/badge/Python-3.9%2B-blue)
![Flask](https://img.shields.io/badge/Framework-Flask-green)
![Server](https://img.shields.io/badge/Server-Waitress-red)
![Status](https://img.shields.io/badge/Status-Production-success)

## Características

- Monitoreo en tiempo real, con actualización automática cada 3 segundos.
- Procesamiento concurrente mediante `ThreadPoolExecutor` (20 hilos) y servidor WSGI Waitress, para atender varias rutas de logs y usuarios al mismo tiempo.
- Lectura por copia temporal, que permite leer archivos que otro proceso está escribiendo sin interferir en el proceso.
- Trazabilidad histórica: buscador para rastrear el historial de un número de serie en los últimos 7 días.
- Estadísticas de calidad: cálculo automático de yield (Pass/Fail), top 10 de fallas más frecuentes y detección de rachas de fallas consecutivas.
- Interfaz con tema oscuro y notificaciones tipo toast para las alertas.

## Requisitos

- Windows 10 o superior.
- Acceso a las rutas de red definidas en `rutas.ini`.

## Estructura del proyecto

```text
fvs-monitor/
├── server.exe          # servidor y worker
├── rutas.ini           # rutas de red a monitorear
├── requirements.txt    # dependencias del proyecto
├── static/             # archivos CSS y JS locales
│   ├── css/
│   └── js/
└── logs/               # carpeta para logs
```

## Interfaz

![Vista principal](https://github.com/user-attachments/assets/a341b43c-41d9-4e8a-b332-4130fa7e2b7d)

![Estadísticas de calidad](https://github.com/user-attachments/assets/914579ad-9832-413f-85a2-be80fe91a271)

## Autor

Alejandro Espinoza
Foxconn México
