# Addenda Multiasistencia · Reparaciones

Herramienta web que agrega la Addenda comercial de Multiasistencia (giro Reparaciones, esquema `multiasistencia_v1.07` de Diverza) a un CFDI 4.0 **ya timbrado**.

**Abrir:** https://miguelglz.github.io/addenda-multiasistencia/

## Qué hace

- **XML:** inserta `<cfdi:Addenda>` como texto justo antes de `</cfdi:Comprobante>`. Todo lo anterior queda idéntico byte a byte (sello, timbre y UUID intactos). Verifica el resultado antes de permitir la descarga.
- **PDF:** conserva todas las páginas del PDF original y agrega al final una hoja con los datos de la Addenda.
- **Validaciones:** campos requeridos, formato de importes, máximo 10 vales por tipo, orden Refacciones → Complemento MO y cuadre contra el SubTotal del CFDI.
- **Autopruebas** integradas (A1–A17).

## Privacidad

Es una página estática. Los archivos XML y PDF se procesan solo en el navegador del usuario; no se envían a ningún servidor. La única dependencia externa es [pdf-lib](https://pdf-lib.js.org/) desde cdnjs.

## Fuera de alcance

Otros giros (Cristales, Honorarios, Grúas, Asistencia, GMedicos), retenciones, timbrado, cancelación y validación de sellos.
