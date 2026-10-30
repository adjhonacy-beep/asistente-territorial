# Asistente Territorial de Pasto

Aplicación web básica para consultar la base `Pasto.xlsx` por barrio, comuna, corregimiento, vereda o sector.

## Requisitos
- Python 3.10 o superior
- `Pasto.xlsx` en la misma carpeta que `app.py`

## Instalar
Abra PowerShell o Terminal dentro de esta carpeta y ejecute:

```bash
pip install -r requirements.txt
```

## Ejecutar

```bash
streamlit run app.py
```

La aplicación se abrirá en el navegador. También puede cargar una versión actualizada del Excel en el panel lateral.

## Consultas de ejemplo
- ¿A qué comuna pertenece el barrio El Tejar?
- ¿Qué barrios tiene la comuna 5?
- ¿Qué veredas tiene el corregimiento Catambuco?
- ¿A qué corregimiento pertenece la vereda La Cadena?

## Limitación de direcciones
La hoja actual contiene ZONA, COMUNA, BARRIO, CORREGIMIENTO, VEREDA y SECTOR, pero no una columna de dirección ni coordenadas/rangos de vías. Por tanto, esta versión no puede ubicar una dirección exacta. Para ello se necesita una tabla de direcciones o cartografía territorial validada.

## Actualizaciones
Al cambiar el archivo guardado `Pasto.xlsx`, reinicie la aplicación si no se refleja el cambio. Si se carga una versión desde el panel lateral, se usa esa versión durante la sesión.

## Importante
Este prototipo usa búsqueda determinista sobre el Excel; no requiere una clave API ni envía los datos a un proveedor externo. Para uso compartido en internet, configure autenticación y controles de acceso antes de publicar la aplicación.
