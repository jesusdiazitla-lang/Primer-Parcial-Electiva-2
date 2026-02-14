Proyecto CI/CD con GitHub Actions y Surge.sh
Este proyecto demuestra la integración continua y despliegue automático usando GitHub Actions y Surge.sh.
🚀 Configuración Inicial
1. Instalar Surge.sh localmente
bashnpm install -g surge
2. Crear cuenta y obtener token de Surge
bash# Crear cuenta (solo la primera vez)
surge login

# Obtener tu token
surge token
Guarda el token que aparece, lo necesitarás para GitHub.
3. Configurar Secrets en GitHub
Ve a tu repositorio en GitHub:

Click en Settings (Configuración)
En el menú lateral, click en Secrets and variables → Actions
Click en New repository secret
Crea dos secrets:
Secret 1:

Name: SURGE_TOKEN
Value: (pega el token que obtuviste con surge token)

Secret 2:

Name: SURGE_DOMAIN
Value: tu-nombre-proyecto.surge.sh (elige un nombre único)



4. Estructura del Proyecto
Primer-Parcial-Electiva-2/
├── .github/
│   └── workflows/
│       └── main.yml          # Configuración de GitHub Actions
├── index.html                 # Página web principal
└── README.md                  # Este archivo
5. Comandos Git
bash# Agregar archivos
git add .

# Hacer commit
git commit -m "Configurar CI/CD con GitHub Actions y Surge.sh"

# Subir a GitHub (esto activará el despliegue automático)
git push origin main
📋 Cómo Funciona

Haces cambios en tu código local
Ejecutas git push a GitHub
GitHub Actions detecta el push automáticamente
Se ejecuta el workflow que:

Instala Node.js
Instala Surge
Despliega tu sitio a Surge.sh


Tu sitio está disponible en: https://tu-nombre-proyecto.surge.sh

🔍 Verificar el Despliegue

Ve a la pestaña Actions en tu repositorio de GitHub
Verás el workflow ejecutándose
Click en el workflow para ver los detalles
Una vez completado (✓), visita tu dominio de Surge

🛠️ Probar Localmente con Surge
bash# Desplegar manualmente desde tu computadora
surge ./ tu-nombre-proyecto.surge.sh
📝 Notas Importantes

El dominio de Surge debe ser único en todo Surge.sh
Los secrets de GitHub están encriptados y seguros
Cada push a la rama main o master activará un nuevo despliegue
Puedes ver los logs de despliegue en la pestaña Actions de GitHub

🎓 Tecnologías Utilizadas

Git: Control de versiones
GitHub: Repositorio remoto
GitHub Actions: CI/CD pipeline
Surge.sh: Hosting estático
HTML/CSS: Página web

✅ Checklist de Verificación

 Repositorio local creado
 Archivo index.html creado
 Repositorio en GitHub creado
 Directorio .github/workflows creado
 Archivo main.yml configurado
 Surge.sh instalado localmente
 Token de Surge obtenido
 Secrets configurados en GitHub
 Push a GitHub realizado
 Despliegue verificado en Surge.sh


Desarrollado para Electiva 2 - Primer Parcial 🎓