# 🚀 Guía de Configuración - SoloTaxi

## Requisitos Previos

- Node.js v16+
- PostgreSQL v12+
- npm o yarn
- Git

## Instalación Backend

### 1. Clonar repositorio
```bash
git clone https://github.com/taxialcantarilla-beep/solotaxi.git
cd solotaxi/backend
```

### 2. Instalar dependencias
```bash
npm install
```

### 3. Configurar variables de entorno
```bash
cp .env.example .env
```

Edita `.env` con tu configuración:
```
DB_HOST=localhost
DB_PORT=5432
DB_NAME=solotaxi
DB_USER=postgres
DB_PASSWORD=tu_contraseña
PORT=5000
JWT_SECRET=tu_secret_jwt
GOOGLE_MAPS_API_KEY=tu_clave_google_maps
```

### 4. Crear base de datos
```bash
createdb solotaxi
psql -U postgres -d solotaxi -f database/schema.sql
```

### 5. Iniciar servidor
```bash
npm run dev
```

El servidor estará en `http://localhost:5000`

---

## Instalación Frontend

### 1. Navegar a carpeta frontend
```bash
cd ../frontend
```

### 2. Instalar dependencias
```bash
npm install
```

### 3. Configurar variables de entorno
```bash
cp .env.example .env
```

Edita `.env`:
```
REACT_APP_API_URL=http://localhost:5000/api
REACT_APP_SOCKET_URL=http://localhost:5000
REACT_APP_GOOGLE_MAPS_API_KEY=tu_clave_google_maps
```

### 4. Iniciar aplicación
```bash
npm start
```

La app estará en `http://localhost:3000`

---

## Instalación Mobile (React Native)

### 1. Navegar a carpeta mobile
```bash
cd ../mobile
```

### 2. Instalar dependencias
```bash
npm install
```

### 3. Configurar Expo
```bash
npm install -g expo-cli
```

### 4. Iniciar en desarrollo
```bash
npm start
```

Scanea el código QR con tu teléfono

---

## Estructura de Carpetas

```
solotaxi/
├── backend/
│   ├── database/
│   ├── routes/
│   ├── controllers/
│   ├── middleware/
│   ├── server.js
│   └── package.json
├── frontend/
│   ├── src/
│   ├── public/
│   └── package.json
├── mobile/
│   ├── src/
│   └── package.json
└── docs/
```

---

## 🔗 Puertos por Defecto

- Backend API: `5000`
- Socket.io: `5000`
- Frontend React: `3000`
- Mobile: `8081` (con Expo)
- PostgreSQL: `5432`

---

## 🛠️ Comandos Útiles

### Backend
```bash
npm run dev          # Modo desarrollo
npm start            # Producción
npm test             # Tests
npm run migrate      # Migraciones BD
```

### Frontend
```bash
npm start            # Desarrollo
npm run build        # Build producción
npm test             # Tests
```

---

## 📚 Próximas Pasos

1. Crear endpoints de autenticación
2. Implementar Google Maps en frontend
3. Configurar Socket.io para geolocalización
4. Crear sistema de pagos
5. Implementar rating y reviews

---

¡Listo para empezar! 🎉
