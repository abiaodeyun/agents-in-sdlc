---
title: "Lección 12 - Despliega el sitio con GitHub Pages"
description: "Usa la aplicación GitHub Copilot para configurar un flujo de trabajo de Pages, revisar su pull request y verificar que Space Quiz está disponible."
authors:
  - jamesmontemagno
lastUpdated: 2026-10-12
---

Publica Space Quiz en GitHub Pages para que todo el mundo pueda acceder a él. Copilot puede preparar el flujo de trabajo y guiarte durante el despliegue, pero tú eres responsable de revisar los cambios y confirmar que el sitio está disponible.

En esta lección:

- pedirás a Copilot que configure el despliegue en GitHub Pages.
- revisarás el flujo de trabajo y el pull request antes de fusionarlo.
- seguirás el despliegue y verificarás el sitio publicado.

## Escenario

Space Quiz ya está en un repositorio de GitHub, pero otras personas aún necesitan una forma sencilla de probarlo. Publicar el sitio de un solo archivo con GitHub Pages lo hace accesible mediante una URL pública sin añadir un servidor ni una dependencia del entorno de ejecución.

## Pide a Copilot que despliegue el sitio

En la sesión de la aplicación Copilot para `space-quiz`, envía este prompt:

```plaintext
Enable GitHub Pages for this repository. Create a GitHub Actions workflow that builds the website if needed and deploys it to GitHub Pages. Add a README describing the app and how to run it locally if one does not already exist. Create a pull request with these changes and merge it after required checks pass. Monitor the deployment until it succeeds, then report the final URL of the live website. If you lack permission to enable Pages or merge, tell me exactly what I need to approve or do; do not report success until the site is live.
```

![Diagrama de tres fases: un pull request de space-quiz fusionado; una ejecución correcta de GitHub Actions para desplegar el sitio, con los pasos Build website, Upload artifact y Deploy to Pages; y Space Quiz disponible en yourname.github.io/space-quiz/.](../../../_images/first-steps-app-pages-deploy.svg)

> [!WARNING]
> Este prompt pide al agente que cree y fusione un pull request y que cambie la configuración de Pages del repositorio. Antes de continuar, revisa el diff, los permisos de despliegue y las solicitudes de aprobación de GitHub.

## Revisa el flujo de trabajo y verifica el despliegue

1. Confirma que el README solo se ha añadido si el repositorio aún no tenía uno.
2. Revisa los cambios del pull request, incluidos los pasos de compilación y despliegue del flujo de trabajo.
3. Fusiona el pull request solo cuando se hayan superado las comprobaciones obligatorias.
4. Sigue la ejecución de despliegue de GitHub Actions hasta que se complete correctamente.
5. Abre la URL indicada y confirma que se carga Space Quiz.

Si el agente no puede habilitar Pages o fusionar el pull request, sigue las instrucciones concretas que te proporcione. No des la tarea por terminada hasta que el despliegue se complete correctamente y se cargue el sitio publicado.

## Resumen y siguientes pasos

Space Quiz ya está disponible como sitio publicado y has verificado el despliegue en lugar de depender del informe del agente. Continúa con la [lección 13: repaso y próximos pasos][next-lesson].

[next-lesson]: ../13-review/
