# PHP2Shell — Auditoría técnica, fase 42

## Laboratorio local
- Contenedor Apache operativo.
- PHP 8.5.11.
- GET /index.php: HTTP 200.
- POST ordinario: HTTP 200.
- Puerto publicado: 127.0.0.1:8085.

## Transporte del exploit
- Implementa sockets TCP sin TLS.
- No interpreta correctamente el esquema HTTPS.
- La detección automática puede utilizar GET.
- Construye solicitudes multipart manualmente.
- Puede devolver respuestas parciales.
- El análisis de Set-Cookie depende del formato.

## Riesgos de ejecución
- Perfil PHP 8.5.11 con campo de 24 MiB.
- Operaciones de agotamiento de memoria.
- Rotación de trabajadores Apache.
- Reintentos que pueden aumentar la carga.

## Limitaciones remotas
- Arquitectura del servidor no verificada.
- Offsets del binario remoto no verificados.
- Configuración interna de PHP no verificada.
- RCE remota no demostrada.
- Lectura de /flag pendiente.

## Conclusión
La RCE local y la conectividad HTTP están demostradas
en el laboratorio. La compatibilidad con el desafío
remoto sigue sin verificarse.
