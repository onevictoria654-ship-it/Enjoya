# 📊 CONSOLIDADO ENJOYA - Guía de Excel

Este archivo te guiará para crear el Excel consolidado con 5 pestañas.

## Instrucciones para crear las 5 pestañas:

### PESTAÑA 1: INICIO (Dashboard Resumido)

```
DASHBOARD ENJOYA - MAYO 2026

Última actualización: [fecha]

├─ RESUMEN DEL MES
│  ├─ Ingresos totales:          S/ _____ (=SUMA(VENTAS!D:D))
│  ├─ Costos totales:            S/ _____ (=SUMA(COSTOS-PRODUCTOS!E:E)*Unidades vendidas)
│  ├─ Ganancia neta:             S/ _____ (=B3-B4)
│  └─ Margen %:                  _____ % (=(B5/B3)*100)
│
├─ ESTADO FISCAL (RUS)
│  ├─ Ingresos acumulados 2025:  S/ 96,000 (Límite máximo)
│  ├─ Cuota mensual RUS:         S/ 50 (Si ingresos entre S/5,000-S/8,000)
│  └─ ⚠️ Viabilidad:            ✓ Dentro de límite RUS
│
└─ PRODUCTOS TOP 3
   ├─ 1. [Producto] - Ventas: ___ unidades
   ├─ 2. [Producto] - Ventas: ___ unidades
   └─ 3. [Producto] - Ventas: ___ unidades
```

---

### PESTAÑA 2: COSTOS-PRODUCTOS (Desglose de costos por producto)

```
┌─────────────────────────────────────────────────────────────────┐
│ COSTEO DE PRODUCTOS - ENJOYA                                    │
└─────────────────────────────────────────────────────────────────┘

PRODUCTO: COLLAR DE PLATA

MATERIA PRIMA DIRECTA (MPD)
Descripción         │ Cantidad │ Precio Unit │ Subtotal      │ INSTRUCCIÓN
────────────────────┼──────────┼─────────────┼───────────────┼──────────────────
Plata (gramos)      │    50    │   S/ 0.80   │ =B3*C3        │ Multiplica qty × precio
Hilo/cordón         │     1    │   S/ 0.50   │ =B4*C4        │
Cierre              │     1    │   S/ 0.30   │ =B5*C5        │
───────────────────────────────────────────────────────────────────
TOTAL MPD           │          │             │ =SUMA(D3:D5)  │ Suma todos los subtotales


MANO DE OBRA DIRECTA (MOD)
Descripción              │ Horas │ Tarifa/hr  │ Subtotal      │ INSTRUCCIÓN
─────────────────────────┼───────┼────────────┼───────────────┼──────────────────
Tejido + diseño          │  0.5  │  S/ 7.10   │ =B9*C9        │ Horas × tarifa (S/7.10/hr)
Control de calidad       │  0.1  │  S/ 7.10   │ =B10*C10      │
─────────────────────────────────────────────────────────────────
TOTAL MOD           │             │ =SUMA(D9:D10) │ Suma de horas trabajadas


COSTOS INDIRECTOS DE FABRICACIÓN (CIF)
Descripción              │ Monto  │ % Asignado │ Valor         │ INSTRUCCIÓN
─────────────────────────┼────────┼────────────┼───────────────┼──────────────────
Luz/agua (S/ 50/mes)     │ S/ 50  │    2.5%    │ =B14*C14      │ Reparte entre todos los productos
Internet/web             │ S/ 30  │    1.5%    │ =B15*C15      │
Transporte de fichas     │ S/ 20  │    1.0%    │ =B16*C16      │
─────────────────────────────────────────────────────────────────
TOTAL CIF           │             │ =SUMA(D14:D16) │ Suma CIF asignado


┌──────────────────────────────────────────────────────────────────┐
│ COSTO UNITARIO TOTAL = MPD + MOD + CIF                           │
│ Costo Unitario: S/ _____ (=D6+D11+D17)                           │
└──────────────────────────────────────────────────────────────────┘


REPETIR ESTRUCTURA PARA:
- PULSERA DE PLATA
- RESINA (especificar tipo)
- [Otros productos futuros]
```

---

### PESTAÑA 3: PUNTO-EQUILIBRIO (Cálculo de viabilidad)

```
┌────────────────────────────────────────────────────────────────┐
│ ANÁLISIS DE PUNTO DE EQUILIBRIO                                │
└────────────────────────────────────────────────────────────────┘

COLLAR DE PLATA

DATOS BASE
┌──────────────────────────────────────────────────────────────┐
│ Precio unitario de venta:    S/ _____ (ingresa aquí)         │
│ Costo unitario:              S/ _____ (=COSTOS-PRODUCTOS!D18)│
│ Margen por unidad:           S/ _____ (=B23-B24)             │
│ Margen %:                    _____ % (=(B25/B23)*100)        │
└──────────────────────────────────────────────────────────────┘

COSTOS FIJOS MENSUALES
Descripción                  │ Monto      │ INSTRUCCIÓN
─────────────────────────────┼────────────┼──────────────────
Alquiler taller (o % casa)   │ S/ _____   │ Ingresa costo mensual
Cuota RUS                    │ S/ 50      │ O S/ 20 si ingresos < S/5k
Página web/hosting           │ S/ 30      │
Teléfono/Internet            │ S/ 40      │
─────────────────────────────────────────────────────────────────
TOTAL COSTOS FIJOS    │ S/ _____ (=SUMA(B28:B31))


CÁLCULO DEL PUNTO DE EQUILIBRIO
┌──────────────────────────────────────────────────────────────┐
│ PE = Costos Fijos / (Precio Unitario - Costo Unitario)       │
│                                                              │
│ PE = _____ / (_____) = _____ unidades/mes                   │
│      =B32 / (B23-B24)                                       │
│                                                              │
│ Ingresos necesarios: S/ _____ (=B23*PE)                     │
└──────────────────────────────────────────────────────────────┘

INTERPRETACIÓN:
▪ Debes vender MÍNIMO _____ unidades/mes para cubrir costos
▪ Ingreso mínimo necesario: S/ _____
▪ Con _____ unidades/mes tienes ganancia


REPETIR PARA:
- PULSERA DE PLATA
- RESINA
- [Otros productos]
```

