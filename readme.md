# nexo play 

## Portada

Nombre: Fabricio  
Módulo: CSS Responsive Design  
Fecha: 27/06/2026  


Se identificaron los siguientes problemas:

## Macro Layout
La página original tenía el header, sidebar y contenido apilados sin orden.

Solución:
Se utilizó CSS Grid para separar sidebar y contenido principal.

## Box Model
Los elementos chocaban entre sí por falta de margin y padding.

Solución:
Se agregaron espacios internos y externos usando padding, margin y box-sizing.

## Micro Layout
Las tarjetas de video estaban desalineadas.

Solución:
Se utilizó Flexbox dentro de cada card para alinear imagen, título y botón.

---

# Implementación de CSS Grid

Se usó:

```css
.layout {
    display: grid;
    grid-template-columns: 250px 1fr;
}
```

Esto separa el menú lateral del contenido principal.

También se utilizó Grid en:

```css
.video-grid {
    display: grid;
}
```

Para organizar videos en filas y columnas adaptables.

---

# Implementación de Flexbox

Se usó Flexbox en:

```css
.card {
    display: flex;
    flex-direction: column;
}
```

Esto alinea verticalmente:

- Imagen
- Título
- Botón

También se utilizó en la barra de navegación.

---

# Reto IA

## CSS Original

```css
.card button {
    background: purple;
    color: white;
    padding: 10px;
}
```

## Prompt enviado a IA

Rol:
Actúa como un experto en CSS y accesibilidad web.

Contexto:
Estoy desarrollando una plataforma responsive de streaming llamada NexoPlay.

Tarea:
Optimiza este CSS usando variables CSS, mejora el contraste visual con estándar AAA y mantén el diseño responsive.

Formato:
Devuelve código CSS comentado y explica mejoras.

## CSS Devuelto por IA

```css
:root {
    --button-bg: #5a31ff;
    --button-text: #ffffff;
}

.card button {
    background: var(--button-bg);
    color: var(--button-text);
    padding: 12px;
    border-radius: 8px;
}
```

---

# Análisis Crítico

## ¿El código generado por la IA respetó el diseño responsivo?

Sí. El código respeto por completo el diseño responsivo y dio medidas fijas y mantuvo tamaños adaptables.

## ¿Qué ventajas técnicas aportó?

- Uso de variables CSS reutilizables
- Mejor contraste visual (AAA)
- Mayor mantenibilidad
- Código más limpio y escalable