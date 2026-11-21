# ZoneCosmeticos

## 1.12.2 · Entregas RPG / RPG deliveries

### Español

Actualización de servidor para Minecraft Forge 1.20.1 y Java 17. Añade saldo de niveles de ZoneLevelUp que se reclama por personaje con /comprasniveles reclamar. El saldo que excede el nivel máximo se conserva. Los grimorios de ZGrimory quedan pendientes si el jugador está desconectado o el inventario está lleno. Se pueden recoger con /compras. La integración registra recibos para evitar entregas duplicadas.

Actualiza el JAR de servidor y conserva el cliente 1.12.1 compatible (protocolo 9). En servidor se requiere ZoneCore 2.1.0 o posterior. ZoneLevelUp y ZGrimory habilitan sus respectivas integraciones.

### English

Server update for Minecraft Forge 1.20.1 and Java 17. Claim ZoneLevelUp level credits for the active character with /comprasniveles reclamar. Excess credits remain available after reaching the level cap. ZGrimory books stay queued for offline players or full inventories and can be collected with /compras. Receipt tracking prevents duplicate deliveries.

Replace the server JAR and keep the compatible 1.12.1 client (protocol 9). The server requires ZoneCore 2.1.0 or later. ZoneLevelUp and ZGrimory enable their respective integrations.

### Archivos / Files

- [Servidor 1.12.2 / Server 1.12.2](https://www.curseforge.com/minecraft/mc-mods/zonecosmeticos/files/9730551)
- [Cliente compatible 1.12.1 / Compatible client 1.12.1](https://www.curseforge.com/minecraft/mc-mods/zonecosmeticos/files/9515741)

[Notas de la versión / Release notes](RELEASE-2026-11-21-1.12.2.md)

## Historial / Previous releases

A cosmetic wardrobe with seven categories, preview, purchases, permissions and three saved outfits. The standard collection now contains 94 entries, 61 geometric models and 14 wing styles.

Armario de siete categorías con vista previa, compras, permisos y tres conjuntos. El catálogo estándar reúne 94 entradas, 61 modelos geométricos y 14 estilos de alas.

## Current release / Entrega actual — 2026-11-08

| Side / Lado | Version / Versión |
|---|---|
| Universal / Ambos lados | 1.12.1 |

**Protocol / Protocolo:** 9.

[Downloads / Descargas](https://www.curseforge.com/projects/1738048/files) · [Release / Novedades](RELEASE-2026-11-08.md) · [Configuration / Configuración](CONFIGURATION.md)

## English

Minecraft 1.20.1, Forge 47.4+, Java 17. Universal JAR; ZoneCore 2.1.0+ required only on server. Optional ZoneCrates supplies the wallet for currency purchases; free/permission access works without it. Upgrade both sides from 1.10.x/1.11.x to protocol 9.

1.12.1 includes the wing expansion and 20-piece Anime collection: 94 default cosmetics, 61 geometric models and 14 wing styles. The redesigned wardrobe offers search/filter/sort, preview rotation, confirmed purchases and three saved outfits. New entries migrate additively and start permission-locked. The camera patch automatically hides your own aura in first person, clears lingering own particles when switching camera, and restores emission in third person; remote auras and wardrobe previews remain available. Same universal JAR, protocol 9, Core 2.1.0+ server-only. Client 1.12.1 was checked against server 1.12.0; earlier protocol 8 is incompatible. Preserve catalog, permissions, ownership and saved outfits.

Open `/cosmetic`, choose a category and preview an item. Confirm purchases separately; preview never grants ownership. Use Conjuntos to save/apply one of three outfits. No setting is needed for first-person aura protection.

## Español

Minecraft 1.20.1, Forge 47.4+, Java 17. JAR universal; ZoneCore 2.1.0+ obligatorio solo servidor. ZoneCrates opcional aporta cartera para compras; acceso gratuito/por permiso funciona sin él. Desde 1.10.x/1.11.x actualiza ambos lados a protocolo 9.

1.12.1 incluye ampliación de alas y colección Anime de 20 piezas: 94 cosméticos, 61 modelos y 14 estilos de alas. Armario renovado con búsqueda/filtros/orden, giro, compra confirmada y tres conjuntos. Las entradas nuevas se añaden sin reemplazar catálogo y empiezan bloqueadas por permiso. La corrección oculta automáticamente tu aura en primera persona, retira partículas propias al cambiar cámara y restaura emisión en tercera; mantiene auras ajenas y previsualización. Universal, protocolo 9, Core 2.1.0+ solo servidor. Cliente 1.12.1 comprobado con servidor 1.12.0; protocolo 8 incompatible. Conserva catálogo, permisos, propiedad y conjuntos.

Abre `/cosmetic`, elige categoría y previsualiza. Confirma compras aparte; previsualizar no concede propiedad. Conjuntos guarda/aplica uno de tres equipos. El cuidado de aura en primera persona es automático.

## Updating / Actualizar

Stop the affected instance, back up world/configuration and replace only the previous same-mod/same-side JAR. Keep one JAR per mod per instance and preserve player data. / Detén la instancia correspondiente, respalda mundo/configuración y sustituye solo el JAR del mismo mod y lado. Conserva un JAR por mod e instancia y los datos de jugador.

## Validation scope / Alcance de verificación

1.12.0 delivery evidence includes 485 server checks, 113 controlled real-client UI checks and model/UI captures. The 1.12.1 patch records 249 programmatic checks in a real client/local-server setup. These do not establish full-modpack multiplayer gameplay, every shader or FPS/TPS.

1.12.0 registra 485 pruebas de servidor, 113 de UI real controlada y capturas de modelos/interfaz. El parche1.12.1 registra 249 comprobaciones programáticas con cliente real/servidor local. No certifican gameplay multijugador del pack, todos los shaders ni FPS/TPS.

## Rights / Derechos

Original ZONE code/assets © Elgochogms; existing third-party licenses and notices remain applicable. Public documentation repository. / Código y recursos originales ZONE © Elgochogms; se conservan licencias y avisos de terceros. Repositorio de documentación pública.
