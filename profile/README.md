## 👋 STACK TECNOLÓGICO

🤖 Android (Repo: jolgorio-android)
Lenguaje: Kotlin.

UI Framework: Jetpack Compose (Material 3).

Arquitectura: MVVM + Clean Architecture.

Inyección de Dependencias: Hilt.

Asincronía: Coroutines & Flow.

Red: Retrofit o Ktor Client.

Imágenes: Coil.

🍏 iOS (Repo: jolgorio-ios)
Lenguaje: Swift 6+.

UI Framework: SwiftUI.

Arquitectura: TCA (The Composable Architecture).

Concurrencia: Swift Concurrency (Async/Await).

Inyección de Dependencias: Swift-Dependencies.

Red: URLSession.

Imágenes: Kingfisher/AsyncImage.

🔥 Backend & Servicios (Común)
Auth & Base de datos: Firebase (Auth, Firestore, Storage) o Supabase. Crucial definir la estructura de datos JSON antes de empezar para que iOS y Android sean compatibles.

3. Estrategia de Git y CI/CD (DevOps)
Para mantener el orden profesional en Jolgorio, usaremos GitHub Actions para la Integración Continua (CI) y Despliegue Continuo (CD).

Estrategia de Ramas (Git Flow Simplificado)
main: Código de producción (lo que está en la tienda).

develop: Código estable de pre-producción (beta).

feature/nombre-funcionalidad: Ramas de trabajo diario (ej: feature/login-screen)
Pipeline de CI/CD (Automatización)
A. El Guardián (Pull Request Checks)

Cuándo se ejecuta: Cada vez que alguien hace un Pull Request (PR) hacia develop o main.

Qué hace:

Linting: Revisa que el código esté limpio (SwiftLint para iOS, KtLint para Android).

Unit Tests: Ejecuta los tests automáticos. Si fallan, no deja fusionar el código.

Build Test: Comprueba que la app compila sin errores.

B. El Repartidor (CD - Delivery)

Cuándo se ejecuta: Al hacer merge en main o al crear un tag de versión (ej: v1.0.0).

Qué hace:

Incrementa el número de versión.

Genera el binario (.aab para Android, .ipa para iOS).

Firma la app con las claves criptográficas (guardadas en GitHub Secrets).

Android: Sube a Google Play Console (Track: Internal Testing).

iOS: Sube a TestFlight (usando Fastlane).

<!--

**Here are some ideas to get you started:**

🙋‍♀️ A short introduction - what is your organization all about?
🌈 Contribution guidelines - how can the community get involved?
👩‍💻 Useful resources - where can the community find your docs? Is there anything else the community should know?
🍿 Fun facts - what does your team eat for breakfast?
🧙 Remember, you can do mighty things with the power of [Markdown](https://docs.github.com/github/writing-on-github/getting-started-with-writing-and-formatting-on-github/basic-writing-and-formatting-syntax)
-->
