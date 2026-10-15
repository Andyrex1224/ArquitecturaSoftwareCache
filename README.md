# Ferretería: comparación con y sin caché

- **Backend:** Java + Spring Boot. Lee 10.000 productos de MySQL y guarda los resultados en una caché en memoria.
- **Frontend:** una página web que consulta los productos con caché y sin caché, y compara los tiempos con dos barras.

## Cómo ejecutar

### 1. Base de datos (en tu propio computador)

La base de datos **no está en internet**: tiene que crearse en **MySQL instalado en tu propio computador**.

1. Abre **MySQL Workbench** y conéctate como `root`.
2. Abre el script `Base Datos Ferreteria/FerreteriaDB.sql`, que está en este repositorio.
3. Ejecuta completo el script.

Esto crea la base `ferreteria`, los 10.000 productos y el usuario `usuario_ferreteria`.

### 2. Backend

1. Abre la carpeta del proyecto en **IntelliJ IDEA**.
2. Abre `ferreteria-backend/src/main/java/com/ferreteria/Main.java`.
3. Pulsa ▶ **Run 'Main'**.

### 3. Frontend

En una terminal, dentro de la carpeta `ferreteria-frontend`:

```bash
python -m http.server 5173
```

Abre **http://localhost:5173** y prueba los botones **sin caché** y **con caché**.
