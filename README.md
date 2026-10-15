# ALLYAGENTIA — sitio provisional en Render

Este proyecto contiene exclusivamente una página HTML estática con el logotipo ALLYAGENTIA.
La imagen va incrustada en `public/index.html`, por lo que no requiere archivos adicionales ni base de datos.

## Despliegue en Render

1. Crear un repositorio nuevo de GitHub llamado `allyagentia-web`.
2. Subir la carpeta `public` con `index.html` dentro (conservar la estructura de carpetas).
3. En https://dashboard.render.com seleccionar **New → Static Site**, conectar el repositorio y su rama principal.
4. Nombre del servicio: `allyagentia-web`.
5. Build command: `echo "HTML listo"`.
6. Publish directory: `public`.
7. Confirmar el despliegue y comprobar que la URL `...onrender.com` muestre el logotipo.
8. En el servicio, ir a Settings → Custom Domains, y agregar el dominio principal y `www` si se desea.
9. En el proveedor DNS del dominio (si es Hostinger, Dominio → DNS/Nameservers) modificar SOLO los registros web que correspondan, de acuerdo con los valores mostrados por Render.
10. Volver a Render a verificar el dominio y esperar a que el certificado HTTPS esté activo.

## Configuración DNS habitual con Hostinger

- A    @     216.24.57.1    (referencia oficial de Render para dominios raíz si no hay ANAME/ALIAS)
- CNAME www  <subdominio-del-sitio>.onrender.com    (reemplazar por el subdominio real asignado por Render)

IMPORTANTE: confirmar la zona DNS activa antes de editar. NO borrar los registros MX, SPF, DKIM o DMARC del correo. No cambiar nameservers por este motivo. Si la configuración real difiere, seguir la pantalla de Render.

Documentación oficial:
- https://render.com/docs/static-sites
- https://render.com/docs/custom-domains
- https://render.com/docs/configure-other-dns
