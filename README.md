# Proyecto DevOps: reserva de horas médicas

## Descripción
Sitio web estático de demostración para simular la reserva de horas médicas. Se sirve con Nginx usando Docker y Docker Compose. No utiliza API ni base de datos y el formulario no envía ni almacena información real.

## Requisitos
- Git instalado.
- Cuenta de GitHub.
- Docker Desktop iniciado.
- Navegador web.

## Estructura
```text
proyecto_reserva_devops/
├── .github/workflows/devops-automation.yml
├── src/
│   ├── index.html
│   └── styles.css
├── .dockerignore
├── .env.example
├── .gitignore
├── Dockerfile
├── docker-compose.yml
└── README.md
```

## Ejecutar localmente
Desde la carpeta principal del proyecto, ejecutar:

```bash
docker compose up -d --build
docker compose ps
```

Abrir en el navegador: http://localhost:8080

## Revisar logs y recursos
```bash
docker compose logs
docker stats --no-stream
```

## Detener el servicio
```bash
docker compose down
```

## Seguridad
No se deben subir credenciales, tokens, claves ni datos personales. El archivo `.env` está excluido mediante `.gitignore`; se incluye `.env.example` solo como referencia y sin secretos. Para esta simulación no se recopilan datos reales y el formulario es únicamente visual.

## Verificación
El servicio se considera disponible cuando el contenedor aparece activo con `docker compose ps` y la página se visualiza desde `http://localhost:8080`.

## Verificación del servicio

Para comprobar que la aplicación funciona correctamente:

- Ejecutar `docker compose ps` para revisar el estado del contenedor.
- Ejecutar `docker compose logs` para revisar los registros.
- Abrir http://localhost:8080 en el navegador para verificar la página.
- Ejecutar `docker compose down` para detener el servicio.