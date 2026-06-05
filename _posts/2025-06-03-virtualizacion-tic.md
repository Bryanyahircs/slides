---
title: Solución Estratificada de Problemas en TIC
layout: post
permalink: /virtualizacion-tic/
slides:
 - slide-data: |
     <div style="padding:0 5%;">
       <h2 style="font-size:1.3em; font-weight:bold; margin:0 0 0.3em;">Solución Estratificada de Problemas en TIC</h2>
       <p style="font-size:0.8em; margin:0 0 0.5em;">Virtualización: Conceptos y Estrategias</p>
       <hr style="border-color:rgba(255,255,255,0.3); margin:0.4em 0;">
       <p style="font-size:0.72em; margin:0.3em 0;"><b>Bryan Yahir Colorado Salazar</b> &nbsp;·&nbsp; Matrícula: 230300798</p>
       <p style="font-size:0.68em; margin:0.2em 0;"><em>Procesamiento de datos en la nube</em></p>
       <p style="font-size:0.68em; margin:0.2em 0;"><em>Ingeniería en Datos e Inteligencia Organizacional</em></p>
     </div>
   background: "#1a1a2e"

 - slide-data: |
     <div style="padding:0 5%;">
       <h2 style="font-size:1.05em; font-weight:bold; margin:0 0 0.4em;">1.1 Solución Estratificada en TIC</h2>
       <ul style="font-size:0.7em; text-align:left; line-height:1.7; margin:0; padding-left:1.2em;">
         <li>Divide un sistema complejo en <b>capas de abstracción</b>.</li>
         <li>Cada capa gestiona recursos sin exponer sus detalles internos.</li>
         <li>La <b>virtualización</b> abstrae el hardware para que múltiples entornos lógicos coexistan en el mismo equipo.</li>
         <li>Base de servicios en la nube: IaaS, PaaS, SaaS.</li>
       </ul>
     </div>
   background: "#16213e"

 - slide-data: |
     <div style="padding:0 5%;">
       <h2 style="font-size:1.0em; font-weight:bold; margin:0 0 0.35em;">1.1.a — Virtualización por Interpretación Pura</h2>
       <p style="font-size:0.67em; text-align:left; margin:0 0 0.25em;"><b>Descripción:</b> Cada instrucción del invitado se lee, traduce y ejecuta <em>una a una</em> sin contacto directo con el hardware real.</p>
       <p style="font-size:0.67em; text-align:left; margin:0 0 0.15em;"><b>Características:</b></p>
       <ul style="font-size:0.64em; text-align:left; line-height:1.55; margin:0 0 0.25em; padding-left:1.2em;">
         <li>Aislamiento total entre huésped y anfitrión.</li>
         <li>Compatible con arquitecturas distintas (x86 ↔ ARM).</li>
         <li>Alto costo de rendimiento por cada instrucción.</li>
       </ul>
       <p style="font-size:0.67em; text-align:left; margin:0 0 0.1em;"><b>Casos de uso:</b> Emulación de consolas retro, pruebas de compatibilidad multi-arquitectura, entornos educativos.</p>
       <p style="font-size:0.67em; text-align:left; margin:0;"><b>Ejemplos:</b> QEMU (modo puro), Bochs, DOSBox.</p>
     </div>
   background: "#0f3460"

 - slide-data: |
     <div style="padding:0 5%;">
       <h2 style="font-size:1.0em; font-weight:bold; margin:0 0 0.35em;">1.1.b — Virtualización por Recompilación Dinámica</h2>
       <p style="font-size:0.67em; text-align:left; margin:0 0 0.25em;"><b>Descripción:</b> El código invitado se traduce en <em>bloques</em> (Binary Translation) y se almacena en caché para reutilizarse, no instrucción por instrucción.</p>
       <p style="font-size:0.67em; text-align:left; margin:0 0 0.15em;"><b>Características:</b></p>
       <ul style="font-size:0.64em; text-align:left; line-height:1.55; margin:0 0 0.25em; padding-left:1.2em;">
         <li>Mucho más rápida que la interpretación pura.</li>
         <li>No requiere soporte especial del CPU (sin VT-x / AMD-V).</li>
         <li>Penalización solo en la primera ejecución de cada bloque.</li>
       </ul>
       <p style="font-size:0.67em; text-align:left; margin:0 0 0.1em;"><b>Casos de uso:</b> VMs en equipos sin Intel VT-x, entornos de desarrollo y prueba.</p>
       <p style="font-size:0.67em; text-align:left; margin:0;"><b>Ejemplos:</b> QEMU (TCG), VMware Workstation legacy, VirtualPC.</p>
     </div>
   background: "#533483"

 - slide-data: |
     <div style="padding:0 5%;">
       <h2 style="font-size:1.0em; font-weight:bold; margin:0 0 0.35em;">1.1.c — Hipervisión Bare Metal (Tipo 1)</h2>
       <p style="font-size:0.67em; text-align:left; margin:0 0 0.25em;"><b>Descripción:</b> El hipervisor se instala <em>directamente sobre el hardware físico</em>, sin sistema operativo anfitrión de por medio.</p>
       <p style="font-size:0.67em; text-align:left; margin:0 0 0.15em;"><b>Características:</b></p>
       <ul style="font-size:0.64em; text-align:left; line-height:1.55; margin:0 0 0.25em; padding-left:1.2em;">
         <li>Máximo rendimiento: acceso casi nativo al hardware.</li>
         <li>Alto aislamiento entre máquinas virtuales.</li>
         <li>Requiere soporte de CPU: Intel VT-x o AMD-V.</li>
       </ul>
       <p style="font-size:0.67em; text-align:left; margin:0 0 0.1em;"><b>Casos de uso:</b> Centros de datos, nube pública (AWS, Azure, GCP), alta disponibilidad.</p>
       <p style="font-size:0.67em; text-align:left; margin:0;"><b>Ejemplos:</b> VMware ESXi, Microsoft Hyper-V, KVM, Xen.</p>
     </div>
   background: "#c84b31"

 - slide-data: |
     <div style="padding:0 5%;">
       <h2 style="font-size:1.0em; font-weight:bold; margin:0 0 0.4em;">Comparativa General</h2>
       <table style="font-size:0.62em; width:100%; border-collapse:collapse;">
         <thead>
           <tr style="background:rgba(255,255,255,0.2);">
             <th style="padding:6px 8px; border:1px solid rgba(255,255,255,0.3); text-align:left;">Tipo</th>
             <th style="padding:6px 8px; border:1px solid rgba(255,255,255,0.3);">Velocidad</th>
             <th style="padding:6px 8px; border:1px solid rgba(255,255,255,0.3);">Compatibilidad</th>
             <th style="padding:6px 8px; border:1px solid rgba(255,255,255,0.3); text-align:left;">Uso ideal</th>
           </tr>
         </thead>
         <tbody>
           <tr>
             <td style="padding:6px 8px; border:1px solid rgba(255,255,255,0.3);">Interpretación pura</td>
             <td style="padding:6px 8px; border:1px solid rgba(255,255,255,0.3); text-align:center;">🐢 Baja</td>
             <td style="padding:6px 8px; border:1px solid rgba(255,255,255,0.3); text-align:center;">✅ Máxima</td>
             <td style="padding:6px 8px; border:1px solid rgba(255,255,255,0.3);">Emulación multi-arq.</td>
           </tr>
           <tr style="background:rgba(255,255,255,0.08);">
             <td style="padding:6px 8px; border:1px solid rgba(255,255,255,0.3);">Recompilación dinámica</td>
             <td style="padding:6px 8px; border:1px solid rgba(255,255,255,0.3); text-align:center;">🚗 Media</td>
             <td style="padding:6px 8px; border:1px solid rgba(255,255,255,0.3); text-align:center;">✅ Alta</td>
             <td style="padding:6px 8px; border:1px solid rgba(255,255,255,0.3);">Dev / Test sin VT-x</td>
           </tr>
           <tr>
             <td style="padding:6px 8px; border:1px solid rgba(255,255,255,0.3);">Bare metal (Tipo 1)</td>
             <td style="padding:6px 8px; border:1px solid rgba(255,255,255,0.3); text-align:center;">🚀 Alta</td>
             <td style="padding:6px 8px; border:1px solid rgba(255,255,255,0.3); text-align:center;">⚠️ Req. VT-x</td>
             <td style="padding:6px 8px; border:1px solid rgba(255,255,255,0.3);">Producción / Nube</td>
           </tr>
         </tbody>
       </table>
     </div>
   background: "#2d4a22"

 - slide-data: |
     <div style="padding:0 5%;">
       <h2 style="font-size:1.05em; font-weight:bold; margin:0 0 0.4em;">Conclusión</h2>
       <ul style="font-size:0.7em; text-align:left; line-height:1.7; margin:0 0 0.4em; padding-left:1.2em;">
         <li><b>Interpretación pura</b> → máxima compatibilidad, mínimo rendimiento.</li>
         <li><b>Recompilación dinámica</b> → equilibrio entre compatibilidad y velocidad.</li>
         <li><b>Bare metal (Tipo 1)</b> → máximo rendimiento para producción.</li>
       </ul>
       <p style="font-size:0.68em;">Cada enfoque tiene su lugar según el contexto: emulación, desarrollo o infraestructura crítica en la nube.</p>
     </div>
   background: "#1a1a2e"
---
{% for slide in page.slides %}
<section data-background="{% if slide.background %}{{slide.background}}{% else %}{{page.background}}{% endif %}">
  {{ slide.slide-data }}
</section>
{% endfor %}
