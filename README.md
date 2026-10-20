# 🏫 Sistema Escolar

Sistema web para la organización y administración visual de información escolar.

![HTML5](https://img.shields.io/badge/HTML5-E34F26?style=flat&logo=html5&logoColor=white)
![CSS3](https://img.shields.io/badge/CSS3-1572B6?style=flat&logo=css3&logoColor=white)
![JavaScript](https://img.shields.io/badge/JavaScript-F7DF1E?style=flat&logo=javascript&logoColor=black)
![POO](https://img.shields.io/badge/POO-Clases-blueviolet)
![Status](https://img.shields.io/badge/status-en%20desarrollo-yellow)

---

## 📌 Descripción

El **Sistema Escolar** es un proyecto desarrollado en **HTML5**, **CSS3** y **JavaScript** que presenta una interfaz visual e interactiva para gestionar la información de los alumnos de una institución educativa.

En esta etapa, el código se ha refactorizado para usar **Programación Orientada a Objetos (POO)** real en JavaScript, replicando las clases que se crearon en C++ en actividades anteriores.

---

## ✨ Características

- 🏠 **Encabezado:** logotipo y nombre del sistema.
- 🧭 **Menú de navegación:** accesos a las diferentes secciones.
- 📝 **Registro de alumnos:** instancias reales de la clase `Alumno`.
- 📋 **Tabla dinámica:** llena con métodos y getters de las clases.
- ✏️ **Editar filas:** actualiza datos de un alumno.
- 🗑️ **Eliminar filas:** borra un alumno con confirmación.
- 📊 **Resumen en vivo:** total, promedio general y último registrado.
- 🎨 **Diseño con CSS:** colores, layout responsive y fondo animado.
- ⚡ **Interactividad:** delegación de eventos y manipulación del DOM.
- 🏗️ **POO en JavaScript:** Clases, herencia, polimorfismo, getters, setters y campos privados.

---

## 🏗️ Clases Implementadas

El proyecto ahora usa un modelo orientado a objetos:

| Clase | Atributos | Métodos destacados |
|-------|-----------|--------------------|
| **Persona** (Base) | `#id`, `nombre`, `edad` | `rol()`, `mostrarInfo()`, getter `id` |
| **Alumno** | `matricula`, `correo`, `calificaciones` | `agregarCalificacion()`, getter `promedio` |
| **Maestro** | `empleadoId`, `materia` | `mostrarInfo()` |
| **Administrador** | `departamento` | `mostrarInfo()` |

- **Polimorfismo:** El método `mostrarInfo()` se comporta diferente según la clase.
- **Herencia:** `Alumno`, `Maestro` y `Administrador` heredan de `Persona` usando `extends` y `super()`.
- **Encapsulamiento:** Uso de campos privados con `#` para el ID.

---

## 🛠️ Tecnologías

| Tecnología | Uso |
|------------|-----|
| HTML5 | Estructura de la página web |
| CSS3 | Estilos, layout, variables y responsive |
| JavaScript (ES6+) | Lógica, clases, objetos y manipulación del DOM |
| CSS Grid & Flexbox | Distribución del layout principal |
| Delegación de eventos | Manejo eficiente de botones dinámicos |

---

## 📁 Estructura del proyecto

```
Sistema-Escolar/
├── public/
│   ├── index.html
│   ├── styless.css
│   ├── app.js
│   └── img/
│       ├── mi.png
│       └── fondo.gif
├── main.cpp
└── README.md
```

---

## 🚀 Instalación y ejecución

1. Descarga el proyecto o clona el repositorio.
2. Abre la carpeta `Sistema-Escolar`.
3. Comprueba que las imágenes estén en `public/img/`.
4. Abre `public/index.html` en tu navegador.

---

## 🧠 Comparación: C++ vs JavaScript

| Concepto | C++ | JavaScript |
|----------|-----|------------|
| **Declaración** | `class Alumno { ... };` | `class Alumno { ... }` |
| **Constructor** | Mismo nombre de la clase | `constructor(...)` |
| **Herencia** | `class A : public B` | `class A extends B` |
| **Llamar a base** | Lista de inicialización | `super(...)` |
| **Crear objeto** | `Alumno a("Ana", 20);` | `const a = new Alumno(...)` |
| **Destructor** | `~Alumno()` (determinista) | No hay (Garbage Collector) |
| **Polimorfismo** | `virtual` + punteros | Automático (sobrescritura) |
| **Encapsulamiento** | `private` / `protected` | `#campoPrivado` (ES2022) |

---

## 🧪 Cómo probarlo

1. Abre `public/index.html` en el navegador.
2. Registra un alumno con sus calificaciones.
3. Observa cómo la columna "Promedio" se calcula automáticamente usando el getter de la clase.
4. Abre la consola del navegador (F12) y ejecuta:

```javascript
const ana = new Alumno('Ana', 20, 'A001', 'ana@escuela.com');
const luis = new Maestro('Luis', 40, 'M001', 'Cálculo');
const admin = new Administrador('Sofía', 35, 'Control Escolar');

console.log(ana.mostrarInfo());
console.log(luis.mostrarInfo());
console.log(admin.mostrarInfo());

ana.agregarCalificacion(9);
ana.agregarCalificacion(8);
ana.agregarCalificacion(10);
console.log('Promedio:', ana.promedio.toFixed(2));
```

**Salida esperada en consola:**
```text
Alumno: Ana (20 años) — Matrícula: A001
Maestro: Luis (40 años) — Materia: Cálculo
Administrador: Sofía (35 años)
Promedio: 9.00
```

---

## 📌 Estado del proyecto

| Actividad | Estado |
|-----------|--------|
| Actividad 16 — Estructura HTML | ✅ Completada |
| Actividad 17 — Estilos CSS | ✅ Completada |
| Actividad 18 — JavaScript básico | ✅ Completada |
| Actividad 19 — DOM + Tabla dinámica | ✅ Completada |
| Actividad 20 — Clases en JavaScript | ✅ Completada |
| Actividad 21 — Conexión con backend | ⏳ Pendiente |

En esta etapa los datos **se pierden al recargar** porque aún no hay backend en C++ ni `localStorage`.

---

## 🎯 Próximas mejoras

- [ ] Guardar datos en `localStorage`.
- [ ] Conectar el formulario con el backend en C++ usando `fetch()`.
- [ ] Validar correos con expresiones regulares.
- [ ] Agregar buscador en la tabla.
- [ ] Modo oscuro.

---

## 📄 Licencia

MIT License
