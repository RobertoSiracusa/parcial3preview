# Control de Proyectos - Dashboard

Sistema de gestión de proyectos con control de empleados, materiales, tareas y gastos.

## 🚀 Deploy en Render

### Configuración para Render

Este proyecto está configurado para funcionar correctamente en Render como un sitio estático. Los archivos de configuración incluidos son:

- `render.yaml` - Configuración específica para Render
- `_redirects` - Manejo de rutas para el sitio estático

### Pasos para el Deploy

1. **Conectar el repositorio a Render:**
   - Ve a [render.com](https://render.com)
   - Crea una nueva cuenta o inicia sesión
   - Haz clic en "New +" y selecciona "Static Site"
   - Conecta tu repositorio de GitHub/GitLab

2. **Configuración del sitio:**
   - **Name:** `control-proyectos` (o el nombre que prefieras)
   - **Build Command:** Dejar vacío (no es necesario para sitios estáticos)
   - **Publish Directory:** `.` (directorio raíz)
   - **Environment:** Static

3. **Configuración adicional:**
   - El archivo `render.yaml` ya está configurado
   - El archivo `_redirects` maneja las rutas correctamente

### Estructura del Proyecto

```
src/
├── css/
│   └── style.css          # Estilos principales
├── html/
│   ├── index.html         # Dashboard principal
│   ├── empleados.html     # Gestión de empleados
│   ├── materiales.html    # Gestión de materiales
│   ├── tareas.html        # Gestión de tareas
│   └── otros-gastos.html  # Gestión de gastos
├── js/
│   ├── index.js           # Script principal
│   ├── empleados.js       # Lógica de empleados
│   ├── materiales.js      # Lógica de materiales
│   ├── tareas.js          # Lógica de tareas
│   └── otros-gastos.js    # Lógica de gastos
└── storage/
    └── vectors/           # Iconos SVG
```

### Características

- ✅ **Rutas absolutas:** Todas las rutas están configuradas como absolutas para funcionar en hosting estático
- ✅ **Responsive design:** Interfaz adaptativa para móviles y desktop
- ✅ **LocalStorage:** Los datos se guardan localmente en el navegador
- ✅ **Dashboard interactivo:** Gráficos y estadísticas en tiempo real
- ✅ **Gestión completa:** CRUD para empleados, materiales, tareas y gastos

### Solución de Problemas

Si los estilos no aparecen después del deploy:

1. **Verificar rutas:** Asegúrate de que todas las rutas en los archivos HTML usen `/` al inicio
2. **Cache del navegador:** Limpia el cache del navegador o usa modo incógnito
3. **Verificar archivos:** Confirma que todos los archivos CSS y JS estén en el repositorio
4. **Logs de Render:** Revisa los logs de build en Render para identificar errores

### Desarrollo Local

Para probar localmente:

1. Clona el repositorio
2. Abre `html/index.html` en tu navegador
3. O usa un servidor local:
   ```bash
   # Con Python
   python -m http.server 8000
   
   # Con Node.js
   npx serve .
   ```

### Tecnologías Utilizadas

- HTML5
- CSS3 (con Flexbox y Grid)
- JavaScript (ES6+)
- LocalStorage para persistencia de datos
- Chart.js para gráficos
- Google Fonts (Inter)

---

**Nota:** Este proyecto utiliza almacenamiento local del navegador. Los datos no se sincronizan entre dispositivos ni se respaldan en la nube.
