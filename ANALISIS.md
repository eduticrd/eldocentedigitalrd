# Análisis

El original mezcla UI, autenticación, Firestore, OCR, PDF, Excel, anuncios y traducciones en más de 300 KB. Descarga y reescribe el JSON completo del usuario desde `/datos`, aunque solo se vea una pestaña. También contiene funciones y manejadores duplicados, bibliotecas pesadas cargadas al inicio y numerosas interpolaciones `innerHTML` con riesgo de XSS almacenado.

La nueva base separa shell, servicios y vistas, usa consultas granulares, límites, `serverTimestamp`, escape de texto, CSP y reglas con campos permitidos. La carga diferida no sustituye las reglas de Firestore.