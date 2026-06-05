---
title: Solución Estratificada de Problemas en TIC
layout: post
permalink: /virtualizacion-tic/
slides:
title: " "
slide-data: |
<h2 style="font-size:1.4em; font-weight:bold; margin-bottom:0.3em;">Solución Estratificada de Problemas en TIC</h2>
     <p style="font-size:0.85em;">Virtualización: Conceptos y Estrategias</p>
     <br>
     <p style="font-size:0.75em;"><b>Bryan Yahir Colorado Salazar</b> · 230300798</p>
     <p style="font-size:0.7em;"><em>Procesamiento de datos en la nube</em></p>
     <p style="font-size:0.7em;"><em>Ingeniería en Datos e Inteligencia Organizacional</em></p>
   background: "#1a1a2e"
title: " "
slide-data: |
<h2 style="font-size:1.1em; font-weight:bold; margin-bottom:0.5em;">1.1 Solución Estratificada en TIC</h2>
     <ul style="font-size:0.72em; text-align:left; line-height:1.6;">
       <li>Divide un sistema complejo en <b>capas de abstracción</b>.</li>
       <li>Cada capa gestiona recursos sin exponer sus detalles internos.</li>
       <li>La <b>virtualización</b> es el pilar: abstrae el hardware para que múltiples entornos lógicos coexistan en el mismo equipo.</li>
     </ul>
   background: "#16213e"
title: " "
slide-data: |
<h2 style="font-size:1em; font-weight:bold; margin-bottom:0.4em;">1.1.a — Interpretación Pura</h2>
     <p style="font-size:0.68em; text-align:left; margin-bottom:0.3em;"><b>Descripción:</b> Cada instrucción del invitado se lee, traduce y ejecuta <em>una a una</em> sin contacto directo con el hardware.</p>
     <p style="font-size:0.68em; text-align:left; margin-bottom:0.2em;"><b>Características:</b></p>
     <ul style="font-size:0.65em; text-align:left; line-height:1.5;">
       <li>Aislamiento total huésped–anfitrión.</li>
       <li>Compatible con arquitecturas distintas (x86 ↔ ARM).</li>
       <li>Alto costo de rendimiento por instrucción.</li>
     </ul>
     <p style="font-size:0.68em; text-align:left; margin-top:0.3em;"><b>Casos de uso:</b> emulación de consolas retro, pruebas de compatibilidad multi-arq.</p>
     <p style="font-size:0.68em; text-align:left;"><b>Ejemplos:</b> QEMU (modo puro), Bochs, DOSBox.</p>
   background: "#0f3460"
title: " "
slide-data: |
<h2 style="font-size:1em; font-weight:bold; margin-bottom:0.4em;">1.1.b — Recompilación Dinámica</h2>
     <p style="font-size:0.68em; text-align:left; margin-bottom:0.3em;"><b>Descripción:</b> El código invitado se traduce en <em>bloques</em> (Binary Translation) y se almacena en caché para reutilizarse.</p>
     <p style="font-size:0.68em; text-align:left; margin-bottom:0.2em;"><b>Características:</b></p>
     <ul style="font-size:0.65em; text-align:left; line-height:1.5;">
       <li>Mucho más rápida que la interpretación pura.</li>
       <li>No requiere soporte especial del CPU (sin VT-x).</li>
       <li>Penalización solo en la primera ejecución de cada bloque.</li>
     </ul>
     <p style="font-size:0.68em; text-align:left; margin-top:0.3em;"><b>Casos de uso:</b> VMs en equipos sin Intel VT-x / AMD-V, entornos de dev/test.</p>
     <p style="font-size:0.68em; text-align:left;"><b>Ejemplos:</b> QEMU (TCG), VMware Workstation legacy, VirtualPC.</p>
   background: "#533483"
