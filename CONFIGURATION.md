# ZoneCosmeticos — Configuration / Configuración (2026-11-08)

| Side / Lado | Version / Versión |
|---|---|
| Universal / Ambos lados | 1.12.1 |

## Catalog and permissions / Catálogo y permisos

Server file: `config/ZONEMODS/zonecosmeticos/catalogo.toml`. Edit existing ID sections and use `/cosmetic reload`; do not duplicate sections or rename purchased IDs. / Edita secciones existentes y recarga; no dupliques ni renombres IDs adquiridas.

The six additional wings from 1.11 and20 Anime entries from 1.12 start as:

```toml
modo = "permiso"
precio = 0
permiso = ""
```

This does not grant them for free. They require an administrative grant or individual permission. / Ese estado no las regala; requiere concesión o nodo individual.

ZoneCrates is an optional wallet integration. Without it the currency purchase path is unavailable; free items and permission-based access remain usable. Core is required separately on the server. / ZoneCrates es integración opcional de cartera; sin él no hay compra monetaria, pero se conservan accesos gratis y por permisos. Core se exige aparte solo en servidor.

| Goal / Objetivo | Settings / Ajustes |
|---|---|
| Grant or individual node / Concesión o nodo | `modo="permiso"`, `precio=0`, `permiso=""` |
| Rank access / Acceso por rango | `modo="permiso"`, `permiso="verified.rank.node"` using the real node / usando nodo real |
| Currency sale / Venta monetaria | `modo="gochocoins"`, positive `precio`, coin provider available / precio positivo y proveedor disponible |
| Free entry / Entrada gratuita | `modo="gratis"`, `precio=0` |

`zonecosmeticos.use` permits wardrobe/purchase/equip operations but does not unlock all items. `zonecosmeticos.cosmetic.<ID>` grants direct individual access. Category permission `zonecosmeticos.categoria.<zona>` additionally applies when `acceso_categorias.exigir_permiso=true`. A configured extra permission remains required where applicable. / Uso no desbloquea todo; nodo individual da acceso directo y categorías pueden exigir permiso adicional.

Saved outfits need `zonecosmeticos.conjuntos` plus normal use access. Administration separates `zonecosmeticos.admin.otorgar`, `.retirar`, `.reload`; `zonecosmeticos.admin` or OP 2 grants full administration. / Conjuntos requiere permiso adicional; administración separa concesión, retirada y recarga.

## Commands / Comandos

```text
/cosmetic
/cosmetic catalogo espalda
/cosmetic info corona_astral
/cosmetic equipar corona_astral
/cosmetic quitarzona cabeza
/cosmetic conjunto guardar 1
/cosmetic conjunto aplicar 1
/cosmetic conjunto borrar 1
/cosmetic otorgar NombreJugador corona_astral
/cosmetic otorgaruuid UUID corona_astral
/cosmetic retirar NombreJugador corona_astral
/cosmetic retiraruuid UUID corona_astral
/cosmetic reload
```

Names require online players; UUID administration also works offline. Outfit slots are 1–3. Removing equipment does not revoke ownership. Administrative revocation removes the grant/old receipts without refunding coins or removing external permissions. There is no `/cosmetic comprar`; purchase is in the UI. / Nombre exige conectado; UUID admite desconectado. Slots 1–3; desequipar no revoca. Revocar no reembolsa ni quita permisos externos. Compra solo desde interfaz.

## Migration, effects and data / Migración, efectos y datos

The Anime migration adds absent IDs only, preserving edited names/prices/permissions and player data. It creates `catalogo.pre-1.12.0.toml` without overwriting an existing backup; keep `coleccion_anime_1120=true` so deliberately removed entries remain removed. Catalog cap: 128. / Migración aditiva conserva ajustes/datos y respaldo existente; mantén marcador para respetar eliminaciones. Límite 128.

Back up `<world>/data/zonecosmeticos.dat` and server config. Local preference is `config/zonecosmeticos-cliente.json`, with effects all/own/off. Server `[rendimiento]` supports `presupuesto_particulas`0–256, `intervalo_ticks`2–40 and `distancia`8–64. / Conserva datos/configuración; preferencia local todos/propios/desactivados y límites del servidor.

Only one accessory per zone equips. Wings, capes, backpacks, katanas and scrolls share `espalda`. Own first-person aura suppression applies by `aura` category, including custom entries. Camera changes do not send an equip change or hide your aura from others. / Una pieza por zona; espalda es compartida. Ocultar aura propia se aplica a categoría aura, incluso entradas custom, sin desequipar ni ocultarla a los demás.

[Current release / Entrega actual](RELEASE-2026-11-08.md) · [README](README.md).
