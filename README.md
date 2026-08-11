# Formularios CRIM: AS-52 y AS-74

Aplicación web estática para asistir en la preparación de los formularios del Centro de Recaudación de Ingresos Municipales (CRIM) de Puerto Rico:

- **AS-52 — Solicitud de cambio de dueño:** para recopilar los datos de la propiedad, la transacción, el transmitente y los adquirentes.
- **AS-74 — Hoja de información de dueños en comunidad:** para documentar comuneros o herederos de una propiedad, con sus participaciones y datos de contacto.

La aplicación presenta los campos de cada formulario en una interfaz clara y genera un PDF descargable a partir de las plantillas incluidas. Es una herramienta de apoyo administrativo: no está afiliada al CRIM y no sustituye el criterio o la revisión de profesionales cualificados.

## Qué puede hacer

- Completar los datos de propiedad, catastro, escritura, notario, dueños y adquirentes.
- Generar un PDF AS-52 rellenado para solicitudes de cambio de dueño.
- Generar un PDF AS-74 rellenado para propiedades en comunidad hereditaria o pro-indiviso.
- Añadir hasta diez dueños o comuneros por hoja AS-74.
- Marcar opciones relevantes del AS-52, como tipo de negocio jurídico, uso, material y condición del solar.
- Validar de forma orientativa campos comunes: número de catastro, fechas, teléfonos, números de Seguro Social, porcentajes y datos requeridos.
- Exportar la información de un caso como archivo JSON e importarla posteriormente.
- Conservar la información de trabajo en el almacenamiento local del navegador para continuar un caso en el mismo dispositivo.
- Descargar los documentos generados sin enviar los datos a un servidor.

## Uso

1. Abra `index.html` en un navegador moderno o publique el proyecto en un servidor web estático.
2. Seleccione **AS-52** o **AS-74**.
3. Complete los campos solicitados.
4. Si aparecen avisos de validación, revise la información; también puede continuar si corresponde.
5. Seleccione **Generar PDF** para descargar el documento preparado.
6. Revise cuidadosamente el PDF antes de firmarlo, presentarlo o entregarlo.

Para continuar un caso en otro momento o equipo, use **Exportar JSON**. Use **Importar JSON** para restaurar una exportación previa.

## Privacidad y datos sensibles

El procesamiento de los formularios y la generación del PDF ocurren en el navegador. La aplicación no incluye servidor, base de datos ni mecanismo de envío de información a terceros.

Los datos introducidos pueden guardarse en el `localStorage` del navegador para facilitar la continuidad del trabajo. Esto puede incluir información sensible, como números de Seguro Social.

Al trabajar con esta herramienta:

- Use un equipo y navegador de confianza.
- Evite usar equipos compartidos; si los usa, seleccione **Limpiar** al terminar.
- Guarde las exportaciones JSON y los PDFs únicamente en ubicaciones seguras.
- Borre los datos del sitio desde el navegador si desea eliminar toda información local.
- Confirme que los datos del PDF sean correctos antes de firmar o presentar el documento.

## Requisitos y publicación

No requiere instalación, compilación, base de datos ni dependencias de servidor. Se puede abrir localmente o publicar en servicios y servidores de archivos estáticos, por ejemplo GitHub Pages, Apache o Nginx.

Mantenga `index.html` y el directorio `assets/` juntos al publicar, porque este último contiene las plantillas PDF y la biblioteca utilizada para rellenarlas.

## Estructura del proyecto

```text
.
├── index.html                 # Interfaz principal y avisos al usuario
├── README.md                  # Documentación del proyecto
└── assets/
    ├── app.js                 # Campos, validaciones y generación local de PDF
    ├── styles.css             # Estilos de la interfaz
    ├── templates/
    │   ├── as52.pdf           # Plantilla PDF del formulario AS-52
    │   └── as74.pdf           # Plantilla PDF del formulario AS-74
    └── vendor/
        └── pdf-lib.min.js     # Biblioteca para rellenar PDFs en el navegador
```

## Limitaciones y aviso

Esta herramienta ayuda a preparar información y documentos, pero no garantiza que un formulario sea completo, correcto o aceptado por el CRIM u otra agencia gubernamental. Los requisitos, versiones de los formularios y procedimientos pueden cambiar.

El usuario es responsable de verificar la exactitud, integridad y pertinencia de la información ingresada, así como de consultar a un abogado, CPA u otro profesional cuando sea necesario. La aplicación no constituye asesoramiento legal, contributivo ni profesional.

## Licencia

Este repositorio se distribuye bajo la licencia incluida en [LICENSE](LICENSE).
