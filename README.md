# gitflow-demo
cat > README.md << 'EOF'
# gitflow-demo

## Estrategia de branching: GitFlow

### Ramas permanentes
| Rama | Propósito |
|------|-----------|
| `main` | Código en producción |
| `develop` | Integración de features |

### Ramas temporales
| Patrón | Sale desde | Merge hacia |
|--------|-----------|-------------|
| `feature/*` | `develop` | `develop` |
| `hotfix/*` | `main` | `main` + `develop` |
| `release/*` | `develop` | `main` + `develop` |

## Convenciones de commits

| Tipo | Uso |
|------|-----|
| `feat` | Nueva funcionalidad |
| `fix` | Corrección de bug |
| `test` | Añadir o modificar tests |
| `docs` | Documentación |
| `refactor` | Refactor sin cambio funcional |
| `chore` | Mantenimiento y configuración |

Formato: `tipo(scope): descripción corta`
Ejemplo: `feat(auth): add JWT refresh token`

## Proceso de Pull Request

1. Crear rama desde la base correcta
2. Commits atómicos y descriptivos
3. Abrir PR con descripción del cambio
4. Mínimo 1 aprobación requerida
5. Pasar todos los checks de CI
6. Merge con Squash hacia `develop`, Merge commit hacia `main`

## Naming de ramas

- `feature/nombre-en-kebab-case`
- `hotfix/descripcion-del-bug`
- `release/v1.0.0`
EOF
