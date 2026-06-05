---
layout: slide
permalink: /presentation-1/
title: Pizza as a Service 2.0
description: Tarea 997 Modelos en la Nube
theme: night
transition: convex
slides:

  - title: Tarea 997
    slide-data: |
      <h2>Pizza as a Service 2.0</h2>
      <p>Modelos de Servicio en la Nube</p>
      <br>
      <p><b>Por: Bryan Yahir Colorado Salazar</b></p>
      <p><em>Ingeniería en Datos e Inteligencia Organizacional</em></p>

  - title: ¿Qué es Pizza as a Service 2.0?
    slide-data: |
      <p>Es una evolución de la clásica analogía de la pizza para explicar <b>Cloud Computing</b>.</p>
      <br>
      <p>Añade arquitecturas modernas como <b>CaaS</b> (Contenedores) y <b>FaaS</b> (Funciones serverless).</p>

  - title: 1. On-Premises (Hecho en casa)
    slide-data: |
      <ul style="font-size: 0.8em; text-align: left;">
        <li><b>Descripción:</b> Gestionas TODO. Pones la cocina, el gas, la masa y la horneas.</li>
        <li><b>Ventajas:</b> Control total y privacidad.</li>
        <li><b>Desventajas:</b> Alto costo (CAPEX) y mantenimiento propio.</li>
        <li><b>Ejemplos:</b> Servidores físicos en la universidad, o tu propio script de Python corriendo localmente en una Raspberry Pi 5.</li>
      </ul>

  - title: 2. IaaS (Take and Bake)
    slide-data: |
      <ul style="font-size: 0.8em; text-align: left;">
        <li><b>Descripción:</b> Te dan la infraestructura. Usas una cocina compartida, pero tú armas la pizza.</li>
        <li><b>Ventajas:</b> Escalabilidad, evitas comprar hardware físico.</li>
        <li><b>Desventajas:</b> Tú administras el Sistema Operativo y la red.</li>
        <li><b>Ejemplos:</b> AWS EC2, Google Compute Engine.</li>
      </ul>

  - title: 3. CaaS (Traes pizza para hornear)
    slide-data: |
      <ul style="font-size: 0.8em; text-align: left;">
        <li><b>Descripción:</b> El proveedor gestiona los clústeres. Tú solo llevas tu contenedor listo (Docker).</li>
        <li><b>Ventajas:</b> Portabilidad y alta eficiencia de recursos.</li>
        <li><b>Desventajas:</b> Curva de aprendizaje en orquestación.</li>
        <li><b>Ejemplos:</b> Google Kubernetes Engine, o desplegar un proyecto como CunGo separado en microservicios.</li>
      </ul>

  - title: 4. PaaS (Pizza a domicilio)
    slide-data: |
      <ul style="font-size: 0.8em; text-align: left;">
        <li><b>Descripción:</b> Te dan la plataforma completa. Tú solo pones tu código y base de datos. Pides la pizza hecha.</li>
        <li><b>Ventajas:</b> Te enfocas 100% en programar sin tocar servidores.</li>
        <li><b>Desventajas:</b> Menos control subyacente (dependencia de marca / vendor lock-in).</li>
        <li><b>Ejemplos:</b> Heroku, Google App Engine.</li>
      </ul>

  - title: 5. FaaS (Pizzería con amigos)
    slide-data: |
      <ul style="font-size: 0.8em; text-align: left;">
        <li><b>Descripción:</b> Ejecutas fragmentos de código bajo demanda (Serverless).</li>
        <li><b>Ventajas:</b> Cobro exacto por milisegundo, auto-escalado desde cero.</li>
        <li><b>Desventajas:</b> Retrasos en primera ejecución (cold starts).</li>
        <li><b>Ejemplos:</b> AWS Lambda, Google Cloud Functions.</li>
      </ul>

  - title: 6. SaaS (Cenando fuera)
    slide-data: |
      <ul style="font-size: 0.8em; text-align: left;">
        <li><b>Descripción:</b> Aplicación lista para usar. Vas a una fiesta donde te sirven todo, tú solo consumes.</li>
        <li><b>Ventajas:</b> Sin mantenimiento, acceso inmediato vía web.</li>
        <li><b>Desventajas:</b> Control casi nulo sobre el código de la plataforma.</li>
        <li><b>Ejemplos:</b> GitHub, Gmail, Webjeda Slides.</li>
      </ul>
---
