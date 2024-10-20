# Convenciones de Commits

Este repositorio sigue la convención de mensajes de commit basada en **Conventional Commits**, una convención que proporciona estructura y claridad a los mensajes de commit. El formato tiene la siguiente estructura:

```
tipo(scope): descripción
```

- **tipo**: Define la naturaleza del commit (por ejemplo, agregar una funcionalidad, corregir un error).
- **scope**: Indica el área específica del código afectada (por ejemplo, `client`, `backend`).
- **descripción**: Un resumen claro y conciso de lo que se ha modificado.

## Ejemplo

```
feat(backend): adicion de nueva ruta para obtener usuarios
fix(client): corregir error de visualización en el formulario
refactor(backend): reorganización de servicios de autenticación
```

## Tipos de Commits

A continuación, se detallan todos los tipos de commits que pueden realizarse en este proyecto:

### 1. **feat** (nueva funcionalidad)
   Se utiliza para agregar una nueva funcionalidad al código. Este tipo generalmente incrementa la versión *minor* (versión `X.Y.0` -> `X.Y+1.0`).

   Ejemplo:
   ```
   feat(backend): adicion de endpoint para actualizar perfil
   ```

### 2. **fix** (corrección de errores)
   Se utiliza para corregir un error existente en el código. Este tipo incrementa la versión *patch* (versión `X.Y.Z` -> `X.Y.Z+1`).

   Ejemplo:
   ```
   fix(client): corregir el botón de envío que no se deshabilita
   ```

### 3. **refactor** (refactorización)
   Cambios que no añaden nuevas funcionalidades ni corrigen errores, pero mejoran la estructura o legibilidad del código sin modificar su comportamiento externo.

   Ejemplo:
   ```
   refactor(backend): reorganizar funciones de manejo de errores
   ```

### 4. **docs** (documentación)
   Para cambios en la documentación del proyecto, como en archivos `README`, comentarios en el código, o guías de instalación.

   Ejemplo:
   ```
   docs: actualizar documentación de instalación
   ```

### 5. **test** (pruebas)
   Se utiliza para cambios en las pruebas unitarias, de integración u otros tipos de test.

   Ejemplo:
   ```
   test(backend): agregar pruebas para el servicio de autenticación
   ```

### 6. **chore** (tareas varias)
   Cambios en la configuración del proyecto o mantenimiento que no afectan directamente el código de producción. Esto incluye actualizaciones de dependencias, configuraciones del proyecto, o scripts.

   Ejemplo:
   ```
   chore: actualizar versión de ESLint y Prettier
   ```

### 7. **build** (sistema de build)
   Cambios que afectan el sistema de construcción del proyecto o las dependencias externas, como `webpack`, `npm`, `pip`, etc.

   Ejemplo:
   ```
   build: actualizar configuración de webpack para producción
   ```

### 8. **ci** (integración continua)
   Cambios en los archivos y configuraciones de integración continua, como en `.github/workflows`, `Jenkinsfile`, etc.

   Ejemplo:
   ```
   ci: configurar pipeline de CI para pruebas unitarias
   ```

### 9. **style** (estilo de código)
   Cambios que no afectan el significado del código (espacios, formato, punto y coma, etc.). No debe incluir cambios funcionales.

   Ejemplo:
   ```
   style: aplicar formato automático al código
   ```

### 10. **perf** (rendimiento)
   Cambios que mejoran el rendimiento del código sin alterar su comportamiento funcional.

   Ejemplo:
   ```
   perf(backend): optimizar consulta de base de datos para obtener usuarios
   ```

### 11. **revert** (revertir cambios)
   Se utiliza para revertir un commit anterior.

   Ejemplo:
   ```
   revert: revertir commit abc123 por problemas de compatibilidad
   ```

### 12. **ci** (integración continua)
   Se refiere a cambios en los archivos y scripts relacionados con la configuración de CI/CD (Integración continua/Entrega continua), como los flujos de trabajo de GitHub Actions o Jenkins.

   Ejemplo:
   ```
   ci: ajustar configuración de pipeline para pruebas automáticas
   ```

### 13. **build** (construcción del proyecto)
   Se usa para los cambios que afectan el sistema de construcción (build) o las dependencias externas.

   Ejemplo:
   ```
   build: actualizar dependencias del proyecto
   ```

### 14. **release** (publicación de versiones)
   Este tipo se usa cuando se crea una nueva versión del proyecto.

   Ejemplo:
   ```
   release: publicar versión 1.2.0
   ```

### 15. **hotfix** (corrección urgente)
   Se utiliza para cambios críticos de corrección de errores que se realizan de manera urgente en producción.

   Ejemplo:
   ```
   hotfix: corregir error crítico de autenticación en producción
   ```

### 16. **security** (mejora de seguridad)
   Se usa para cambios relacionados con la mejora de la seguridad del sistema.

   Ejemplo:
   ```
   security(backend): actualizar política de contraseñas para mayor seguridad
   ```

## Uso de Scopes (Ámbitos)

El **scope** indica qué parte del proyecto se ve afectada por el commit. Algunos ejemplos comunes de scopes son:

- **client**: Cambios en el frontend o la interfaz de usuario.
- **backend**: Cambios en la lógica del servidor o en la API.
- **auth**: Cambios relacionados con autenticación y autorización.
- **database**: Cambios en el esquema o consultas de la base de datos.
- **ci**: Cambios en las configuraciones de CI/CD.

## Beneficios de esta Convención

1. **Claridad**: Los mensajes de commit estructurados hacen que sea fácil entender qué cambios se hicieron, por qué y en qué parte del código.
2. **Mantenimiento**: Facilita el mantenimiento y la navegación por el historial de git, permitiendo encontrar commits relevantes más rápidamente.
3. **Versionado Semántico**: Ayuda a adherirse al versionado semántico, asegurando que los incrementos de versión reflejen con precisión los cambios introducidos.
4. **Colaboración**: Fomenta una mejor colaboración, especialmente en equipos grandes donde diferentes miembros trabajan en diferentes partes del código.
