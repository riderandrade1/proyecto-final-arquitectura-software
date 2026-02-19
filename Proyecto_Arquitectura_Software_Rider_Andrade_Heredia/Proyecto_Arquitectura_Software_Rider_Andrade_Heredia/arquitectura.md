# Arquitectura del Sistema

## Flujo de Datos
El cliente móvil se conecta vía HTTPS al API Gateway.
El Gateway redirige a microservicios.
Los microservicios utilizan PostgreSQL y Redis.

## Diagrama

```mermaid
graph LR
A[Mobile App] --> B[API Gateway]
B --> C[Microservicio Cuentas]
B --> D[Microservicio Transacciones]
C --> E[(PostgreSQL)]
D --> E
C --> F[(Redis)]
D --> F
