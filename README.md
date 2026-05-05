# FamilyFood DevOps

DevOps y CI/CD para FamilyFood - Docker, Kubernetes, GitHub Actions

## Contenido

| Archivo | Descripción |
|---------|-------------|
| `openapi.yml` | Contrato OpenAPI 3.0 para sincronización Frontend/Backend |
| `README.md` | Este archivo |

## Contrato API (OpenAPI)

El archivo `openapi.yml` define el contrato API entre frontend y backend. Incluye:

- **Auth:** Registro e inicio de sesión con JWT
- **Familias:** CRUD de grupos familiares, solicitudes de unión
- **Usuarios:** Perfil de usuario
- **Recetas:** CRUD completo con ingredientes, etiquetas y niveles de cocina

### Generación de tipos

```bash
# Frontend: generar tipos TypeScript desde el contrato
npx openapi-typescript openapi.yml -o ../familyfood-frontend/src/app/core/models/api.ts

# Backend: generar DTOs Java (si se usa openapi-generator-maven-plugin)
mvn generate-sources
```
