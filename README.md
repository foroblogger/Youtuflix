# Youtuflix

Archivos de apoyo para una pagina estatica de Blogger con catalogo propio de peliculas y series embebidas desde YouTube.

## Objetivo

Blogger muestra la interfaz. Este repositorio guarda el catalogo editable de videos. No hace falta YouTube API ni GitHub Pages.

## Archivo principal

- `catalogo-videos.json`: catalogo editable de peliculas, series, documentales y capitulos.

## URL para Blogger

Como el repositorio es publico, Blogger puede leer el JSON desde esta URL directa:

```txt
https://raw.githubusercontent.com/foroblogger/Youtuflix/main/catalogo-videos.json
```

En el codigo de Blogger debe quedar asi:

```js
CATALOG_JSON_URL: 'https://raw.githubusercontent.com/foroblogger/Youtuflix/main/catalogo-videos.json'
```

## Editar catalogo

Anade entradas a `catalogo-videos.json` con este formato:

```json
{
  "videoId": "ID_DE_YOUTUBE",
  "title": "Titulo",
  "channel": "Canal",
  "description": "Descripcion corta",
  "publishedAt": "2024-01-01T00:00:00Z",
  "duration": "1:32:00",
  "genre": "peliculas-espanol",
  "type": "pelicula",
  "relevance": 90
}
```

Tambien puedes usar `url` en vez de `videoId`. Si `url` apunta a una busqueda o canal de YouTube, la ficha abrira YouTube en una pestana nueva.

Generos disponibles:

- `accion`
- `comedia`
- `terror`
- `ciencia-ficcion`
- `drama`
- `documentales`
- `animacion`
- `clasicos`
- `peliculas-espanol`
- `series-espanol`
- `series-latino`
- `webseries`
- `series-documentales`

## Legal

No subas ni indexes contenido que no tengas derecho a insertar. Los videos pertenecen a sus respectivos canales de YouTube.
