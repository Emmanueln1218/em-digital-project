[README-Access.md](https://github.com/user-attachments/files/26792093/README-Access.md)
# Cómo Hacer Visible EM-DIGITAL desde Cualquier Parte del Mundo

## Opción 1: Usar Ngrok (Recomendado - Gratis y Fácil)

### Paso 1: Descargar Ngrok
```bash
# Descargar ngrok para Windows
# Ir a https://ngrok.com/download y descargar la versión para Windows
# O usar PowerShell:
Invoke-WebRequest -Uri "https://bin.equinox.io/c/bNyj1mQVY4c/ngrok-v3-stable-windows-amd64.zip" -OutFile "ngrok.zip"
Expand-Archive -Path "ngrok.zip" -DestinationPath "." -Force
```

### Paso 2: Configurar Ngrok
```bash
# Registrar cuenta gratuita en https://ngrok.com/signup
# Obtener authtoken desde tu dashboard
./ngrok config add-authtoken TU_AUTHTOKEN_AQUI
```

### Paso 3: Iniciar Servidor Local
```bash
# Iniciar servidor web en puerto 8000
python -m http.server 8000 --bind 0.0.0.0
```

### Paso 4: Crear Túnel Ngrok
```bash
# En otra terminal, ejecutar:
./ngrok http 8000
```

### Paso 5: Compartir URL Pública
Ngrok te dará una URL como:
- `https://random-words.ngrok.io`

Esta URL será accesible desde cualquier parte del mundo.

---

## Opción 2: Usar GitHub Pages (Gratis y Permanente)

### Paso 1: Crear Repositorio GitHub
1. Ve a https://github.com y crea un nuevo repositorio
2. Nombra el repositorio: `em-digital-project`

### Paso 2: Subir Archivos
```bash
git init
git add EM-DIGITAL-Presentation.html
git commit -m "Initial commit"
git branch -M main
git remote add origin https://github.com/tu-usuario/em-digital-project.git
git push -u origin main
```

### Paso 3: Activar GitHub Pages
1. En tu repositorio GitHub, ve a Settings
2. En la sección "Pages", selecciona "Deploy from a branch"
3. Elige la rama "main" y carpeta "/root"
4. Guarda y espera unos minutos

### Paso 4: Acceder
Tu sitio estará disponible en:
`https://tu-usuario.github.io/em-digital-project/`

---

## Opción 3: Usar Netlify (Gratis y Fácil)

### Paso 1: Ir a https://netlify.com
1. Crea cuenta gratuita
2. Arrastra el archivo `EM-DIGITAL-Presentation.html` al sitio

### Paso 2: Obtener URL
Netlify te dará una URL como:
`https://amazing-name-123456.netlify.app`

---

## Opción 4: Usar Vercel (Gratis y Profesional)

### Paso 1: Ir a https://vercel.com
1. Crea cuenta gratuita
2. Importa tu proyecto
3. Sube el archivo HTML

### Paso 2: Obtener URL
Vercel te dará una URL como:
`https://em-digital-project.vercel.app`

---

## Opción 5: Configurar Firewall y Router (Avanzado)

### Paso 1: Configurar Firewall de Windows
```bash
# Permitir entrada en puerto 8000
New-NetFirewallRule -DisplayName "HTTP Server" -Direction Inbound -Protocol TCP -LocalPort 8000 -Action Allow
```

### Paso 2: Configurar Router
1. Accede a tu router (usualmente 192.168.1.1)
2. Busca "Port Forwarding" o "Reenvío de Puertos"
3. Configura:
   - Puerto externo: 8000
   - Puerto interno: 8000
   - IP interna: 192.168.150.114 (tu IP)
4. Guarda configuración

### Paso 3: Obtener IP Pública
Visita https://whatismyipaddress.com para obtener tu IP pública.

### Paso 4: Compartir URL
`http://TU_IP_PUBLICA:8000`

---

## Recomendación Final

**Para acceso inmediato y fácil:** Usa **Ngrok**
**Para acceso permanente y profesional:** Usa **GitHub Pages** o **Netlify**

## Seguridad Adicional

Si usas Ngrok o GitHub Pages, considera:
- Añadir contraseña si es información sensible
- Usar HTTPS (viene incluido en estas opciones)
- Monitorear quién accede al sitio

## URLs para Compartir

Una vez configurado, podrás compartir:
- **Ngrok:** `https://random-words.ngrok.io`
- **GitHub Pages:** `https://tu-usuario.github.io/em-digital-project/`
- **Netlify:** `https://amazing-name-123456.netlify.app`

Cualquiera de estas URLs funcionará desde cualquier parte del mundo.