title: " "
slide-data: |
<h2 style="font-size:1em; font-weight:bold; margin-bottom:0.4em;">1.1.c — Hipervisión Bare Metal (Tipo 1)</h2>
     <p style="font-size:0.68em; text-align:left; margin-bottom:0.3em;"><b>Descripción:</b> El hipervisor se instala <em>directamente sobre el hardware</em>, sin SO anfitrión de por medio.</p>
     <p style="font-size:0.68em; text-align:left; margin-bottom:0.2em;"><b>Características:</b></p>
     <ul style="font-size:0.65em; text-align:left; line-height:1.5;">
       <li>Máximo rendimiento: acceso casi nativo al hardware.</li>
       <li>Alto aislamiento entre VMs.</li>
       <li>Requiere CPU con Intel VT-x o AMD-V.</li>
     </ul>
     <p style="font-size:0.68em; text-align:left; margin-top:0.3em;"><b>Casos de uso:</b> centros de datos, nube pública, alta disponibilidad.</p>
     <p style="font-size:0.68em; text-align:left;"><b>Ejemplos:</b> VMware ESXi, Microsoft Hyper-V, KVM, Xen.</p>
   background: "#c84b31"
title: " "
slide-data: |
<h2 style="font-size:1em; font-weight:bold; margin-bottom:0.5em;">Comparativa</h2>
     <table style="font-size:0.62em; width:100%; border-collapse:collapse;">
       <thead>
         <tr style="background:rgba(255,255,255,0.2);">
           <th style="padding:5px; border:1px solid rgba(255,255,255,0.3);">Tipo</th>
           <th style="padding:5px; border:1px solid rgba(255,255,255,0.3);">Velocidad</th>
           <th style="padding:5px; border:1px solid rgba(255,255,255,0.3);">Compatibilidad</th>
           <th style="padding:5px; border:1px solid rgba(255,255,255,0.3);">Uso ideal</th>
         </tr>
       </thead>
       <tbody>
         <tr>
           <td style="padding:5px; border:1px solid rgba(255,255,255,0.3);">Interpretación pura</td>
           <td style="padding:5px; border:1px solid rgba(255,255,255,0.3);">🐢 Baja</td>
           <td style="padding:5px; border:1px solid rgba(255,255,255,0.3);">✅ Máxima</td>
           <td style="padding:5px; border:1px solid rgba(255,255,255,0.3);">Emulación multi-arq.</td>
         </tr>
         <tr style="background:rgba(255,255,255,0.08);">
           <td style="padding:5px; border:1px solid rgba(255,255,255,0.3);">Recompilación dinámica</td>
           <td style="padding:5px; border:1px solid rgba(255,255,255,0.3);">🚗 Media</td>
           <td style="padding:5px; border:1px solid rgba(255,255,255,0.3);">✅ Alta</td>
           <td style="padding:5px; border:1px solid rgba(255,255,255,0.3);">Dev/Test sin VT-x</td>
         </tr>
         <tr>
           <td style="padding:5px; border:1px solid rgba(255,255,255,0.3);">Bare metal</td>
           <td style="padding:5px; border:1px solid rgba(255,255,255,0.3);">🚀 Alta</td>
           <td style="padding:5px; border:1px solid rgba(255,255,255,0.3);">⚠️ Req. VT-x</td>
           <td style="padding:5px; border:1px solid rgba(255,255,255,0.3);">Producción / Nube</td>
         </tr>
       </tbody>
     </table>
   background: "#2d4a22"
title: " "
slide-data: |
<h2 style="font-size:1.1em; font-weight:bold; margin-bottom:0.5em;">Conclusión</h2>
     <ul style="font-size:0.72em; text-align:left; line-height:1.7;">
       <li><b>Interpretación pura</b> → máxima compatibilidad, mínimo rendimiento.</li>
       <li><b>Recompilación dinámica</b> → equilibrio entre compatibilidad y velocidad.</li>
       <li><b>Bare metal (Tipo 1)</b> → máximo rendimiento para producción.</li>
     </ul>
     <p style="font-size:0.7em; margin-top:0.6em;">Cada enfoque tiene su lugar según el contexto: emulación, desarrollo o infraestructura crítica en la nube.</p>
   background: "#1a1a2e"
---
{% for slide in page.slides %}
<section data-background="{% if slide.background %}{{slide.background}}{% else %}{{page.background}}{% endif %}">
  <h1>{{slide.title}}</h1>
  {{ slide.slide-data }}
</section>
{% endfor %}
