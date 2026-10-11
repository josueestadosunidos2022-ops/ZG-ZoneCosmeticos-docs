# ZG ZoneCosmeticos — releases / entregas

## 1.10.1 protected candidate / candidato protegido

- Minecraft 1.20.1, Forge 47.4+, Java 17. **One universal JAR on client and server**; ZoneCore `[2.1.0,)` required on the server. Network protocol 7; use matching 1.10.1 on both sides.
- `zonecosmeticos-1.10.1-protected.jar` SHA-256: `F38D8BF006064888B8BC72AD81510D8A2F0C0D7CA6FBF1C5151587FE8BB5E3BE`.
- New 1.10.1 distribution metadata identifies Elgochogms. Gameplay and protocol are unchanged from 1.10.0. The original 1.10.0 guide reported 240 Forge fixture checks and a controlled graphical review of GUI scales 2–4; **those results do not directly test this protected 1.10.1 JAR**.
- 1.10.1 Gradle build and `modelCheck` passed: 43 styles baked, 358 material meshes. ProGuard completed, with no Java sources or mapping embedded. The exact protected JAR started with protected ZoneCore 2.1.3 and ZoneCrates 2.0.6 on isolated Forge 47.4.10; `/cosmetic` registered, `/cosmetic reload` responded, and shutdown was clean.
- Client rendering, purchase transactions, saved outfits in multiplayer, complete modpack and production hosting have not been tested with the protected 1.10.1 JAR. CurseForge upload and moderation remain pending.

## Español

La entrega 1.10.1 es un único JAR protegido para ambos lados, con autor Elgochogms y licencia All Rights Reserved. Conserva el protocolo 7 y las funciones de 1.10.0. Pasó compilación, revisión de modelos y arranque/comandos/cierre de servidor aislado; todavía faltan cliente gráfico, compras, multijugador, modpack completo y hosting con este JAR exacto. La carga a CurseForge sigue pendiente; comprueba el SHA-256 y respalda el mundo antes de instalar.

