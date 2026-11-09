# AP 3.2 Comandos Linux - Solución

Aquí se detallan los comandos utilizados para resolver cada punto de la actividad.

### 1. Muévete a la carpeta de Sistemas
```bash
cd ~/Sistemas
```

### 2. Crea una carpeta llamada AP32
```bash
mkdir AP32
```

### 3. Crear cuatro subdirectorios (ventas, marketing, desarrollo y direccion) en un solo comando
```bash
mkdir ventas marketing desarrollo direccion
```

### 4. Reflexión sobre `mkdir a b c` vs `mkdir a/b/c`
- `mkdir a b c`: Crea tres directorios independientes llamados 'a', 'b' y 'c' en el directorio actual.
- `mkdir a/b/c`: Intenta crear el directorio 'c' dentro de 'b', que a su vez debe estar dentro de 'a'. Si los directorios 'a' y 'b' no existen previamente, el comando fallará (a menos que se use la opción `-p`, ej: `mkdir -p a/b/c`, que crea toda la ruta de directorios necesarios).

### 5. Crear ficheros en la carpeta ventas (enero, febrero y marzo)
```bash
cd ventas
touch enero febrero marzo
```

### 6. Copiar ficheros de ventas a marketing en un solo comando
```bash
cd ..
cp ventas/* marketing/
# Verificación: ls marketing/
```

### 7. Desde marketing, crear directorio del año actual (2026) en ventas y copiar ficheros
```bash
cd marketing
mkdir ../ventas/2026
cp * ../ventas/2026/
```

### 8. Desde ventas, crear directorio del año anterior (2025) y copiar ficheros de marketing que terminen en -ero
```bash
cd ../ventas
mkdir 2025
cp ../marketing/*ero .
```

### 9. Posicionada en desarrollo, copiar contenido de ventas/2025 en desarrollo/ventas_2025
```bash
cd ../desarrollo
mkdir ventas_2025
cp -r ../ventas/2025/. ventas_2025/
```

### 10. Posicionada en desarrollo, borrar el directorio ventas/2025
```bash
rm -rf ../ventas/2025
```

### 11. Posicionada en AP32, renombra desarrollo/ventas_2025 como desarrollo/ventas2025
```bash
cd ..
mv desarrollo/ventas_2025 desarrollo/ventas2025
```

### 12. Posicionada en ventas, renombra el directorio anterior como desarrollo/v_2025
```bash
cd ventas
mv ../desarrollo/ventas2025 ../desarrollo/v_2025
```
