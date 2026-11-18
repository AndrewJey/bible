# Comprobar la colección OSIS

Fork personal de [gratis-bible/bible](https://github.com/gratis-bible/bible), rama `master`. Contiene traducciones en XML OSIS. Es una colección de datos, por lo que no se compila ni se ejecuta como aplicación.

Con Python 3 instalado, desde la raíz:

```powershell
python tools/validate-local.py
```

La comprobación analiza todos los XML versionados con un parser incremental y devuelve un código distinto de cero si alguno no está bien formado. No modifica traducciones, no descarga contenido y no comprueba la exactitud teológica, las licencias de cada traducción ni la conformidad completa con un esquema OSIS.

Los archivos se pueden revisar en VS Code, Sublime Text o cualquier editor XML. Para usarlos se necesita una aplicación o importador que admita OSIS; no son un proyecto de Visual Studio. Respeta la licencia y la atribución específica de cada traducción.

Se reparó `en/bwe.xml` eliminando únicamente bytes binarios y un fragmento duplicado situados después del cierre completo de la raíz XML. El contenido anterior al cierre se conserva byte por byte y el original permanece en el historial del upstream.

`origin` es el fork personal; `upstream/master` es el original y su push está deshabilitado localmente. Integra actualizaciones conservando el historial y ejecuta el validador antes de publicar.
