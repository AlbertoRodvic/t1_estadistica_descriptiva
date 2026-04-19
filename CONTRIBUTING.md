# Contributing Guide

Gracias por contribuir a este proyecto.

## Alcance

Este repositorio contiene un trabajo académico reproducible basado en notebooks y un script de carga de datos. Las contribuciones deben mejorar claridad, mantenibilidad o reproducibilidad sin alterar el objetivo analítico del trabajo.

## Requisitos Previos

1. Usar Python 3.12+.
2. Crear y activar entorno virtual.
3. Instalar dependencias:

```bash
python -m pip install -r requirements.txt
```

## Flujo Recomendado

1. Crea una rama desde `main` con nombre descriptivo.
2. Realiza cambios pequeños y atómicos.
3. Escribe commits claros en imperativo.
4. Abre una pull request con contexto y validación.

## Estilo De Cambios

- Respeta la estructura actual de carpetas y nombres.
- No incluyas refactors no relacionados.
- No subas archivos temporales, caches ni checkpoints.
- Si cambias documentación, verifica rutas y comandos.

## Checklist Antes De Abrir PR

1. `requirements.txt` refleja dependencias reales usadas.
2. README y documentación siguen siendo consistentes.
3. El flujo de ejecución de notebooks se mantiene reproducible.
4. No se han añadido archivos locales accidentales.

## Pull Request

Incluye en la descripción:

- Resumen breve de cambios.
- Motivación del cambio.
- Validación realizada.
- Impacto esperado (si aplica).

Al enviar una contribución, aceptas que se distribuya bajo la licencia del repositorio (MIT).
