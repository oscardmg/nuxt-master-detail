# nuxt-master-detail

> ejemplo de factura encabezado detalle master detail
[Tutorial url](https://github.com/CodAffection/Angular-7-Master-Detail-CRUD-with-Web-API)

# subir a githubpages
[tutorial](https://medium.com/@ianaya89/crea-tu-sitio-web-con-github-pages-y-nuxt-js-6a90fd0a0dc4)
modificar package.json
```
"scripts": {
  // otros scripts (no borrarlos)
  
  "deploy": "push-dir --dir=dist --branch=gh-pages --cleanup"
}
```
Modificar nuxt.config.js y adicionar para que no genere error the server responded with a status of 404
```
router: {
  base: '/nuxt-master-detail/'
},
```

## Build Setup



``` bash
# install dependencies
$ npm install

# serve with hot reload at localhost:3000
$ npm run dev

# build for production and launch server
$ npm run build
$ npm start

# generate static project
$ npm run generate
```

For detailed explanation on how things work, checkout [Nuxt.js docs](https://nuxtjs.org).
