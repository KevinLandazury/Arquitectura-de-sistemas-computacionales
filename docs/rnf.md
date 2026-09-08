# Requerimientos no funcionales

| # | Atributo | Metrica | Umbral | Condicion de carga | Verificacion | Consecuencia si no se cumple |
|---|---|---|---|---|---|---|
| 1 | Rendimiento | p95 de latencia | menor a 400 ms | 200 usuarios concurrentes | Prueba de carga | El usuario abandona la reserva |
| 2 | Disponibilidad | Uptime mensual | 99.9% | Operacion continua 24/7 | Monitoreo sintético | Pérdida de transacciones |
| 3 | Seguridad | Cifrado en tránsito | TLS 1.3 | Peticiones HTTP | Auditoría de tráfico | Vulnerabilidad de interceptación |

## Escenarios completos

### Escenario 1
- **Fuente:** Usuario final
- **Estímulo:** Envío de formulario de reserva
- **Artefacto:** API REST de reservas
- **Entorno:** Operación normal con carga pico
- **Respuesta:** Procesar la transacción y responder la confirmación
- **Medida:** Latencia p95 menor a 400 ms
