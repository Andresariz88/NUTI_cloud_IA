# Portafolio Personal - Andrés Felipe Ariza Pardo

## Descripción del Proyecto

Sitio web personal tipo portafolio profesional de una sola página (single-page) que presenta mi información como Ingeniero de Sistemas. El sitio incluye secciones de presentación personal, experiencia profesional, formación académica, habilidades técnicas, proyectos realizados e información de contacto.

El diseño es limpio, moderno y completamente responsivo, optimizado para ofrecer una experiencia de usuario fluida en dispositivos móviles, tablets y escritorio.

## Tecnologías Utilizadas

- **HTML5**: Estructura semántica del sitio web
- **CSS3**: Estilos y diseño responsivo con Flexbox y Grid
- **JavaScript**: Interactividad, navegación suave y animaciones
- **Azure Static Web Apps**: Plataforma de hosting y despliegue

### Características Técnicas

- Diseño responsivo (mobile-first)
- Navegación suave entre secciones (smooth scroll)
- Animaciones al hacer scroll (Intersection Observer API)
- Resaltado dinámico del menú según la sección activa
- Optimizado para rendimiento y accesibilidad

## URL del Sitio Publicado

🌐 **[https://cv-aariza-eugphaeqbaggfteq.eastus-01.azurewebsites.net/index.html](https://cv-aariza-eugphaeqbaggfteq.eastus-01.azurewebsites.net/index.html)**


## Estructura del Proyecto

```
/
├── index.html          # Página principal
├── styles.css          # Estilos CSS
├── script.js           # Funcionalidad JavaScript
├── server.js           # Servidor Express para Azure
├── package.json        # Dependencias del proyecto
├── web.config          # Configuración IIS para Azure Windows
├── .deployment         # Configuración de despliegue
├── deploy.cmd          # Script de despliegue para Azure
├── .gitignore          # Archivos ignorados por Git
├── profile.jpg         # Foto de perfil (agregar)
└── README.md           # Este archivo
```

## Instalación y Uso Local

### Opción 1: Abrir directamente (sin servidor)

1. Clona o descarga este repositorio
2. Agrega tu foto de perfil como `profile.jpg` en la raíz del proyecto
3. Abre `index.html` en tu navegador web

### Opción 2: Con servidor Node.js (recomendado para pruebas)

1. Clona o descarga este repositorio
2. Instala las dependencias:
   ```bash
   npm install
   ```
3. Agrega tu foto de perfil como `profile.jpg` en la raíz del proyecto
4. Inicia el servidor:
   ```bash
   npm start
   ```
5. Abre tu navegador en `http://localhost:8080`

## Despliegue en Azure App Service

### Opción 1: Despliegue desde Azure Portal

1. Crea una cuenta en [Azure Portal](https://portal.azure.com)
2. Crea un nuevo recurso "App Service"
3. Configura:
   - Runtime stack: Node 18 LTS o superior
   - Sistema operativo: Linux o Windows
   - Plan de App Service según tus necesidades
4. En "Deployment Center", conecta tu repositorio de GitHub o usa despliegue local
5. Azure desplegará automáticamente tu sitio

### Opción 2: Despliegue con Azure CLI

```bash
# Instalar Azure CLI si no lo tienes
# https://docs.microsoft.com/en-us/cli/azure/install-azure-cli

# Iniciar sesión
az login

# Crear grupo de recursos
az group create --name portafolio-rg --location eastus

# Crear App Service Plan
az appservice plan create --name portafolio-plan --resource-group portafolio-rg --sku B1 --is-linux

# Crear Web App
az webapp create --resource-group portafolio-rg --plan portafolio-plan --name tu-portafolio-app --runtime "NODE|18-lts"

# Desplegar desde repositorio local
az webapp up --name tu-portafolio-app --resource-group portafolio-rg
```

### Opción 3: Despliegue con VS Code

1. Instala la extensión "Azure App Service" en VS Code
2. Haz clic derecho en la carpeta del proyecto
3. Selecciona "Deploy to Web App"
4. Sigue las instrucciones para crear o seleccionar un App Service

### Configuración Post-Despliegue

Asegúrate de que en la configuración de tu App Service:
- El comando de inicio sea: `node server.js`
- El puerto esté configurado correctamente (variable de entorno PORT)

## Contacto

- **Email**: andres.ariza70@hotmail.com
- **Teléfono**: +57 311 560 9929
- **LinkedIn**: [linkedin.com/in/andresariza](https://www.linkedin.com/in/andresariza)
- **Ubicación**: Bogotá, Colombia

---

© 2024 Andrés Felipe Ariza Pardo. Todos los derechos reservados.
