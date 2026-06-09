# Shakeaholic · Tablero de Costos

Herramienta interna de uso personal para costear shakes, alimentos, bebidas y snacks,
calcular merma, empaque, IVA, food cost % y precio sugerido. Funciona 100% en el
navegador (GitHub Pages), sin servidor ni base de datos.

## Cómo desplegar en GitHub Pages

1. Crea un repositorio (recomendado **privado**) y sube `index.html` en la raíz.
2. **Settings → Pages → Build and deployment → Source: "Deploy from a branch"**,
   rama `main`, carpeta `/ (root)`. Guarda.
3. En 1–2 minutos tendrás la URL: `https://<tu-usuario>.github.io/<tu-repo>/`

## Acceso

- Usuario inicial: **admin / shakeaholic** → cámbialo en cuanto entres.
- Puedes registrar usuarios nuevos desde la pantalla de acceso.
- Las contraseñas se guardan cifradas (SHA-256) en el navegador.

## Importante (es un candado suave, no seguridad real)

- GitHub Pages es estático: el login evita curiosos, pero no es seguridad fuerte.
  No guardes información sensible aquí.
- Los **usuarios y los datos viven en el navegador** donde los capturas. Si abres la
  app en otra computadora, no estarán.
- Por eso: usa **Respaldar** (descarga un `.json`) seguido cada cierto tiempo, y
  **Restaurar** para mover o recuperar datos. **Exportar CSV** sirve para reportes.

## Estructura

- `index.html` — la aplicación completa (logo, estilos y lógica incluidos).
- Catálogos: Proteínas, Ingredientes (shakes/alimentos), Empaque.
- Parámetros: food cost objetivo, IVA, merma default, mano de obra.
- Costeo: Shakes y Alimentos (recetas con cálculo automático).
- Reventa: Bebidas y Snacks/Treats.
- Resumen: KPIs y semáforo de food cost.

## Notas de costeo

- Costo total = (insumos × (1 + merma)) + empaque + mano de obra.
- Precio sin IVA = precio público ÷ (1 + IVA).
- Food cost % = costo total ÷ precio sin IVA. Meta sugerida: 28–32%.
- Confirma la tasa de IVA aplicable con tu contador.
