# extension-chrome
 
Esta extensión tiene la finalidad de cambiar el color de fondo de la página de Google + sus búsquedas.

 Explicación del manifest

  "action": { //cada vez que entra en el botón de extensión toma el código html, el popup.html
  <br>
    "default_popup": "popup.html",
    <br>
    "default_icon": { //define los íconos 
    <br>
      "32": "/img/mundo32.png", //32 es el tamaño, podemos setear varios
    }
  },
  <br>
  "icons": { //define los íconos dentro del menú de extensiones general
  <br>
    "32": "/img/mundo32.png",
  },
  <br>
  "content_scripts":[
    {
      "matches": ["https://www.google.com.ar/*"], //toma como match la página de Google y sus derivados. El * hace que si hacemos una búsqueda, lo reconozca como parte del dominio Google
      <br>
      "js": ["content_scripts.js"]
    }
  ]
  
