# Shakeaholic · Tablero de Costos e Inventario

Herramienta interna para costear shakes, alimentos, bebidas y snacks (merma, empaque,
IVA, food cost %, precio sugerido) **y** controlar inventario en dos ubicaciones:
**bodega** (presentación original) y **kiosko** (venta individual / por porción).
Funciona 100% en el navegador (GitHub Pages), sin servidor ni base de datos.

## Desplegar en GitHub Pages
1. Sube `index.html` y `README.md` a la raíz de un repositorio (recomendado **privado**).
2. **Settings → Pages → Source: "Deploy from a branch" → `main` → `/ (root)`**.
3. En 1–2 min: `https://<tu-usuario>.github.io/<tu-repo>/`

## Acceso
- Usuario inicial: **admin / shakeaholic** (cámbialo en cuanto entres).
- Puedes registrar usuarios nuevos. Las contraseñas se guardan cifradas (SHA-256).

## Inventario y traspasos (bodega → kiosko)
- Cada producto tiene **dos inventarios**: presentación original (bodega) e individual/porción (kiosko), cada uno con su **stock mínimo**.
- Cada producto define una **equivalencia** (ej. 1 bote = 27 scoops, 1 caja = 12 piezas, 1 bolsa = 20 porciones).
- El botón **⇄ Traspasar** mueve mercancía de bodega a kiosko según la equivalencia y **pide la clave del encargado** (se configura en Parámetros).
- La pestaña **Inventario** tiene tres vistas (**Todos / Bodega / Kiosko**) con búsqueda, filtro por categoría, estados (OK / Bajo / Agotado) y alertas de caducidad. Desde Kiosko, si algo está bajo, el botón sugiere **Reponer** trayéndolo de bodega.

## Catálogos
- Proteínas, Ingredientes (shakes/alimentos), Empaque, Bebidas y Snacks: con código/item,
  proveedor, marca, fechas de compra y caducidad, presentación, precios e inventarios.
- Botones para **agregar, editar y eliminar** productos en cada catálogo.
- Costeo de Shakes y Alimentos: cada uno con su **número de item** e ingredientes que se
  pueden **agregar o quitar**.

## Importante (candado suave, no seguridad real)
- GitHub Pages es estático: el login evita curiosos, pero no es seguridad fuerte.
- **Usuarios y datos viven en el navegador** donde los capturas. En otra computadora no estarán.
- Por eso: usa **Respaldar** (descarga `.json`) seguido, y **Restaurar** para mover/recuperar.
  **Exportar CSV** sirve para reportes de costeo.

## Notas de costeo
- Costo total = (insumos × (1 + merma)) + empaque + mano de obra.
- Precio sin IVA = precio público ÷ (1 + IVA). Food cost % = costo ÷ precio sin IVA. Meta: 28–32%.
- Confirma la tasa de IVA con tu contador.
