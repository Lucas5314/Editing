

```html
<!DOCTYPE html>
<html>
<head>
<title>Reproductor de Música</title>
<style>
  body {
    font-family: sans-serif;
  }
  .container {
    display: flex;
    flex-direction: column;
    align-items: center;
  }
  .player-controls {
    display: flex;
  }
  .player-controls button {
    margin: 0 10px;
  }
</style>
</head>
<body>
<div class="container">
  <h1>Reproductor de Música</h1>
  <audio id="audio-player" controls>
    Tu navegador no admite la etiqueta de audio.
  </audio>
  <div class="player-controls">
    <button id="play-button">Reproducir</button>
    <button id="pause-button">Pausar</button>
    <button id="stop-button">Detener</button>
  </div>
</div>

<script>
  const audioPlayer = document.getElementById('audio-player');
  const playButton = document.getElementById('play-button');
  const pauseButton = document.getElementById('pause-button');
  const stopButton = document.getElementById('stop-button');

  playButton.addEventListener('click', () => {
    audioPlayer.play();
  });

  pauseButton.addEventListener('click', () => {
    audioPlayer.pause();
  });

  stopButton.addEventListener('click', () => {
    audioPlayer.pause();
    audioPlayer.currentTime = 0;
  });
</script>
</body>
</html>
```

**Explicación:**

1. **HTML:**
   - Se crea una etiqueta `<audio>` con el atributo `controls` para mostrar los controles de reproducción predeterminados.
   - Se agregan botones para "Reproducir", "Pausar" y "Detener".

2. **JavaScript:**
   - Se obtienen referencias a los elementos del reproductor de audio y los botones.
   - Se agregan eventos `click` a los botones:
     - **Reproducir:** Llama a `audioPlayer.play()`.
     - **Pausar:** Llama a `audioPlayer.pause()`.
     - **Detener:** Llama a `audioPlayer.pause()` y `audioPlayer.currentTime = 0` para reiniciar la reproducción.

**Para usar este código:**

1. Guarda el código como un archivo HTML (por ejemplo, `reproductor.html`).
2. Abre el archivo en un navegador web.
3. Puedes agregar tus propias canciones al elemento `<audio>` como fuente:
   ```html
   <audio id="audio-player" controls>
     <source src="tu_cancion.mp3" type="audio/mpeg">
     Tu navegador no admite la etiqueta de audio.
   </audio>
   ```

**Recuerda:**

- Reemplaza `tu_cancion.mp3` con la ruta de tu archivo de audio.
- Puedes agregar más funciones como la selección de canciones, control de volumen, etc.

Espero que este código básico te ayude a comenzar con tu aplicación de reproducción de música. ¡Si necesitas ayuda con funcionalidades adicionales, no dudes en preguntar!

Este mensaje ha sido generado por Nova - descárgalo gratis: https://novaappai.page.link/ZhRpSJeqjCYgxGHS9
