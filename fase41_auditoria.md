# PHP2Shell — Auditoría técnica, fase 41

## Evidencia local
- PHP 8.5.11 con Apache mod_php.
- RCE local confirmada como www-data.
- SHA-256 del exploit verificado.
- Configuración original restaurada.

## Dependencias observadas
- La filtración inicial falló con display_errors=Off.
- Los offsets remotos no están confirmados.
- La prueba de RCE requiere acceso al contenedor.

## Limitaciones del cliente HTTP
- No implementa TLS.
- Usa puerto 80 de forma predeterminada.
- La detección automática puede enviar GET.
- El lector puede devolver respuestas parciales.
- El analizador de Set-Cookie exige un formato específico.

## Estado del desafío remoto
- RCE remota: no demostrada.
- Lectura de /flag: pendiente.
- Evasión del WAF: no iniciada.

## Próxima actividad
Evaluación de compatibilidad y seguridad del transporte
en un entorno local controlado.
