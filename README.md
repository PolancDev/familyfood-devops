# DevOps - Infraestructura y Despliegue

## Estructura

```
devops/
├── docker/           # Dockerfiles para cada servicio
├── pipelines/        # Pipelines CI/CD
├── k8s/              # Manifests de Kubernetes
├── scripts/          # Scripts de automatización
└── openapi.yml      # Especificación OpenAPI
```

## Componentes

### docker/
- `Dockerfile.backend` - Imagen del backend Spring Boot
- `Dockerfile.frontend` - Imagen del frontend Angular
- `docker-compose.yml` - Orquestación local/desarrollo
- `docker-compose.prod.yml` - Producción con múltiples réplicas

### pipelines/
- `.github/workflows/` - GitHub Actions
  - `ci.yml` - Integración continua
  - `deploy-staging.yml` - Despliegue a staging
  - `deploy-production.yml` - Despliegue a producción

### k8s/
- Manifests Kubernetes para despliegue en cluster

### scripts/
- Scripts Bash/PowerShell para automatización
- `setup.sh` - Configuración inicial
- `deploy.sh` - Despliegue automatizado

## Agente Asignado

**DEVOPS** → Trabaja en este directorio

## Comandos Útiles

```bash
# Construir imágenes
docker-compose build

# Ejecutar localmente
docker-compose up

# Ver logs
docker-compose logs -f

# Escalar servicios
docker-compose up -d --scale backend=3
```
