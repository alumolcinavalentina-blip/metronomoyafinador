# 🎵 Herramientas Musicales

Metrónomo y afinador cromático en HTML puro, sin dependencias.

## Archivos

| Archivo | Descripción |
|---|---|
| `metronomo.html` | Metrónomo con péndulo, tempo tap, compás configurable y click de audio |
| `afinador.html` | Afinador cromático con detección de pitch por micrófono |

## Características comunes

- **Fondo aleatorio** al abrir la página (paleta oscura, tonos ricos)
- **⋮ Menú de color** (arriba a la derecha): cambia el fondo con presets, color personalizado o aleatório
- Sin frameworks, sin dependencias — un único archivo HTML cada uno

## Metrónomo

- BPM de 20 a 240 con slider y botones ±5
- **Tap tempo**: haz clic sobre el número de BPM para marcar el pulso
- Teclado: `Espacio` = play/stop, `↑↓` = ±1 BPM
- Compases: 4/4 · 3/4 · 6/8 · 2/4
- Acento visual y sonoro en el primer tiempo
- Péndulo animado sincronizado al tempo
- Click generado con Web Audio API (sin archivos externos)

## Afinador

- Detección de pitch por **autocorrelación** sobre el micrófono
- Rango útil: 50 Hz – 2000 Hz (cubre guitarra, bajo, voz, viento...)
- Medidor de **cents** con aguja en tiempo real
  - 🟢 Verde: ±5¢ — afinado
  - 🟡 Amarillo: ±15¢ — cerca
  - 🔴 Rojo: >±15¢ — desafinado
- **Notas de referencia** para guitarra estándar (E2–E4): toca el botón y suena el tono durante 2,5 s
- Requiere permiso de micrófono en el navegador

## Uso

Abre cada `.html` directamente en el navegador o sírvelo con cualquier servidor estático.

```bash
# Ejemplo rápido con Python
python3 -m http.server 8000
```

Luego visita `http://localhost:8000/metronomo.html` o `http://localhost:8000/afinador.html`.

## Compatibilidad

Funciona en Chrome, Firefox, Safari y Edge modernos.  
El afinador requiere HTTPS (o `localhost`) para acceder al micrófono.
