# Curso de VFP Visual FoxPro (VFP)

La edicion de los capitulos del libro se hace en el folder **src**

[Ver el Indice](./src/SUMMARY.md)

Usaremos la herramienta mdbook, para generar el libro en PDF y como consulta en HTML
Para conocer mas sobre mdbook revisar: https://rust-lang.github.io/mdBook/

Para generar el libro usar el comando:
```

cd repository-folder
docker-compose run --rm mdbook build
2022-09-28 17:22:14 [INFO] (mdbook::book): Book building has started
2022-09-28 17:22:14 [INFO] (mdbook::book): Running the html backend

```
Esto genera en el folder book, con la estructura del libro en formato HTML

Para ver el libro, usar el navegador para abrir el archivo **book/index.html**
