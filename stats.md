### ESTADISTICAS
## 1. Integrante que realizó la mayor cantidad de commits:
> git shortlog -sn --all

Resultado: 19. valenvitale

Explicación:
git shortlog genera un resumen de commits agrupados por autor.
-s muestra solamente la cantidad de commits.
-n ordena de mayor a menor cantidad.
--all considera todas las ramas del repositorio.

## 2. Cantidad total de merges realizados:
> git log --merges --oneline | wc -l

Resultado: 18

git log muestra el historial de commits.
--merges filtra unicamente los commits de tipo merge.
--oneline muestra cada commit en una sola linea.
| envia el resultado al siguiente comando.
wc -l cuenta la cantidad de líneas recibidas.
Como cada merge aparece en una linea el resultado es la cantidad totala de merges.

## 3. Cantidad de conflictos producidos:
No hay un commit como tal para contabilizar la cantidad de conflictos, ni github posee de un historial, pero si se puede contar manualmente.
Nosotros tuvimos unicamente un conflicto en la carpeta "7. Cambio y Creación de Ramas" donde dentro habia una subcarpeta llamada "Switch.".
El punto al final del nombre nos ocasionó problemas al momento de hacer un git pull, y la solucion fue renombrar el directorio pero otra persona habia subido cambios, git no supo con cual version quedarse y genero un conflicto en el que habia que elegir.

## 4. Cantidad de ramas existentes:
> git branch -a | wc -l

Resultado: 19 ramas

git branch -a lista todas las ramas.
| wc -l cuenta cuantas lineas tiene la lista.

## 5. Commit con mayor cantidad de archivos modificados:
> git log --stat
Para encontrar el commit con mas archivos modificados.
Despues se muestra el detalle con:
> git show HASH

Resultado: 37e727e - 3 archivos.
![Captura del diff](/assets/stat5.png)

## 6. Captura de un conflicto previo a su resolución:
![Captura git status](/assets/conflicto.png)
hash: 880b7d7