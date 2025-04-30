# Vue Composition Project

![Vue.js](https://img.shields.io/badge/Vue.js-v3.4.19-42b883.svg)
![TypeScript](https://img.shields.io/badge/TypeScript-v5.3.3-3178c6.svg)
![Vite](https://img.shields.io/badge/Vite-v5.1.4-646cff.svg)
![License](https://img.shields.io/badge/License-MIT-blue.svg)

Una aplicación de demostración que muestra el uso de Vue 3 con Composition API, TypeScript y las mejores prácticas de desarrollo modernas.

## 📋 Descripción

Este proyecto es una aplicación de demostración desarrollada con Vue.js 3 y la Composition API, que incluye:

- Implementación completa del Composition API con TypeScript
- Formulario de usuario con validación básica y efectos visuales
- Sistema de gestión de estado con Pinia
- Estructura de proyecto optimizada siguiendo las mejores prácticas
- Flujo de trabajo de Git automatizado con Commitizen y Husky
- Estilo consistente usando la metodología BEM y CSS variables

## 🚀 Características principales

- **Formulario de usuario**: Permite añadir nombre y apellido con una interfaz atractiva
- **Fondo visual**: Paisaje noruego con degradado de 3 colores para una experiencia visual agradable
- **Interfaz responsiva**: Diseñada para funcionar en diferentes tamaños de pantalla
- **Estilo moderno**: Utilizando efectos visuales como backdrop-filter, sombras y transiciones

## 🛠️ Tecnologías utilizadas

- **Vue.js 3**: Framework progresivo para construir interfaces de usuario
- **Composition API**: API moderna para organización lógica del código en Vue
- **TypeScript**: Soporte de tipado estático para mejorar la robustez del código
- **Vite**: Herramienta de construcción ultrarrápida para desarrollo moderno
- **Pinia**: Biblioteca de gestión de estado para Vue 3
- **Vue Router**: Enrutador oficial para Vue.js
- **ESLint**: Herramienta de linting para mantener la coherencia del código
- **Vitest**: Marco de pruebas rápido para aplicaciones Vite
- **Commitizen**: Herramienta para crear mensajes de commit estandarizados

## 📦 Estructura del proyecto

```
/
├── src/                     # Código fuente
│   ├── assets/              # Recursos estáticos (imágenes, fuentes, etc.)
│   ├── components/          # Componentes Vue reutilizables
│   │   ├── HelloWorld.vue   # Componente de ejemplo
│   │   └── user-form.vue    # Formulario de usuario
│   ├── App.vue              # Componente raíz
│   └── main.ts              # Punto de entrada de la aplicación
├── index.html               # Plantilla HTML principal
├── package.json             # Configuración del proyecto y dependencias
├── vite.config.ts           # Configuración de Vite
├── git-workflow.md          # Documentación del flujo de trabajo Git
└── README.md                # Esta documentación
```

## 🔧 Instalación

1. Clonar el repositorio:

```bash
git clone https://github.com/tu-usuario/vue-composition-project.git
cd vue-composition-project
```

2. Instalar las dependencias:

```bash
npm install
```

3. Iniciar el servidor de desarrollo:

```bash
npm run dev
```

## 🖥️ Comandos disponibles

- `npm run dev`: Inicia el servidor de desarrollo
- `npm run build`: Compila y minifica para producción
- `npm run test`: Ejecuta las pruebas unitarias con Vitest
- `npm run lint`: Ejecuta ESLint para verificar el código
- `npm run lint:fix`: Corrige automáticamente los problemas de linting
- `npm run commit`: Inicia la interfaz de Commitizen para crear commits estandarizados

## 📝 Convenciones de código

Este proyecto sigue estrictas convenciones de código que se detallan en el archivo `.github/copilot-instructions.md`:

- Uso exclusivo de Composition API con `<script lang="ts" setup>`
- Gestión de estado reactivo con `ref` y `reactive`
- Estructura de componentes consistente (script, template, style)
- Estilos con CSS scoped siguiendo la metodología BEM
- Variables CSS para colores y espaciado consistente
- Tipos TypeScript para seguridad y autocompletado

## 🔄 Flujo de trabajo Git

El proyecto utiliza un flujo de trabajo Git automatizado con:

- **Commitizen**: Para crear mensajes de commit estandarizados
- **Husky**: Para ejecutar hooks de Git (pre-commit, pre-push)
- **Convención de commits**: Formato estructurado (feat, fix, docs, etc.)

Para más detalles, consulta el archivo `git-workflow.md`.

## 🤝 Contribuciones

Las contribuciones son bienvenidas. Por favor, asegúrate de seguir las convenciones de código y de utilizar el flujo de trabajo Git apropiado:

1. Crea una rama para tu feature: `git checkout -b feature/nombre-de-caracteristica`
2. Haz tus cambios y utiliza `npm run commit` para crear mensajes de commit estandarizados
3. Envía un pull request a la rama principal

## 📄 Licencia

Este proyecto está bajo la Licencia MIT - ver el archivo `LICENSE` para más detalles.

---

Desarrollado con ❤️ utilizando Vue.js y Composition API
