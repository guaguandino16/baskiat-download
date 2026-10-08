<p align="center">
  <picture>
    <source media="(prefers-color-scheme: dark)" srcset="baskiat-logo-white.svg">
    <img src="baskiat-logo-black.svg" alt="BASKIAT" width="360">
  </picture>
</p>

<p align="center"><b>Visuales en vivo que tocas como un instrumento.</b><br>
Escenas que lanzas al compás, capas que modelas a mano y agentes de IA que hacen el trabajo pesado mientras tú mantienes el flujo creativo.</p>

<p align="center">
  <a href="https://github.com/guaguandino16/baskiat-download/releases/latest"><b>⬇ Descargar la última versión</b></a>
</p>

---

## Descarga

| Sistema | Archivo | Requisitos |
|---|---|---|
| **macOS** | `BASKIAT-<versión>-arm64.dmg` | Mac con Apple Silicon (M1 o posterior), macOS 13 (Ventura) o superior |
| **Windows** | `BASKIAT-Setup-<versión>.exe` | Windows 10 u 11 de 64 bits |

Los dos están en la página de [Releases](https://github.com/guaguandino16/baskiat-download/releases/latest), en la sección **Assets**.

> BASKIAT todavía no está firmado por Apple ni por Microsoft, así que la primera vez el sistema pide confirmación. Abajo se explica cómo hacerlo; solo se hace una vez.

## Instalar en Mac

1. Descarga el `.dmg` y ábrelo con doble clic.
2. Arrastra **BASKIAT** a la carpeta **Applications** (Aplicaciones).
3. Abre BASKIAT desde Aplicaciones. macOS dirá que no puede comprobar la app: pulsa **Hecho**.
4. Ve a **Ajustes del Sistema → Privacidad y seguridad**, baja hasta el aviso de BASKIAT y pulsa **Abrir igualmente**. Confirma con tu contraseña o Touch ID.
5. Cuando BASKIAT lo pida, permite el **micrófono** (para que los visuales reaccionen al sonido) y la **cámara** si la vas a usar.

<details>
<summary>Si macOS dice que la app “está dañada”</summary>

Ocurre a veces con apps descargadas que no están firmadas. Abre la app **Terminal** y pega esta línea:

```bash
xattr -dr com.apple.quarantine /Applications/BASKIAT.app
```

Después abre BASKIAT de nuevo.
</details>

## Instalar en Windows

1. Descarga `BASKIAT-Setup-<versión>.exe` y ábrelo.
2. Si aparece **Windows protegió tu PC** (SmartScreen), pulsa **Más información → Ejecutar de todas formas**.
3. Se instala solo y abre BASKIAT. Lo encontrarás en el menú Inicio y en el escritorio.
4. Si Windows pregunta por el **Firewall**, permite el acceso en redes privadas: lo usan Ableton Link, OSC, NDI y el control desde otro ordenador.

## Primeros pasos

- **Tour de bienvenida**: se abre la primera vez y explica todo, paso a paso. Vuelve a verlo en **Menú → How it works**.
- **Empieza un set**: *Start a set* → elige el **Demo set** → **A/V Performance**.
- **Pantalla de salida**: pulsa **Output** (`O`), arrastra la ventana al proyector y ponla a pantalla completa.
- **Atajos**: `Espacio` play · `L` capas · `B` biblioteca · `C` código · `S` setlist · `P` parámetros · `M` motion · `O` output · `T` patrón de prueba.

## Activar los agentes de IA

BASKIAT trae un agente (el orbe de abajo a la derecha) con especialistas: **Visuals**, **Motion** y **Show**. Para usarlos necesitas una clave de un proveedor de IA. Se guarda solo en tu ordenador.

| Proveedor | Dónde conseguir la clave | Coste |
|---|---|---|
| **Gemini** | [aistudio.google.com/apikey](https://aistudio.google.com/apikey) → *Create API key* (empieza por `AIza`) | Tiene nivel gratuito |
| **Claude** | [platform.claude.com](https://platform.claude.com) → *API keys* (empieza por `sk-ant-api03-`) | De pago, con créditos. La suscripción a Claude no incluye la API |
| **OpenRouter** | [openrouter.ai](https://openrouter.ai) → *Keys* (empieza por `sk-or-v1-`) | De pago, con créditos. Da acceso a Claude, Gemini y otros |

En BASKIAT: **orbe → ⚙ → elige el proveedor → pega la clave → Save**.
Para OpenRouter elige **Custom**, con dirección `https://openrouter.ai/api/v1` y un modelo como `google/gemini-3.8-flash` o `anthropic/claude-sonnet-5.5`.

Después: elige el agente, escribe lo que imaginas (o toca una sugerencia), pulsa **✨** para mejorar el texto y arrastra imágenes de referencia al panel. Cada cambio llega como una tarjeta: **Apply** o **Dismiss**.

## Opcional

- **NDI** (enviar la imagen por red): instala [NDI Tools](https://ndi.video/tools/).
- **MIDI virtual**: en Mac, el driver IAC (Configuración de Audio MIDI); en Windows, [loopMIDI](https://www.tobias-erichsen.de/software/loopmidi.html).
- **Ableton Live**: BASKIAT sigue el tempo de Live por Ableton Link.

## Actualizar

Descarga la versión nueva e instálala encima: en Mac, reemplaza la app en Aplicaciones; en Windows, ejecuta el nuevo instalador. **Tus proyectos y claves se conservan**. Viven en `~/Library/Application Support/BASKIAT` (Mac) y en `%APPDATA%\BASKIAT` (Windows).

Para mover un proyecto a otro ordenador: **Menú → Export .avshow**, y en el otro **Menú → Open .avshow…**.

## Problemas frecuentes

- **Los agentes dan error 401**: la clave no es válida o no es una clave de API. Error **402**: tu cuenta no tiene saldo. **503 / high demand**: el modelo está saturado; prueba otra vez o cambia de modelo.
- **No reacciona al sonido**: activa **Audio** arriba y permite el micrófono (Mac: Ajustes → Privacidad y seguridad → Micrófono).
- **Mac con Intel**: por ahora BASKIAT solo funciona en Apple Silicon.

---

<details>
<summary><b>English</b></summary>

**BASKIAT** — live visuals you play like an instrument.

- **Download** the `.dmg` (Mac, Apple Silicon, macOS 13+) or the `.exe` (Windows 10/11, 64-bit) from [Releases](https://github.com/guaguandino16/baskiat-download/releases/latest).
- **Mac**: open the DMG and drag BASKIAT to Applications. On first launch macOS blocks it because it is not notarized: go to *System Settings → Privacy & Security → Open Anyway*. If it says the app is damaged, run `xattr -dr com.apple.quarantine /Applications/BASKIAT.app` in Terminal.
- **Windows**: run the installer. On *Windows protected your PC*, choose *More info → Run anyway*. Allow private-network access in the firewall prompt.
- **First steps**: the welcome tour opens on first launch (Menu → How it works to see it again).
- **AI agents**: orb → ⚙ → pick Gemini (free key at aistudio.google.com/apikey), Claude (platform.claude.com) or Custom (OpenRouter: `https://openrouter.ai/api/v1`) → paste the key → Save.
- **Updating** keeps your projects and keys.
</details>
