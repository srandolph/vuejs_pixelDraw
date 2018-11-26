# pixel

## Project setup
```
npm install
```

### Compiles and hot-reloads for development
```
npm run serve
```

### Compiles and minifies for production
```
npm run build
```

### Run your tests
```
npm run test
```

### Lints and fixes files
```
npm run lint
```

### Customize configuration
See [Configuration Reference](https://cli.vuejs.org/config/).


https://medium.com/codeartisan/how-to-run-nuxt-js-on-digitalocean-159fc558d2ab

server {
    listen 80;
    listen [::]:80;
    index index.html;
    server_name pixel.indiecio.net;

    location / {
        proxy_pass http://localhost:3000;
        proxy_http_version 1.1;
        proxy_set_header Upgrade $http_upgrade;
        proxy_set_header Connection 'upgrade';
        proxy_set_header Host $host;
        proxy_cache_bypass $http_upgrade;
    }
}

https://github.com/srandolph/vuejs_pixelDraw.git