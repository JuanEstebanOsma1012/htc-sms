# Artículo de investigación sobre universos HTCondor hecho en LaTex.



## Configuraciones especiales de VSCode

#### Compilar en un directorio específico 
En el settings.json, para la extensión de James Yu "Latex Workshop", colocar la siguiente linea
```json
 "latex-workshop.latex.outDir": "./build",
```


## Notas

- No forzar en lo posible los saltos de linea mediante '\\\\'. En teoría, IEEEtran.cls ya maneja el espaciado. Si se quiere un salto de linea, unicamente usar un salto de linea de toda la vida dentro del archivo .tex 