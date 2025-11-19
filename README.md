# Quiz Dart - Aplicación Android

## 📱 Descripción de la Aplicación

**Quiz Dart** es una aplicación móvil Android desarrollada en Kotlin que permite a los usuarios realizar quizzes interactivos sobre tecnología y desarrollo móvil. La aplicación carga preguntas dinámicamente desde Firebase Firestore, permitiendo una experiencia de aprendizaje gamificada.

### Características Principales

-  Interfaz moderna y atractiva con gradientes y animaciones
-  Sistema de preguntas dinámico desde Firebase Firestore
-  10 preguntas aleatorias por sesión de quiz
-  Cálculo automático de puntuación
-  Almacenamiento de resultados en la nube
-  Diseño responsive optimizado para dispositivos móviles

## 👥 Nombre 
     
     Janier palacios

**Equipo Quiz Dart**

##  Cómo Ejecutar la Aplicación

### Requisitos Previos

- Android Studio (Hedgehog o superior)
- JDK 17 o superior
- Dispositivo Android (físico o emulador) con Android 7.0 (API 24) o superior
- Conexión a Internet
- Cuenta de Firebase configurada

### Pasos para Ejecutar

1. **Clonar el Repositorio**
   ```bash
   git clone https://github.com/JASPASA10/APK_QUIZZ.git
   cd APK_QUIZZ
   ```

2. **Abrir en Android Studio**
   - Abre Android Studio
   - Selecciona **File → Open**
   - Navega a la carpeta del proyecto y selecciónala

3. **Sincronizar Gradle**
   - Haz clic en el ícono de **elefante** (Sync Project with Gradle Files)
   - O ve a **File → Sync Project with Gradle Files**
   - Espera a que termine la sincronización

4. **Configurar Firebase**
   - El archivo `app/google-services.json` ya está configurado
   - Verifica que Firestore Database esté creada en Firebase Console
   - Las reglas de Firestore deben permitir lectura/escritura (modo de prueba)

5. **Reconstruir el Proyecto**
   - Ve a **Build → Rebuild Project**
   - Esto generará las clases de ViewBinding automáticamente

6. **Ejecutar la Aplicación**
   - Conecta un dispositivo Android o inicia un emulador
   - Haz clic en el botón **Run**  (o presiona `Shift + F10`)
   - La aplicación se instalará y ejecutará automáticamente

### Primera Ejecución

- Al ejecutar la app por primera vez, se agregarán automáticamente 10 preguntas a Firestore
- Verifica en Firebase Console que la colección `questions` tenga 10 documentos
- Si no aparecen, revisa Logcat en Android Studio para ver errores

##  Generar APK

### APK de Debug (Pruebas)
```bash
.\gradlew.bat assembleDebug
```
El APK estará en: `app/build/outputs/apk/debug/app-debug.apk`

### APK de Release (Producción)
1. En Android Studio: **Build → Generate Signed Bundle / APK**
2. Selecciona **APK** → Next
3. Crea un keystore o usa uno existente
4. Selecciona **release** → Finish
5. El APK estará en: `app/build/outputs/apk/release/app-release.apk`

##  Estructura del Proyecto

```
app/
├── src/main/
│   ├── java/App/Quizz1_/
│   │   ├── MainActivity.kt
│   │   ├── fragments/
│   │   │   ├── WelcomeFragment.kt
│   │   │   ├── QuizFragment.kt
│   │   │   └── ResultFragment.kt
│   │   ├── models/
│   │   │   └── Question.kt
│   │   ├── repository/
│   │   │   └── QuizRepository.kt
│   │   ├── viewmodel/
│   │   │   └── QuizViewModel.kt
│   │   └── utils/
│   │       └── QuestionInitializer.kt
│   ├── res/
│   │   ├── layout/          # Diseños XML
│   │   ├── drawable/        # Recursos gráficos
│   │   └── values/          # Colores, strings, temas
│   └── AndroidManifest.xml
└── google-services.json     # Configuración Firebase
```

##  Tecnologías Utilizadas

- **Kotlin** - Lenguaje de programación
- **Android SDK** - Framework de desarrollo
- **Firebase Firestore** - Base de datos en la nube
- **ViewBinding** - Binding de vistas
- **ViewModel & LiveData** - Arquitectura MVVM
- **Coroutines** - Programación asíncrona
- **Material Design** - Componentes de UI

## 🎥 Video Explicativo

[ble en la carpeta `releases/` o puedes generarlo siguiendo las instrucciones en la sección "Generar APK".

Este proyecto es parte del proyecto final del curso.



