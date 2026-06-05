---
title: Pizza as a Service 2.0
layout: post
permalink: /pizza-as-a-service/

slides:
 - title: Pizza as a Service 2.0
   slide-data: |
     <p>Modelos de Servicio en la Nube</p>
     <br>
     <p><b>Por: Bryan Yahir Colorado Salazar</b></p>
     <p><em>Ingeniería en Datos e Inteligencia Organizacional</em></p>
   background: "#2c3e50"
     
 - title: ¿Qué es Pizza as a Service 2.0?
   slide-data: |
     <p>Es una evolución de la clásica analogía de la pizza para explicar <b>Cloud Computing</b>.</p>
     <p>Añade arquitecturas modernas como <b>CaaS</b> (Contenedores) y <b>FaaS</b> (Funciones serverless).</p>
   background: "#e74c3c"
   
 - title: 1. On-Premises (Hecho en casa)
   slide-data: |
     <ul style="font-size: 0.7em; text-align: left;">
       <li><b>Descripción:</b> Gestionas TODO. Pones la cocina, el gas, la masa y la horneas.</li>
       <li><b>Ventajas:</b> Control total y privacidad.</li>
       <li><b>Desventajas:</b> Alto costo inicial y mantenimiento propio.</li>
       <li><b>Ejemplos:</b> Servidores físicos en UniCaribe, o tu script de Python en tu Raspberry Pi 5.</li>
     </ul>
   background: "#f1c40f"
   
 - title: 2. IaaS (Take and Bake)
   slide-data: |
     <ul style="font-size: 0.7em; text-align: left;">
       <li><b>Descripción:</b> Te dan la infraestructura. Usas una cocina compartida, tú armas la pizza.</li>
       <li><b>Ventajas:</b> Escalabilidad rápida, sin comprar hardware físico.</li>
       <li><b>Desventajas:</b> Tú administras el Sistema Operativo y la red.</li>
       <li><b>Ejemplos:</b> AWS EC2, Google Compute Engine.</li>
     </ul>
   background: "#3498db"
   
 - title: 3. CaaS (Traes pizza)
   slide-data: |
     <ul style="font-size: 0.7em; text-align: left;">
       <li><b>Descripción:</b> El proveedor gestiona los clústeres. Tú llevas tu contenedor listo.</li>
       <li><b>Ventajas:</b> Portabilidad y alta eficiencia en despliegues.</li>
       <li><b>Desventajas:</b> Curva de aprendizaje en orquestación.</li>
       <li><b>Ejemplos:</b> Google Kubernetes Engine, o desplegar la app CunGo usando Docker.</li>
     </ul>
   background: "#9b59b6"
   
 - title: 4. PaaS (Pizza a domicilio)
   slide-data: |
     <ul style="font-size: 0.7em; text-align: left;">
       <li><b>Descripción:</b> Plataforma completa. Tú pones tu código y base de datos.</li>
       <li><b>Ventajas:</b> Te enfocas 100% en programar sin tocar servidores.</li>
       <li><b>Desventajas:</b> Menos control sobre la infraestructura (vendor lock-in).</li>
       <li><b>Ejemplos:</b> Heroku, Google App Engine.</li>
     </ul>
   background: "#2ecc71"
   
 - title: 5. FaaS (Pizzería con amigos)
   slide-data: |
     <ul style="font-size: 0.7em; text-align: left;">
       <li><b>Descripción:</b> Ejecutas fragmentos de código bajo demanda (Serverless).</li>
       <li><b>Ventajas:</b> Cobro por milisegundo, auto-escalado desde cero.</li>
       <li><b>Desventajas:</b> Retrasos en la primera ejecución (Cold starts).</li>
       <li><b>Ejemplos:</b> AWS Lambda, Google Cloud Functions.</li>
     </ul>
   background: "#1abc9c"

 - title: 6. SaaS (Cenando fuera)
   slide-data: |
     <ul style="font-size: 0.7em; text-align: left;">
       <li><b>Descripción:</b> Aplicación lista para usar. Tú solo consumes.</li>
       <li><b>Ventajas:</b> Sin mantenimiento, acceso inmediato vía web.</li>
       <li><b>Desventajas:</b> Control casi nulo sobre el código base.</li>
       <li><b>Ejemplos:</b> GitHub, Gmail, Webjeda Slides.</li>
     </ul>
   background: "#e67e22"
---

{% for slide in page.slides %}
<section data-background="{% if slide.background %}{{slide.background}}{% else %}{{page.background}}{% endif %}">
  <h1>{{slide.title}}</h1>
  {{ slide.slide-data }}
</section>
{% endfor %}
