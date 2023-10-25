# extension-chrome
 
 Explicación completa
{
  "manifest_version": 3,
  "name": "Hello Extensions",
  "description": "Base Level Extension",
  "version": "1.0",
  "action": { //cada vez que entra en el botón de extensión toma el código html, el popup.html
    "default_popup": "popup.html",
    "default_icon": { //define los íconos 
      "32": "/img/mundo32.png",
      "48": "/img/mundo48.png",
      "128": "/img/mundo128.png"
    }
  },
  "icons": { //define los íconos dentro del menú de extensiones general
    "32": "/img/mundo32.png",
    "48": "/img/mundo48.png",
    "128": "/img/mundo128.png"
  },
  "content_scripts":[
    {
      "matches": ["https://www.google.com.ar/*"], //toma como match la página de Google y sus derivados. El * hace que si hacemos una búsqueda, lo reconozca como parte del dominio Google
      "js": ["content_scripts.js"]
    }
  ]
  
}