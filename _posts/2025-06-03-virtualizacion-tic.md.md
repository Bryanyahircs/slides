---
title: Solución Estratificada de Problemas en TIC
layout: post
permalink: /virtualizacion-tic/
slides:
 - title: Solución Estratificada de Problemas en TIC
   slide-data: |
     <p>Virtualización: Conceptos y Estrategias</p>
     <br>
     <p><b>Por: Bryan Yahir Colorado Salazar</b></p>
     <p><b>Matrícula: 230300798</b></p>
     <p><em>Materia: Procesamiento de datos en la nube</em></p>
     <p><em>Ingeniería en Datos e Inteligencia Organizacional</em></p>
   background: "#1a1a2e"

 - title: 1.1 Solución Estratificada de Problemas en TIC
   slide-data: |
     <p>La <b>solución estratificada</b> consiste en dividir un sistema complejo en capas o niveles de abstracción.</p>
     <br>
     <p>En TIC, permite que cada capa gestione recursos sin exponer los detalles internos a las capas superiores.</p>
     <br>
     <p>La <b>virtualización</b> es el pilar de esta estrategia: abstrae el hardware físico para que múltiples entornos lógicos coexistan sobre el mismo equipo.</p>
   background: "#16213e"

 - title: 1.1.a Virtualización por Interpretación Pura
   slide-data: |
     <h3 style="font-size:0.8em; margin-bottom:0.4em;">📌 Descripción</h3>
     <p style="font-size:0.65em; text-align:left;">Cada instrucción del sistema invitado es <b>leída, traducida y ejecutada una a una</b> por el software virtual, sin contacto directo con el hardware real.</p>
     <h3 style="font-size:0.8em; margin-top:0.6em; margin-bottom:0.4em;">⚙️ Características</h3>
     <ul style="font-size:0.65em; text-align:left;">
       <li>Total aislamiento entre huésped y anfitrión.</li>
       <li>Compatible con arquitecturas distintas (x86 emulando ARM, por ejemplo).</li>
       <li><b>Alto costo de rendimiento</b>: cada instrucción paga la penalización de interpretación.</li>
     </ul>
   background: "#0f3460"

 - title: 1.1.a — Casos de Uso y Ejemplos
   slide-data: |
     <h3 style="font-size:0.8em; margin-bottom:0.4em;">🎯 Casos de uso</h3>
     <ul style="font-size:0.65em; text-align:left;">
       <li>Emular consolas antiguas (NES, SNES, PS1) en hardware moderno.</li>
       <li>Ejecutar software de arquitectura diferente (ARM en x86) para pruebas de compatibilidad.</li>
       <li>Entornos educativos donde se estudian arquitecturas distintas.</li>
     </ul>
     <h3 style="font-size:0.8em; margin-top:0.6em; margin-bottom:0.4em;">💡 Ejemplos</h3>
     <ul style="font-size:0.65em; text-align:left;">
       <li><b>QEMU</b> en modo emulación pura.</li>
       <li><b>Bochs</b>: emulador x86 por software.</li>
       <li><b>DOSBox</b>: emula el entorno de MS-DOS completo.</li>
     </ul>
   background: "#0f3460"

 - title: 1.1.b Virtualización por Recompilación Dinámica
   slide-data: |
     <h3 style="font-size:0.8em; margin-bottom:0.4em;">📌 Descripción</h3>
     <p style="font-size:0.65em; text-align:left;">El código del sistema invitado se <b>traduce en bloques</b> (Binary Translation) y se almacena en caché para reutilizarse. No instrucción por instrucción, sino por fragmentos optimizados.</p>
     <h3 style="font-size:0.8em; margin-top:0.6em; margin-bottom:0.4em;">⚙️ Características</h3>
     <ul style="font-size:0.65em; text-align:left;">
       <li>Mucho más rápida que la interpretación pura.</li>
       <li>Los bloques ya traducidos se reutilizan directamente.</li>
       <li>Permite virtualizar sistemas operativos completos <b>sin soporte especial del CPU</b>.</li>
       <li>Penalización solo en la primera ejecución de cada bloque.</li>
     </ul>
   background: "#533483"

 - title: 1.1.b — Casos de Uso y Ejemplos
   slide-data: |
     <h3 style="font-size:0.8em; margin-bottom:0.4em;">🎯 Casos de uso</h3>
     <ul style="font-size:0.65em; text-align:left;">
       <li>Correr Windows XP dentro de macOS sin hardware de virtualización dedicado.</li>
       <li>Máquinas virtuales en equipos sin extensiones Intel VT-x / AMD-V.</li>
       <li>Ambientes de desarrollo y prueba donde el rendimiento es aceptable.</li>
     </ul>
     <h3 style="font-size:0.8em; margin-top:0.6em; margin-bottom:0.4em;">💡 Ejemplos</h3>
     <ul style="font-size:0.65em; text-align:left;">
       <li><b>VMware Workstation</b> (versiones antiguas sin VT-x).</li>
       <li><b>QEMU</b> con TCG (Tiny Code Generator).</li>
       <li><b>VirtualPC</b> de Microsoft (para CPU no compatibles).</li>
     </ul>
   background: "#533483"

 - title: 1.1.c Virtualización por Hipervisión (Bare Metal)
   slide-data: |
     <h3 style="font-size:0.8em; margin-bottom:0.4em;">📌 Descripción</h3>
     <p style="font-size:0.65em; text-align:left;">El <b>hipervisor Tipo 1</b> se instala <em>directamente sobre el hardware físico</em>, sin sistema operativo anfitrión de por medio. Controla los recursos y ofrece VMs a los sistemas invitados.</p>
     <h3 style="font-size:0.8em; margin-top:0.6em; margin-bottom:0.4em;">⚙️ Características</h3>
     <ul style="font-size:0.65em; text-align:left;">
       <li>Máximo rendimiento: acceso casi nativo al hardware.</li>
       <li>Alta seguridad: cada VM está totalmente aislada.</li>
       <li>Requiere soporte de CPU (Intel VT-x / AMD-V).</li>
       <li>Ideal para centros de datos y entornos de producción críticos.</li>
     </ul>
   background: "#c84b31"

 - title: 1.1.c — Casos de Uso y Ejemplos
   slide-data: |
     <h3 style="font-size:0.8em; margin-bottom:0.4em;">🎯 Casos de uso</h3>
     <ul style="font-size:0.65em; text-align:left;">
       <li>Centros de datos empresariales que consolidan decenas de servidores.</li>
       <li>Infraestructura de nube pública (AWS, Azure, GCP usan hipervisores bare metal).</li>
       <li>Ambientes de alta disponibilidad con migración en vivo de VMs.</li>
     </ul>
     <h3 style="font-size:0.8em; margin-top:0.6em; margin-bottom:0.4em;">💡 Ejemplos</h3>
     <ul style="font-size:0.65em; text-align:left;">
       <li><b>VMware ESXi</b>: líder en virtualización empresarial.</li>
       <li><b>Microsoft Hyper-V</b>: integrado en Windows Server.</li>
       <li><b>KVM</b> (Kernel-based Virtual Machine): usado en Linux y la nube de AWS.</li>
       <li><b>Xen</b>: base de Amazon EC2 en sus primeras generaciones.</li>
     </ul>
   background: "#c84b31"

 - title: Comparativa General
   slide-data: |
     <table style="font-size:0.6em; width:100%; border-collapse:collapse;">
       <thead>
         <tr style="background:rgba(255,255,255,0.2);">
           <th style="padding:6px; border:1px solid rgba(255,255,255,0.3);">Tipo</th>
           <th style="padding:6px; border:1px solid rgba(255,255,255,0.3);">Velocidad</th>
           <th style="padding:6px; border:1px solid rgba(255,255,255,0.3);">Compatibilidad</th>
           <th style="padding:6px; border:1px solid rgba(255,255,255,0.3);">Uso principal</th>
         </tr>
       </thead>
       <tbody>
         <tr>
           <td style="padding:6px; border:1px solid rgba(255,255,255,0.3);">Interpretación pura</td>
           <td style="padding:6px; border:1px solid rgba(255,255,255,0.3);">🐢 Baja</td>
           <td style="padding:6px; border:1px solid rgba(255,255,255,0.3);">✅ Máxima</td>
           <td style="padding:6px; border:1px solid rgba(255,255,255,0.3);">Emulación multi-arq.</td>
         </tr>
         <tr style="background:rgba(255,255,255,0.1);">
           <td style="padding:6px; border:1px solid rgba(255,255,255,0.3);">Recompilación dinámica</td>
           <td style="padding:6px; border:1px solid rgba(255,255,255,0.3);">🚗 Media</td>
           <td style="padding:6px; border:1px solid rgba(255,255,255,0.3);">✅ Alta</td>
           <td style="padding:6px; border:1px solid rgba(255,255,255,0.3);">Dev/Test sin VT-x</td>
         </tr>
         <tr>
           <td style="padding:6px; border:1px solid rgba(255,255,255,0.3);">Hipervisión (bare metal)</td>
           <td style="padding:6px; border:1px solid rgba(255,255,255,0.3);">🚀 Alta</td>
           <td style="padding:6px; border:1px solid rgba(255,255,255,0.3);">⚠️ Req. VT-x</td>
           <td style="padding:6px; border:1px solid rgba(255,255,255,0.3);">Producción / Nube</td>
         </tr>
       </tbody>
     </table>
   background: "#2d4a22"

 - title: Conclusión
   slide-data: |
     <p>La <b>virtualización estratificada</b> resuelve el problema de aprovechar al máximo el hardware disponible.</p>
     <br>
     <ul style="font-size:0.7em; text-align:left;">
       <li><b>Interpretación pura</b> → máxima compatibilidad, mínimo rendimiento.</li>
       <li><b>Recompilación dinámica</b> → equilibrio entre compatibilidad y velocidad.</li>
       <li><b>Bare metal (Hipervisor Tipo 1)</b> → máximo rendimiento para producción.</li>
     </ul>
     <br>
     <p style="font-size:0.75em;">Cada enfoque tiene su lugar según el contexto: emulación, desarrollo o infraestructura crítica en la nube.</p>
   background: "#1a1a2e"
---
{% for slide in page.slides %}
<section data-background="{% if slide.background %}{{slide.background}}{% else %}{{page.background}}{% endif %}">
  <h1>{{slide.title}}</h1>
  {{ slide.slide-data }}
</section>
{% endfor %}
