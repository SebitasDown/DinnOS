# 📄 Cheatsheet - Git

#recurso #git #cheatsheet

## Configuración inicial
```bash
git config --global user.name "Tu Nombre"
git config --global user.email "tu@email.com"
```

## Flujo básico
```bash
git add .                    # Agregar cambios al staging
git commit -m "mensaje"      # Crear commit
git push origin main         # Subir al remoto
git pull origin main         # Traer cambios del remoto
```

## Ramas
```bash
git branch nueva-rama        # Crear rama
git checkout nueva-rama      # Cambiar a rama
git checkout -b feature/x    # Crear y cambiar en un paso
git merge feature/x          # Fusionar rama actual con feature/x
```

## Deshacer cosas
| Situación | Comando |
|---|---|
| Deshacer último commit (mantener cambios) | `git reset --soft HEAD~1` |
| Deshacer cambios en un archivo | `git checkout -- archivo.txt` |
| Ver historial | `git log --oneline -10` |
| Diferencias | `git diff` |

## Convenciones de commits
- `feat:` nueva funcionalidad
- `fix:` corrección de bug
- `docs:` documentación
- `refactor:` reestructurar código sin cambiar funcionalidad
- `chore:` tareas de mantenimiento
