# ElectronAngular

Ejemplo de Aplicación de escritorio con Angular y Electron

## Tecnologías

- NPM
- Angular 7
- Electron
- Electron-Builder

## Desarrollo

Para levantar el servidor de desarrollo, ejecutar: 

`npm start`

## Instalación

Ejecutar 

`npm install`

## Compilación proyecto Angular

Ejecutar 

`npm run build`

## Compilación aplicación escritorio

Primero se debe ejcutar la compilación Angular y después: 

`npm run pack:<entorno>`

Este script realizará la compilación Angular tradicional, en el entorno especificado (DEV o PROD) y el empaqueamiento de la aplicación electron (también con su entorno especificado). Los archivos quedarán en la carpeta `packaged`


## Limpiar carpetas

Para limpiar las carpetas ejecutar

`npm run clean`


## Configuración Proyecto Electron

La configuración del compportamiento de la aplicación de escritori ose puede cambiar en el archivo **package.json**. Las propiedades importantes son:

```
  "version": "0.1.0",
  "main": "main.js",
  "build": {
    "appId": "cl.hiperactivo.app",
    "productName": "MiApp",
    "directories": {
      "buildResources": "./icons/icon.icns",
      "output": "./packaged"
    },
    "mac": {
      "icon": "./icons/icon.icns",
      "category": "your.app.category.type"
    },
    "linux": {
      "icon": "./icons/icon.icns",
      "target": [
        "AppImage",
        "deb"
      ]
    },
    "win": {
      "target": "squirrel",
      "icon": "./icons/icon.ico"
    }
  },
  ```  
