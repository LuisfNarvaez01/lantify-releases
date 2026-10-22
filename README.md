# Lantify POS — Instaladores

Este repositorio **solo contiene instaladores** de Lantify POS publicados en
[Releases](../../releases). No contiene código fuente.

Desde la versión 2.0, la aplicación instalada consulta este repositorio para buscar
actualizaciones automáticas.

## Instalación

1. Descarga `Lantify-Setup-<versión>.exe` desde la última release.
2. (Recomendado) Verifica el archivo comparando su SHA-256 con el publicado en las notas de la release:
   ```powershell
   Get-FileHash .\Lantify-Setup-<versión>.exe -Algorithm SHA256
   ```
3. Ejecuta el instalador. El instalador no está firmado con un certificado comercial, así que
   Windows mostrará **"Windows protegió su PC"**: haz clic en **Más información → Ejecutar de todos modos**.
4. Si el antivirus pone el archivo en cuarentena, agrega una exclusión para la carpeta de instalación.

## Integridad de las actualizaciones

Cada release incluye `latest.yml` con el hash SHA-512 del instalador y una firma Ed25519 propia de
Lantify. La aplicación rechaza cualquier actualización que no esté firmada con la clave oficial.

## Soporte

La instalación en equipos de clientes la realiza personalmente el equipo de Lantify.
