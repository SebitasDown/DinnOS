# React - Fundamentos

#estudio #frontend #react

## ¿Qué es?
React es una librería de JavaScript para construir interfaces de usuario. Creada por Meta, se basa en **componentes reutilizables**.

## Conceptos Clave

### Componentes
Son bloques de UI independientes. Pueden ser funciones que retornan JSX:
```jsx
function Saludo({ nombre }) {
  return <h1>Hola, {nombre}!</h1>
}
```

### Estado (useState)
Permite que un componente "recuerde" datos entre renders:
```jsx
const [contador, setContador] = useState(0)
```

### Props
Datos que un componente padre le pasa a un hijo. Son **de solo lectura**.

### useEffect
Ejecuta código cuando el componente se monta o cuando cambian ciertas dependencias:
```jsx
useEffect(() => {
  fetchDatos()
}, [userId])
```

## Relación con mis proyectos
- En [[NotCloud - Aprende e Integra]] uso React con Next.js
- En [[DinnOS - Cerebro Integrado a Obsidian]] el frontend usa React Native (Expo)

## Recursos
- [Documentación oficial](https://react.dev)
- [[Bases de datos]] se conectan al frontend mediante APIs REST
