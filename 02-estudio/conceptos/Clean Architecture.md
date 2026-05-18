# Clean Architecture

#estudio #conceptos #arquitectura

## ¿Qué es?
Es un patrón de diseño que separa el código en **capas independientes**, donde las reglas de negocio no dependen de frameworks ni bases de datos.

## Las 3 capas principales

### 🟢 Domain (Centro)
- Entidades y reglas de negocio puras
- **No depende de nada externo**
- Ejemplo: `User`, `Transaction`, `Account`

### 🟡 Application (Intermedia)
- Casos de uso (Use Cases)
- Orquesta la lógica entre Domain e Infrastructure
- Ejemplo: `CreateUserUseCase`, `LoginUseCase`

### 🔴 Infrastructure (Externa)
- Frameworks, bases de datos, APIs externas
- Implementa las interfaces definidas en Domain
- Ejemplo: `PostgresUserRepository`, `JwtTokenGenerator`

## Regla de oro
> Las dependencias siempre apuntan **hacia adentro**. Infrastructure → Application → Domain. Nunca al revés.

## Lo aplico en
- [[NotCloud - Aprende e Integra]] → TypeScript con NestJS
- [[DinnOS - Cerebro Integrado a Obsidian]] → Java con Spring Boot (Dinno-Auth)
