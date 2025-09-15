Cómo cambiar a la rama dev y subir tus cambios sin afectar main
1. Guarda tus cambios actuales (si los hay)

Si has modificado archivos y no quieres perder esos cambios antes de cambiar de rama, guárdalos temporalmente con:

git stash


Esto “esconde” tus cambios para que puedas cambiar de rama sin problemas. Luego, cuando quieras recuperarlos, usa:

git stash pop

2. Cambia a la rama dev

Ahora muévete a la rama de desarrollo con:

git switch dev


💡 Si tu Git es más antiguo y no reconoce switch, usa:

git checkout dev

3. Verifica que estás en dev

Para asegurarte de que estás en la rama correcta, ejecuta:

git branch


Verás algo así:

  main
* dev


El asterisco * indica que ahora estás en dev.

4. Sube tus cambios a dev (sin tocar main)

Una vez que hayas hecho tus cambios y quieras subirlos al repositorio, haz:

git add .
git commit -m "Descripción breve de los cambios"
git push origin dev


Esto enviará solo los cambios de la rama dev, manteniendo main intacta.
