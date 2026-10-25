# SUPERMERCADO_SANDBOX - Catálogo simulado de café molido

**Hablador QR AdaptaPro ERP (Almacenes + Ubicaciones Físicas + habladores QR).**

⚠️ DATOS 100% FICTICIOS - MODELO DE DEMOSTRACIÓN SANDBOX. No son productos, precios ni ubicaciones reales.

**Anaquel de este hablador:** `ANQ-3B` - Pasillo 3 (Cafés y bebidas) - SUPERMERCADO-SBX-01 (simulado). El QR impreso pertenece a este anaquel y abre siempre ESTE catálogo (URL estable).

## Cómo usarlo (comprador con IA en su móvil)

1. Escanea el QR del anaquel: abre este catálogo.
2. Pide a tu IA (Gemini, Instinct u otra) lo que necesitas: "ordena por precio por 100 g", "solo descafeinado", "sin azúcar añadida", "sin gluten declarado".
3. La IA compara por unidad comparable ($/100 g) SOLO entre productos del mismo tipo y filtra o excluye SOLO por atributos e ingredientes DECLARADOS; lo no declarado queda sin confirmar.
4. Menor precio no implica mejor calidad. La IA recomienda; el cliente decide.

## Lista contra presupuesto y recorrido de recogida (picking)

Cada registro trae `ubicacion_fisica` (ID estable simulado) y `ruta_recogida` (orden de picking). Con esos datos tu IA puede:

- Armar una lista contra tu presupuesto (ej.: "tengo $10 y necesito café sin azúcar añadida: ¿qué compro?").
- Ordenar la lista como recorrido de recogida por el anaquel (menor `ruta_recogida` primero), para caminar una sola pasada.

**Alcance honesto del modelo:** el catálogo solo PUBLICA los datos (precios, atributos, ubicación, orden). No hay carrito persistente, ni sincronización automática, ni un asistente que reaccione solo al cambiar de anaquel: cada consulta parte de los archivos publicados en ese momento.

## Actualización sin reimprimir el QR

Precios, altas y bajas se editan en estos archivos (misma URL, mismo QR). La edición es manual: editar el registro del producto y esta tabla.

## Productos ($/100 g de menor a mayor)

| $/100 g | Marca | Tipo | g | $ | Nivel-Pos | Ruta | Registro |
|---|---|---|---|---|---|---|---|
| 0.72 | MARCA GENÉRICA | mezcla básica | 500 | 3.60 | 1-1 | 1 | [SBX-GEN-500.md](https://raw.githubusercontent.com/AdaptaProERP/SUPERMERCADO_SANDBOX/main/productos/SBX-GEN-500.md) |
| 0.80 | MARCA GENÉRICA | mezcla básica | 200 | 1.60 | 1-2 | 2 | [SBX-GEN-200.md](https://raw.githubusercontent.com/AdaptaProERP/SUPERMERCADO_SANDBOX/main/productos/SBX-GEN-200.md) |
| 0.88 | CAFÉ ANÓNIMO | con azúcar añadida | 500 | 4.40 | 1-3 | 3 | [SBX-ANO-500.md](https://raw.githubusercontent.com/AdaptaProERP/SUPERMERCADO_SANDBOX/main/productos/SBX-ANO-500.md) |
| 0.90 | TOP10 CAFÉ | mezcla arábica/robusta | 500 | 4.50 | 2-1 | 5 | [SBX-T10-500.md](https://raw.githubusercontent.com/AdaptaProERP/SUPERMERCADO_SANDBOX/main/productos/SBX-T10-500.md) |
| 0.95 | CAFÉ ANÓNIMO | con azúcar añadida | 200 | 1.90 | 1-4 | 4 | [SBX-ANO-200.md](https://raw.githubusercontent.com/AdaptaProERP/SUPERMERCADO_SANDBOX/main/productos/SBX-ANO-200.md) |
| 1.00 | CAFÉ SANDBOX A | tostado medio | 500 | 5.00 | 2-3 | 7 | [SBX-A-500.md](https://raw.githubusercontent.com/AdaptaProERP/SUPERMERCADO_SANDBOX/main/productos/SBX-A-500.md) |
| 1.00 | TOP10 CAFÉ | mezcla arábica/robusta | 200 | 2.00 | 2-2 | 6 | [SBX-T10-200.md](https://raw.githubusercontent.com/AdaptaProERP/SUPERMERCADO_SANDBOX/main/productos/SBX-T10-200.md) |
| 1.08 | CAFÉ SANDBOX B | tostado oscuro | 500 | 5.40 | 3-1 | 9 | [SBX-B-500.md](https://raw.githubusercontent.com/AdaptaProERP/SUPERMERCADO_SANDBOX/main/productos/SBX-B-500.md) |
| 1.10 | CAFÉ SANDBOX B | tostado oscuro | 200 | 2.20 | 3-2 | 10 | [SBX-B-200.md](https://raw.githubusercontent.com/AdaptaProERP/SUPERMERCADO_SANDBOX/main/productos/SBX-B-200.md) |
| 1.20 | CAFÉ SANDBOX A | tostado medio | 200 | 2.40 | 2-4 | 8 | [SBX-A-200.md](https://raw.githubusercontent.com/AdaptaProERP/SUPERMERCADO_SANDBOX/main/productos/SBX-A-200.md) |
| 1.40 | CAFÉ SANDBOX C | descafeinado | 500 | 7.00 | 3-3 | 11 | [SBX-C-500.md](https://raw.githubusercontent.com/AdaptaProERP/SUPERMERCADO_SANDBOX/main/productos/SBX-C-500.md) |
| 1.55 | CAFÉ SANDBOX C | descafeinado | 200 | 3.10 | 3-4 | 12 | [SBX-C-200.md](https://raw.githubusercontent.com/AdaptaProERP/SUPERMERCADO_SANDBOX/main/productos/SBX-C-200.md) |
| 1.60 | ACME COFFEE | 100% arábica | 500 | 8.00 | 4-1 | 13 | [SBX-ACM-500.md](https://raw.githubusercontent.com/AdaptaProERP/SUPERMERCADO_SANDBOX/main/productos/SBX-ACM-500.md) |
| 1.80 | ACME COFFEE | 100% arábica | 200 | 3.60 | 4-2 | 14 | [SBX-ACM-200.md](https://raw.githubusercontent.com/AdaptaProERP/SUPERMERCADO_SANDBOX/main/productos/SBX-ACM-200.md) |

Índice legible por máquina: [catalogo.json](https://raw.githubusercontent.com/AdaptaProERP/SUPERMERCADO_SANDBOX/main/catalogo.json) - Ubicaciones del modelo: [UBICACIONES.md](https://raw.githubusercontent.com/AdaptaProERP/SUPERMERCADO_SANDBOX/main/UBICACIONES.md)

Última actualización: 2026-10-25
