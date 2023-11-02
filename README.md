# Plugin.Maui.Feature Plantilla

El repositorio `Plugin.Maui.Feature` es un repositorio de plantillas que se puede utilizar para iniciar su propio proyecto de complemento .NET MAUI. Puede utilizar esta estructura de proyecto como modelo para su propio trabajo.

Aprenda cómo comenzar con su complemento en este [video de YouTube](https://www.youtube.com/watch?v=ZCQrlGT7MhI&list=PLfbOp004UaYVgzmTBNVI0ql2qF0LhSEU1&index=27).

Esta plantilla contiene:

- Una [aplicación .NET MAUI de muestra] (muestras) donde puede demostrar cómo funciona su complemento y probarlo mientras lo desarrolla
- La [fuente](src) del complemento
- Un [archivo REDME] (README_Feature.md) repetitivo que puedes usar (¡no olvides cambiarle el nombre a `README.md` y eliminar este!)
- [Acciones de GitHub para CI](.github/workflows) de la biblioteca y la aplicación de muestra
- [Acción de GitHub para publicar](.github/workflows) su paquete en NuGet
- Un [icono genérico](nuget.png) para tu proyecto, ¡siéntete libre de adaptarlo y ser creativo!
- Un archivo [.editorconfig](.editorconfig) para estandarizar la sintaxis del código. Siéntase libre de adaptarlo o eliminarlo.
- El fichero [LICENCIA](LICENCIA) con la licencia MIT. Si quieres que esto sea diferente, cámbialo. ¡Al menos agrega tu nombre allí!

## Empezando

1. Cree su propio repositorio de GitHub a partir de este haciendo clic en el botón "Usar esta plantilla" y luego en "Crear un nuevo repositorio". Más información en la [documentación](https://docs.github.com/repositories/creating-and-managing-repositories/creating-a-repository-from-a-template). Después de eso, clona el repositorio en tu máquina local.

2. Reemplace todas las apariciones de `Plugin.Maui.Feature` con cualquiera que sea su característica o funcionalidad. Por ejemplo: `Plugin.Maui.ScreenBrightness` o `Plugin.Maui.Audio`. Por supuesto, el nombre puede ser cualquier cosa, pero para hacerlo más reconocible podría ser una excelente opción ceñirse a este esquema de nombres. Puede hacer esto fácilmente con su editor de texto favorito y reemplazar todo en todos los archivos.

    2.1 No olvide cambiar también el nombre de los archivos y carpetas de su sistema de archivos.

3. En el archivo csproj del proyecto del complemento (en `src`), asegúrese de reemplazar todos los valores relevantes para su proyecto. Esto significa el autor de este proyecto, la descripción del proyecto, el marco de destino (.NET 7, 8 o algo más). Si no desea o no puede admitir una determinada plataforma, elimine esa plataforma de destino por completo.

4. Elimine este archivo `README.md` y cambie el nombre de `README_Feature.md` a `README.md`. Llene ese archivo README con todos los detalles relevantes de su proyecto.

5. Verifique el archivo LICENCIA si refleja la licencia bajo la cual desea distribuir su proyecto. Al menos agrega tu nombre allí y el año actual en el que vivimos.

6. Cree un icono agradable en el archivo `nuget.png` que aparecerá en nuget.org y en el administrador de NuGet en Visual Studio.

7. Escriba el código de su complemento (en `src`) y agregue muestras a la aplicación de muestra .NET MAUI (en la carpeta `samples`)

8. ¡Asegúrese de que su paquete no aparezca como `Plugin.Maui.Feature` en NuGet! Si lo hace, ¡me debes un trago!

9. Publique su paquete en NuGet. Puede encontrar una buena guía para hacerlo [aquí](https://learn.microsoft.com/nuget/nuget-org/publish-a-package). Consulte también [Publicar en NuGet](#publish-to-nuget) a continuación.

10. ¡Disfruta de la vida como autor de complementos .NET MAUI! ✨

Como ejemplo de todo esto puedes echar un vistazo a:

- [Plugin.Maui.Audio](https://github.com/jfversluis/Plugin.Maui.Audio)
- [Plugin.Maui.Pedómetro](https://github.com/jfversluis/Plugin.Maui.Pedómetro)
- [Plugin.Maui.ScreenBrightness](https://github.com/jfversluis/Plugin.Maui.ScreenBrightness)

## Publicar en NuGet

Si desea publicar su paquete en NuGet, ¡puede hacerlo! En esta plantilla se incluyen un par de acciones de GitHub. Uno de ellos desaparece cuando crea una nueva etiqueta con este patrón: `v1.0.0` o `v1.0.0-preview1`. Obviamente, usted puede determinar la parte `1.0.0` como mejor le parezca, siempre y cuando siga el patrón de 3 números enteros separados por puntos.

También querrá establecer un secreto para este repositorio que contenga su clave API de NuGet. Siga la documentación al respecto [aquí](https://docs.github.com/actions/security-guides/encrypted-secrets#creating-encrypted-secrets-for-a-repository) y agregue un secreto con la clave ` NUGET_API_KEY` y el valor de su clave API de NuGet. La clave API debe estar autorizada para enviar un paquete NuGet con el identificador proporcionado.

A partir de ahí, después de [crear una versión de GitHub](https://docs.github.com/repositories/releasing-projects-on-github/managing-releases-in-a-repository), su complemento se lanzará automáticamente en NuGet.
