# ZG ZoneCosmeticos 1.10.1 — configuración / configuration

## Español

### Archivos

| Ruta | Función |
|---|---|
| `config/ZONEMODS/zonecosmeticos/catalogo.toml` | Catálogo **editable** del servidor; se crea desde datos iniciales si falta. `/cosmetic reload` valida y aplica el TOML completo, sin aplicar cambios parciales si hay un error. Conserva los IDs de compras existentes. |
| `config/ZONEMODS/zonecosmeticos/catalogo.json` | Datos anteriores usados para la migración inicial; después de crear el TOML se conserva como respaldo. |
| `config/zonecosmeticos-cliente.json` | Preferencia visual local `particulas`: `0` todas, `1` solo las propias, `2` desactivadas. El cliente la lee al iniciar y la escribe al cambiar el modo. |
| Datos del mundo `zonecosmeticos.dat` | Propiedad, recibos, equipamiento y tres conjuntos por UUID. Respáldalos con el mundo. |

En `[rendimiento]`, `presupuesto_particulas` acepta `0..256`, `intervalo_ticks` acepta `2..40` y `distancia` acepta `8..64`. Cada sección `[categoria.id]` de las categorías `cabeza`, `espalda`, `cola`, `caminar`, `aura`, `flecha` y `manos` define `nombre`, `modo`, `precio`, `permiso`, `descripcion`, `tipo`, `color_tipo`, `estilo` y `color_modelo`. `modo` acepta `gratis`, `permiso` o `gochocoins`; el modo `gochocoins` exige `precio > 0`. `precio` admite `0..100000000`. Los colores usan `#RRGGBB`. El catálogo admite hasta 128 IDs y el estilo debe existir para su categoría. `[acceso_categorias] exigir_permiso` puede exigir el nodo adicional de categoría.

`/cosmetic` abre el armario. `/cosmetic conjunto guardar|aplicar|borrar <1..3>` guarda, aplica o borra conjuntos. Aplicar vuelve a comprobar propiedad, categoría y permiso; no concede cosméticos ni modifica saldo. `/cosmetic catalogo <zona>`, `/cosmetic info <id>`, `/cosmetic equipar <id>`, `/cosmetic quitarzona <zona>` y `/cosmetic quitar` gestionan el uso. `/cosmetic reload` requiere administración. `zonecosmeticos.use` permite el uso normal; `zonecosmeticos.conjuntos` añade los conjuntos y también requiere `use`. Los nodos `zonecosmeticos.admin`, `zonecosmeticos.admin.otorgar`, `.retirar`, `.reload`, `zonecosmeticos.cosmetic.ID` y opcionalmente `zonecosmeticos.categoria.ZONA` controlan las demás acciones.

## English

`config/ZONEMODS/zonecosmeticos/catalogo.toml` is the **editable server catalog**. `/cosmetic reload` validates and applies a whole snapshot; an invalid file does not partially replace the active catalog. Preserve purchased IDs. The older `catalogo.json` serves as a migration source/backup. Client `config/zonecosmeticos-cliente.json` stores `particulas` values 0 (all), 1 (own only) and 2 (off). World data stores ownership, receipts, equipment and up to three outfits per player UUID.

`[rendimiento]` contains particle budget `0..256`, interval `2..40` ticks and distance `8..64`. Each `[category.id]` entry has name, purchase mode, price, permission, description, rarity, colors and a category compatible style. Modes are `gratis`, `permiso` and `gochocoins`; paid entries need a positive price. The catalog allows at most 128 IDs. Use `/cosmetic ayuda` for the command list. Saving/applying outfits needs both `zonecosmeticos.use` and `zonecosmeticos.conjuntos`; applying one rechecks ownership and permissions, and never grants items or coins. Back up catalog and world data before changes.

