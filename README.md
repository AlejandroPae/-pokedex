# PokeDex en Azure Static Web Apps

Despliegue de la aplicación **PokeDex** (Angular) para **Pueblo Paleta Inc.**, realizado en la nube pública **Microsoft Azure** usando el servicio **Azure Static Web Apps**.

-   **URL pública:** https://lively-water-0e141011e.5.azurestaticapps.net/
-   **Repositorio:** https://github.com/AlejandroPae/pokedex
-   **Autor:** Alejandro Paez Perez

----------

## 1. ¿Por qué Azure Static Web Apps?

La PokeDex es una aplicación Angular que, una vez compilada, son solo archivos estáticos. Azure Static Web Apps sirve este tipo de aplicaciones, se integra con GitHub (cada `git push` despliega automáticamente) y tiene un plan **Free** suficiente para este trabajo. Además entrega HTTPS por defecto y permite configurar encabezados de seguridad.

----------

## 2. Crear la cuenta en Azure

1.  Entra a https://azure.microsoft.com/free/students/ 
2.  Presiona **Start free** / **Activate now**.
3.  Inicia sesión con tu **correo institucional** 
4.  Verifica tu condición de estudiante (en Azure for Students) siguiendo las instrucciones en pantalla.
5.  Completa el perfil (país, nombre, teléfono) y acepta los términos.
6.  Al terminar, entra al portal: https://portal.azure.com
7.  Comprueba en **Suscripciones** que aparece la suscripción activa 
----------

## 3. Configuración inicial en la nube

### 3.1 Crear un grupo de recursos

1.  En el portal, busca **Grupos de recursos** (Resource groups) → **Crear**.
2.  Suscripción: la que acabas de activar.
3.  Nombre: Pokedex.
4.  Región: West u 2.
5.  **Revisar y crear** → **Crear**.

### 3.2 Crear la Static Web App

1.  En el buscador del portal escribe **Static Web Apps** → **Crear**.
2.  **Datos básicos:**
    -   Suscripción y grupo de recursos: los del paso anterior.
    -   Nombre:  Pokedex-Alejnadro.
    -   Tipo de plan: **Free**.
    -   Región: West U 2
3.  **Detalles de implementación:**
    -   Origen: **GitHub**.
    -   Inicia sesión con GitHub y autoriza a Azure.
    -   Organización/usuario: `AlejandroPae`.
    -   Repositorio: `pokedex`.
    -   Rama: `main`.
4.  **Detalles de compilación:**
    -   Valor preestablecido: **Angular**.
    -   Ubicación de la aplicación (`app_location`): `/`
    -   Ubicación de salida (`output_location`): `dist/pokedex-angular`
5.  **Revisar y crear** → **Crear**.


----------

## 4. Verificación

1.  Abre la URL del recurso 
2.  En GitHub, pestaña **Actions**, verifica que el workflow **Azure Static Web Apps CI/CD** termina en verde.
----------

## 5. Resultado de seguridad

El sitio fue escaneado en https://securityheaders.com con calificación **A**.


Los detalles de la configuración están en Despliegue.md

----------