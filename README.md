# NutriVida — Frontend (React + Vite)

Proyecto de la Clínica Nutricional NutriVida. Entrega EP3 de Desarrollo Full Stack 2.

## Equipo
Matías Lazo Núñez · Esteban Alonso Toloza Araneda · Abraham Becerra Muñoz.

## Tecnologías y funcionamiento
React 19, Vite, React Router, React Bootstrap y Bootstrap. `src/App.jsx` define rutas públicas y protegidas; `src/context/AuthContext.jsx` gestiona token y usuario en `localStorage` y consulta `/api/v1/auth/perfil` tras recargar. `src/services/api.js` centraliza peticiones HTTP.

## Backend asociado
**Repositorio público del backend: PENDIENTE DE CREAR / PEGAR URL REAL.** No se inventó un enlace.
Repositorio conjunto de origen: https://github.com/matias-nu/NutriVida.P2

Swagger del backend, según IP elástica informada por el equipo: http://54.243.53.206:3001/api-docs/

## Instalación local
1. Tener Node.js y npm instalados.
2. Ejecutar `npm ci` en la carpeta `frontend`.
3. Tener el backend en ejecución en `127.0.0.1:3001`.
4. Ejecutar `npm run dev` y abrir la dirección que indique Vite.

El proxy de `vite.config.js` dirige `/api` hacia `http://127.0.0.1:3001`. En un despliegue público, el proxy debe estar disponible o configurarse un servidor equivalente.

## Scripts
- `npm run dev`: servidor Vite.
- `npm run build`: compilar.
- `npm test`: tests de componentes.
- `npm run test:coverage`: cobertura.

## Pantallas y permisos
Públicas: inicio, servicios, detalle, agenda, contacto, registro y login. Paciente: `/mis-citas`. Administrador y Nutricionista: `/panel` y `/panel/citas`. Solo Administrador: `/panel/servicios`.

No se identificaron pantallas React de administración de usuarios ni de planes; esos módulos sí tienen endpoints en backend.

## Evidencia y seguridad
README preparado a partir de `NutriVida.P2-main.zip` (22/11/2026). No se ejecutaron pruebas nuevas en esta preparación. No incluir credenciales ni tokens en GitHub.
