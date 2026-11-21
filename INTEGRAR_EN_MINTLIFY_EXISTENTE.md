# Integrar las páginas en un Mintlify ya existente

**No reemplaces tu `docs.json` actual.**

1. Copia los tres archivos `.mdx` de `comparativa/` a la carpeta de tu sitio Mintlify que ya contiene `docs.json`.
2. Abre tu `docs.json` y agrega el siguiente grupo dentro del arreglo `navigation.groups`, conservando los grupos y páginas existentes:

```json
{
  "group": "Comparativa de proveedores",
  "pages": [
    "comparativa/informacion-general-y-flujo",
    "comparativa/reglas-de-negocio-y-calculo",
    "comparativa/integraciones-ia-y-arquitectura"
  ]
}
```

3. Si tu `docs.json` utiliza otra modalidad de navegación (tabs o variantes), incorpora estas tres rutas dentro de la sección correspondiente y no dupliques la propiedad `navigation`.
4. Los enlaces de las tres páginas son absolutos y sin extensión, como requiere Mintlify. Los bloques Mermaid están dentro de las páginas `.mdx`.
5. Desde el directorio del sitio, ejecuta `mint dev` para visualizar y `mint validate` y `mint broken-links` antes de publicar. El CLI se instala con `npm i -g mint` si aún no está disponible.

**Nota:** la portada `index.mdx` y el `docs.json` del paquete de sitio independiente son de ejemplo y no deben sobreescribir la portada ni los ajustes de un sitio en funcionamiento.

**Alcance:** convierte la wiki existente de V1.5.62 sin modificar su interpretación técnica o afirmar verificación operativa en Railway.
