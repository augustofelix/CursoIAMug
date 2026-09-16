# PDR-001: Procesamiento de facturas - Software para el procesamiento de facturas en formato PDF

## Comtexto y problema
En un estudio contable o empresa es necesario cargar las facturas a un sistema que posteriormente calcule los impuestos.
Dada la gran cantidad de comprobantes y complejidad de estos, es necesario reducir el tiempo y erores de tipeo.
Es muy común que en las áreas contables las personas afectadas a esta tare destinen gran parte de su tiempo a esta tarea, en lugar de destinar el tiempo al control, análisis y asesoramiento profesional.

Personas:
- Mariela: administrativa contable, carga mensualmente 5000 comprobantes de diferentes clientes y quiere reducir este tiempo para poder aportarle mas valor al análisis de los gastos de sus clientes.
- Juan Manuel: analista financiero, ingresa al mes 800 comprobantes de compras de una empresa agropecuaria con sus respectivos detalles de productos, le lleva mucho tiempo por los errores en la carga de cada producto.


## Objetivo
Proporcionar una aplicacion capaz de leer los documentos de factura en formato PDF y que los mismos sean retornados en un formato estandard (Json) para que cualquier aplicación pueda utilizarlo para su importación y posterior procesamiento.


## Requerimientos Funcionales
- RF-01: Leer el encabezado de la factura
- RF-02: Leer el cuerpo o detalle de la factura.
- RF-03: Detectar la catidad en cada producto detectado.
- RF-04: Leer el pie de la factura y diferencias los totales, subtotales e impuestos. 
- RF-05: Cargar el lote de facturas en una interface web.
- RF-06: Carga de facturas por API Rest. 

## Requerimiento no funcionales
- RNF-01: La cantidad de comprobantes por lote <= 50
- RNF-02: timepo de proceso para 50 comprobantes < 30 segundos.
- RNF-03: la presision de la lectura >= 90% de la lista de testing de comprobantes.

## Criterios de aceptación
- AC-01: CUIT valido, Razon social (usando NER) y el domicilio.
- AC-02: Distinguir los codigos de profuctos y su descripcion.


## Fuera de alcance
Solo se procesaran archivos PDF, no se enviaran por email, no se escanearan desde la aplicacion

## Riesgo y dependencias
