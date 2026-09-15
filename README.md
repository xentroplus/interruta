# InterRuta v1.6.4

Mini app PWA para el registro y generación de informes de recorridos preventivos en rutas interurbanas de fibra óptica.

## v1.5.2
- Conserva los recorridos creados en v1.4 usando la misma clave de almacenamiento local.
- Habilita el cierre únicamente con 20 novedades y todos los nodos registrados.
- Solicita el Coordinador de Fibra Óptica al cierre y permite observaciones generales.
- Genera localmente el informe oficial XLSX con las tres pestañas operativas: REPORTES_DE_RECORRIDOS, FOTOS_ANEXAS_AL_REPORTE y Checklists MPRIU.
- Inserta fotos de nodos y novedades en el informe; las novedades pendientes dejan vacío el espacio DESPUÉS.
- Permite descargar y compartir el archivo generado.
- Mantiene funcionamiento local/offline una vez actualizados los recursos de la PWA.


Corrección v1.5.2: genera internamente el archivo raíz _rels/.rels para evitar fallos de GitHub Pages al omitir archivos con nombre iniciado en punto.


## Corrección v1.5.2
Se corrige la estructura OOXML interna de la plantilla Excel preservando los namespaces originales de Microsoft Excel. Esto evita que Excel reporte el archivo como dañado o vacío. Mantiene compatibilidad con los recorridos guardados en v1.4/v1.5.


## v1.6
Las fotografías capturadas desde InterRuta incorporan sello permanente con fecha/hora, coordenadas GPS, código de cuadrilla y contexto de evidencia (nodo o novedad ANTES/DESPUÉS).

## v1.6.1
Corrige la vista previa de fotografías para mostrar la imagen completa y permitir validar visualmente las cuatro líneas del sello: fecha/hora, GPS, cuadrilla y contexto de evidencia.

## v1.6.4
- Fuerza actualización del service worker sin caché para despliegues GitHub Pages.
- Mantiene sello fotográfico completo y compatibilidad con datos locales existentes.


## v1.6.4
- Normaliza la orientación de fotografías tomadas con el teléfono en horizontal o vertical antes de aplicar el sello.
- Conserva el sello de fecha/hora, GPS, cuadrilla y tipo de evidencia en orientación legible.
- No modifica la lógica de recorridos, novedades ni generación del informe Excel.


## v1.6.4
Corrección de orientación de cámara: evita la doble rotación cuando el navegador móvil ya entrega el stream orientado. La rotación de 90° se aplica solo si la relación vertical/horizontal del fotograma no coincide con la orientación visible del dispositivo.
