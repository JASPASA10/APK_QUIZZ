# Wiki - Quiz Dart

## 1. Definición del Problema

En la actualidad, existe una necesidad creciente de aplicaciones educativas que permitan a los usuarios aprender de manera interactiva y gamificada. Los métodos tradicionales de aprendizaje pueden resultar aburridos y poco motivadores. Además, la falta de herramientas que permitan evaluar conocimientos de manera inmediata y obtener retroalimentación instantánea limita el proceso de aprendizaje efectivo.

**Problema Principal:** 
No existe una aplicación móvil accesible que permita a los usuarios realizar quizzes interactivos sobre tecnología y desarrollo móvil de manera dinámica, con preguntas actualizadas desde la nube y un sistema de puntuación automático.

## 2. Objetivo General

Desarrollar una aplicación móvil Android que permita a los usuarios realizar quizzes interactivos sobre tecnología y desarrollo móvil, proporcionando una experiencia de aprendizaje gamificada con preguntas dinámicas cargadas desde Firebase Firestore y un sistema de evaluación automática.

## 2.1. Objetivos Específicos

1. Diseñar e implementar una interfaz de usuario moderna y atractiva con tres pantallas principales (Welcome, Quiz, Result)
2. Integrar Firebase Firestore para almacenar y gestionar preguntas de manera dinámica
3. Implementar un sistema de selección aleatoria de 10 preguntas por sesión de quiz
4. Desarrollar un algoritmo de validación de respuestas y cálculo automático de puntuación
5. Crear un sistema de inicialización automática que agregue 10 preguntas predefinidas a Firestore
6. Implementar arquitectura MVVM para mantener la separación de responsabilidades
7. Garantizar una experiencia de usuario fluida con transiciones entre pantallas
8. Almacenar resultados de los quizzes en Firestore para análisis posterior

## 3. Requerimientos Funcionales

### RF1: Pantalla de Bienvenida
La aplicación debe mostrar una pantalla de bienvenida con el nombre de la aplicación, diseño atractivo y un botón para iniciar el quiz.

### RF2: Carga de Preguntas desde Firestore
La aplicación debe cargar preguntas dinámicamente desde Firebase Firestore al iniciar el quiz.

### RF3: Selección Aleatoria de Preguntas
El sistema debe seleccionar aleatoriamente 10 preguntas de un conjunto disponible en Firestore para cada sesión de quiz.

### RF4: Visualización de Preguntas
La aplicación debe mostrar una pregunta a la vez con 4 opciones de respuesta claramente identificadas.

### RF5: Validación de Respuestas
El sistema debe validar automáticamente si la respuesta seleccionada por el usuario es correcta o incorrecta.

### RF6: Navegación entre Preguntas
La aplicación debe permitir avanzar automáticamente a la siguiente pregunta después de seleccionar una respuesta.

### RF7: Cálculo de Puntuación
El sistema debe calcular automáticamente el porcentaje de aciertos al finalizar todas las preguntas.

### RF8: Pantalla de Resultados
La aplicación debe mostrar una pantalla con el resultado final (porcentaje) y opciones para reiniciar el quiz o cerrar la aplicación.

### RF9: Inicialización Automática de Preguntas
El sistema debe agregar automáticamente 10 preguntas predefinidas a Firestore si la colección está vacía.

### RF10: Almacenamiento de Resultados
La aplicación debe guardar los resultados de cada quiz en Firestore para análisis posterior.

## 4. Requerimientos No Funcionales

### RNF1: Rendimiento
La aplicación debe cargar las preguntas desde Firestore en menos de 3 segundos.

### RNF2: Usabilidad
La interfaz debe ser intuitiva y fácil de usar, siguiendo las guías de Material Design.

### RNF3: Compatibilidad
La aplicación debe funcionar en dispositivos Android con versión 7.0 (API 24) o superior.

### RNF4: Escalabilidad
El sistema debe permitir agregar nuevas preguntas sin necesidad de actualizar la aplicación.

### RNF5: Mantenibilidad
El código debe seguir buenas prácticas de programación, usar arquitectura MVVM y estar bien documentado.

## 5. Historias de Usuario

### HU1: Como usuario, quiero ver una pantalla de bienvenida atractiva para que me motive a iniciar el quiz.
**Criterios de Aceptación:**
- La pantalla muestra el nombre de la aplicación
- Hay un botón visible para iniciar el quiz
- El diseño es moderno y atractivo

### HU2: Como usuario, quiero iniciar el quiz con un solo toque para comenzar rápidamente.
**Criterios de Aceptación:**
- Al hacer clic en "let's GO ?", se carga la primera pregunta
- La transición es fluida y rápida

### HU3: Como usuario, quiero ver preguntas sobre tecnología para evaluar mis conocimientos.
**Criterios de Aceptación:**
- Las preguntas son relevantes y actuales
- Cada pregunta tiene 4 opciones de respuesta

### HU4: Como usuario, quiero seleccionar una respuesta tocando el botón correspondiente.
**Criterios de Aceptación:**
- Los botones de respuesta son claramente visibles
- La selección se registra inmediatamente

### HU5: Como usuario, quiero que el sistema valide automáticamente mi respuesta para saber si acerté.
**Criterios de Aceptación:**
- El sistema valida la respuesta sin intervención manual
- La validación es instantánea

### HU6: Como usuario, quiero avanzar automáticamente a la siguiente pregunta después de responder.
**Criterios de Aceptación:**
- Al responder, se muestra la siguiente pregunta automáticamente
- No hay pasos adicionales requeridos