---

### PESTAÑA 4: VENTAS-INGRESOS (Consolidado de ventas)

```
┌────────────────────────────────────────────────────────────────┐
│ REGISTRO DE VENTAS - ENJOYA 2025-2026                          │
└────────────────────────────────────────────────────────────────┘

MAYO 2026

Fecha      │ Producto        │ Cantidad │ Precio Unit │ Subtotal   │ INSTRUCCIÓN
───────────┼─────────────────┼──────────┼─────────────┼────────────┼──────────────────
2026-05-01 │ Collar          │    2     │  S/ 45.00   │ =D4*E4     │ Cantidad × Precio
2026-05-02 │ Pulsera         │    3     │  S/ 25.00   │ =D5*E5     │
2026-05-05 │ Resina          │    1     │  S/ 15.00   │ =D6*E6     │
           │                 │          │             │            │
───────────┴─────────────────┴──────────┴─────────────┴────────────┴──────────────────
TOTAL MAYO:                  S/ _____ (=SUMA(F4:F100))

TOTALES POR PRODUCTO (al final de mes)
Producto  │ Unidades vendidas │ Ingresos generados │ INSTRUCCIÓN
──────────┼───────────────────┼────────────────────┼──────────────────
Collar    │ =CONTAR.SI(B:B;"Collar") │ =SUMAR.SI(B:B;"Collar";F:F) │ Suma automática por tipo
Pulsera   │ =CONTAR.SI(B:B;"Pulsera") │ =SUMAR.SI(B:B;"Pulsera";F:F) │
Resina    │ =CONTAR.SI(B:B;"Resina")  │ =SUMAR.SI(B:B;"Resina";F:F)  │
──────────────────────────────────────────────────────────────────

TABLAS DINÁMICAS A CREAR:
✓ Suma de ingresos por producto (pastel)
✓ Ventas por semana (barras)
✓ Top días de venta
```

---

### PESTAÑA 5: GUIA-FORMULAS (Referencia rápida)

```
┌────────────────────────────────────────────────────────────────┐
│ GUÍA DE FÓRMULAS - CONSULTA RÁPIDA                             │
└────────────────────────────────────────────────────────────────┘

📌 FÓRMULAS BÁSICAS USADAS EN ENJOYA

1. SUMA de un rango
   =SUMA(C4:C10)
   ➜ Suma todas las celdas de C4 a C10

2. MULTIPLICAR (Cantidad × Precio)
   =B4*C4
   ➜ Multiplica valor en B4 por C4

3. SUMAR.SI (Suma si cumple condición)
   =SUMAR.SI(B:B;"Collar";F:F)
   ➜ Suma en columna F donde columna B diga "Collar"

4. CONTAR.SI (Cuenta si cumple condición)
   =CONTAR.SI(B:B;"Collar")
   ➜ Cuenta cuántas veces aparece "Collar" en columna B

5. PORCENTAJE
   =(B5/B3)*100
   ➜ Calcula qué porcentaje es B5 respecto a B3


🎨 COLORES POR SECCIÓN
┌────────────────────────────────────────────────────────────────┐
│ 🟦 Azul = Datos a ingresar manualmente                         │
│ 🟩 Verde = Fórmulas/Cálculos automáticos                       │
│ 🟨 Amarillo = Advertencias o límites RUS                       │
│ 🟥 Rojo = Totales o valores críticos                           │
└────────────────────────────────────────────────────────────────┘


⚠️ RECORDAR PARA RUS:
▪ Límite ingreso anual: S/ 96,000 (S/ 8,000/mes aproximado)
▪ Cuota mensual RUS: S/ 20 (hasta S/ 5k) o S/ 50 (S/ 5k-S/ 8k)
▪ No puedes usar IGV
▪ Fórmula Margen: (Ingresos - Costos) / Ingresos × 100
```

---

## 📋 PRÓXIMOS PASOS:

1. ✅ Crea un archivo Excel en blanco
2. ✅ Renombra las 5 pestañas según arriba
3. ✅ Copia la estructura de cada pestaña
4. ✅ Coloca fórmulas donde dice "INSTRUCCIÓN"
5. ✅ Prueba ingresando datos de prueba
6. ✅ Guarda como: `ENJOYA-CONSOLIDADO-MAYO2026.xlsx`

¿Necesitas que te ayude con alguna pestaña específica? 🚀
