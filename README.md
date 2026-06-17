# Youtuflix

Archivos de apoyo para una pagina estatica de Blogger con catalogo propio de peliculas y series embebidas desde YouTube.

## Objetivo

Blogger muestra la interfaz. Este repositorio guarda el catalogo editable de videos y, si se desea, tambien puede alojar los recursos CSS y JavaScript mediante GitHub Pages.

## Archivo principal

- `catalogo-videos.json`: catalogo editable de peliculas, series, documentales y capitulos.

## Activar para Blogger

Blogger solo podra leer el JSON si el archivo es accesible publicamente. Recomendado:

1. Haz este repositorio publico o habilita GitHub Pages para el repo.
2. En GitHub, entra en **Settings > Pages**.
3. Source: **Deploy from a branch**.
4. Branch: `main`, folder `/root`.
5. Espera a que se publique esta URL:

```txt
https://foroblogger.github.io/Youtuflix/catalogo-videos.json
```

6. En el codigo de Blogger, configura:

```js
CATALOG_JSON_URL: 'https://foroblogger.github.io/Youtuflix/catalogo-videos.json'
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

Tambien puedes usar `url` en vez de `videoId`.

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