### HU7: Como usuario, quiero responder 10 preguntas en cada sesión para tener una evaluación completa.
**Criterios de Aceptación:**
- El sistema muestra exactamente 10 preguntas
- Las preguntas son diferentes en cada sesión (aleatorias)

### HU8: Como usuario, quiero ver mi puntuación al finalizar el quiz para conocer mi desempeño.
**Criterios de Aceptación:**
- Se muestra un porcentaje de aciertos
- El resultado es claro y visible

### HU9: Como usuario, quiero reiniciar el quiz para intentar mejorar mi puntuación.
**Criterios de Aceptación:**
- Hay un botón "Restart Quiz" visible
- Al hacer clic, se reinicia el quiz con nuevas preguntas

### HU10: Como usuario, quiero cerrar la aplicación cuando termine de usar el quiz.
**Criterios de Aceptación:**
- Hay un botón "Close App" disponible
- Al hacer clic, la aplicación se cierra

### HU11: Como administrador, quiero que las preguntas se carguen desde la nube para poder actualizarlas sin modificar la app.
**Criterios de Aceptación:**
- Las preguntas se cargan desde Firebase Firestore
- Se pueden agregar nuevas preguntas desde Firebase Console

### HU12: Como desarrollador, quiero que el sistema inicialice automáticamente las preguntas para facilitar la configuración inicial.
**Criterios de Aceptación:**
- Al ejecutar la app por primera vez, se agregan 10 preguntas automáticamente
- No se requieren pasos manuales adicionales

### HU13: Como usuario, quiero que la aplicación funcione sin conexión a Internet después de cargar las preguntas.
**Criterios de Aceptación:**
- Una vez cargadas las preguntas, el quiz funciona sin conexión
- Los resultados se guardan cuando hay conexión

### HU14: Como usuario, quiero ver mensajes claros si hay errores al cargar las preguntas.
**Criterios de Aceptación:**
- Se muestran mensajes de error comprensibles
- Se indica qué hacer para resolver el problema

### HU15: Como usuario, quiero una experiencia visual atractiva con gradientes y animaciones para disfrutar más el quiz.
**Criterios de Aceptación:**
- La interfaz usa gradientes modernos
- Las transiciones son suaves y fluidas

## 6. Pantallas por Integrante

### Pantalla 1: Welcome Screen (Pantalla de Bienvenida)
- Diseño con gradientes púrpura/rosa
- Botón "let's GO ?" para iniciar
- Patrón de ondas decorativo
- Letras D-A-R-T destacadas

### Pantalla 2: Quiz Screen (Pantalla de Preguntas)
- Header con menú y texto "choose the correct answer"
- Tarjeta de pregunta con gradiente
- 4 botones de respuesta con gradientes
- Navegación automática entre preguntas

### Pantalla 3: Result Screen (Pantalla de Resultados)
- Título "Your Result"
- Puntuación grande en porcentaje
- Botón "Restart Quiz"
- Botón "Close App"

## 7. Mockups y Transiciones

### Mockups de las Pantallas

Las tres pantallas principales fueron diseñadas siguiendo el diseño original de Figma, manteniendo:
- Colores: Gradientes púrpura (#6B66FF), rosa (#FF66E0), y variaciones
- Tipografía: Texto en negrita e itálico donde corresponde
- Dimensiones: 320x568dp (similar a Google Pixel 2 XL)
- Bordes redondeados: 40dp para tarjetas principales

### Transiciones

1. **Welcome → Quiz:** Al hacer clic en "let's GO ?", se carga la primera pregunta
2. **Quiz → Quiz:** Al responder, avanza automáticamente a la siguiente pregunta
3. **Quiz → Result:** Al terminar las 10 preguntas, muestra el resultado
4. **Result → Welcome:** Al hacer clic en "Restart Quiz", vuelve a la pantalla inicial
5. **Result → Close:** Al hacer clic en "Close App", cierra la aplicación

### Herramientas de Diseño

Los mockups fueron creados basándose en el diseño original de Figma proporcionado, manteniendo la fidelidad visual exacta en la implementación Android.

## 8. Información Técnica

### Arquitectura
- **Patrón:** MVVM (Model-View-ViewModel)
- **ViewBinding:** Para binding de vistas
- **Coroutines:** Para operaciones asíncronas
- **StateFlow:** Para gestión de estado reactivo

### Base de Datos
- **Firebase Firestore:** Almacenamiento de preguntas y resultados
- **Colección:** `questions` (preguntas del quiz)
- **Colección:** `quizResults` (resultados de los usuarios)

### Dependencias Principales
- AndroidX Core, AppCompat, Material
- Firebase BOM, Firestore, Auth, Analytics
- Kotlin Coroutines
- Lifecycle Components

## 9. Instrucciones para el Video

Para el video de explicación del proyecto, asegúrate de cubrir:

1. **Explicación del Código:**
   - Arquitectura MVVM
   - Estructura de carpetas
   - Flujo de datos
   - Integración con Firebase

2. **Decisiones de Diseño:**
   - Por qué se mantuvo el diseño original
   - Elección de colores y gradientes
   - Responsive design

3. **Funcionalidades:**
   - Carga de preguntas desde Firestore
   - Sistema de validación
   - Cálculo de puntuación

4. **Ejecución de la App:**
   - Demostrar las 3 pantallas
   - Mostrar el flujo completo del quiz
   - Mostrar resultados

## 10. Enlaces y Recursos

- **Repositorio GitHub:** https://github.com/JASPASA10/APK_QUIZZ.git
- **Firebase Console:** https://console.firebase.google.com/project/baseappquizz
- **Diseño Original:** Basado en Figma (proporcionado en el proyecto original)

