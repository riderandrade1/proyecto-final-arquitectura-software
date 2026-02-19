# Documentación API REST
Versión 1.0 - Sistema Financiero

## Endpoint: Obtener Cuenta
GET /api/v1/accounts/{id}

### Response 200
{
  "id": "123",
  "owner": "Juan Pérez",
  "balance": 5000.00,
  "currency": "USD"
}

## Endpoint: Crear Transacción
POST /api/v1/transactions

### Body
{
  "fromAccount": "123",
  "toAccount": "456",
  "amount": 150.00
}

## Manejo de Errores
- 400 Bad Request
- 401 Unauthorized (Token inválido)
- 404 Not Found
- 500 Internal Server Error
