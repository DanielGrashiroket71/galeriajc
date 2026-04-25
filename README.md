# 📱 PRISMA Gallery v2.0

## Características completas:

### 🖼️ Galería
- Grid ajustable (2-5 columnas)
- Filtros: Todas, Favoritos, Fotos, Videos, Recientes
- Búsqueda en tiempo real
- Selección múltiple con barra de herramientas
- Visor pantalla completa con zoom con dedos y deslizamiento
- Menú contextual (mantener presionado)
- Marcar favoritos

### 📂 Álbumes  
- Crear álbumes con nombre e ícono
- Fijar álbumes importantes
- Renombrar/eliminar álbumes
- Vista de fotos por álbum
- Mover fotos a álbumes

### 🔐 Bóveda
- PIN de 4-6 dígitos
- Soporte biométrico (huella/Face ID)
- **Carpetas dentro de la bóveda** (organización privada)
- Mover fotos entre carpetas
- Restaurar fotos a galería
- Lockout automático

### 📊 Almacenamiento
- Análisis real del almacenamiento del dispositivo
- Desglose por: fotos, videos, bóveda, álbumes
- Barra de progreso con colores de alerta
- Actualización en tiempo real

### ⚙️ Ajustes
- Cambiar PIN de bóveda
- Activar/desactivar biometría
- Tamaño de grilla
- Exportar/importar configuración
- Limpiar todos los datos

---

## 📲 Cómo convertir a APK

### Opción 1: PWA Builder (RECOMENDADO - Gratis)
1. Sube el contenido de esta carpeta a un servidor web o GitHub Pages
2. Ve a https://www.pwabuilder.com
3. Ingresa la URL de tu sitio
4. Haz clic en "Android" → "Generate Package"
5. Descarga el APK firmado
6. Instala en tu Android habilitando "Fuentes desconocidas"

### Opción 2: Trusted Web Activity (TWA)
1. Necesitas Android Studio instalado
2. Instala: `npm install -g @bubblewrap/cli`
3. Ejecuta: `bubblewrap init --manifest https://tu-url.com/manifest.json`
4. Ejecuta: `bubblewrap build`
5. Obtén el APK en la carpeta `app/build/outputs/`

### Opción 3: WebView APK manual
Usa Android Studio para crear una app simple con WebView que cargue el index.html desde assets.

### Opción 4: Capacitor (más control)
```bash
npm install @capacitor/core @capacitor/cli
npx cap init "PRISMA Gallery" "com.prisma.gallery"
npm install @capacitor/android
npx cap add android
cp -r ./* android/app/src/main/assets/public/
npx cap open android
# Luego Build > Generate Signed Bundle/APK
```

---

## 🌐 Para subir a GitHub Pages (gratis):
1. Crea repositorio en github.com
2. Sube todos los archivos
3. Ve a Settings → Pages → Source: main branch
4. Tu URL será: https://tuusuario.github.io/prisma-gallery/

## Nota de privacidad
Todas las fotos se almacenan localmente en el dispositivo usando localStorage.
Nada se sube a internet.
