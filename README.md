# AulaDocente modular

El `index.html` es ahora un shell. Cada pestaña usa `import()` y consulta únicamente su subcolección. La carga diferida mejora rendimiento y reduce exposición accidental, pero la autorización real depende de Authentication y `firestore.rules`.

## Antes de desplegar
1. Completa `src/firebase-config.js`.
2. Migra `/usuarios/{uid}/datos/*` a `/usuarios/{uid}/cursos/{cursoId}/...`.
3. Prueba con Firebase Emulator Suite.
4. Despliega reglas y Hosting.
5. Elimina la compatibilidad `/datos` al terminar.

El original se incluye como `index.original.html`. PDF, XLSX, OCR, firmas, anuncios y biblioteca pública avanzada deben portarse después como módulos secundarios bajo demanda.