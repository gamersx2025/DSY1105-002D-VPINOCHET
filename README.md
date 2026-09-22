🚀 DSY1105-002-INICIALNOMBREAPELLIDO | DesApp Móviles - Duoc UC

    Si estás leyendo esto, felicidades. Ya hiciste más que el compañero que dijo "lo hago mañana".

Bienvenido a tu repositorio oficial de Desarrollo de Aplicaciones Móviles (DSY1105). Aquí vas a sufrir, aprender Kotlin, pelearte con Android Studio y finalmente decir "¡Compiló, w*n!".

Este README es tu manual de supervivencia.
📚 ¿Qué cresta es este repo?

Este repo es tu bitácora, entrega y portafolio. Aquí vive todo tu código Kotlin de la asignatura.
Formato obligatorio del nombre:

DSY1105-002-VPinochet  ->  SIGLA-SECCIÓN-INICIAL+NOMBRE+APELLIDO
Ejemplo: Si te llamas Victor Pinochet, es VPinochet. NO pongas INICIALNOMBREAPELLIDO literal o te funan en GitHub.

🛠️ Stack que usaremos (las 3 bestias)

    GitHub: Donde guardas tu código y demuestras que no lo hiciste todo la noche anterior.
    Trello: Donde finges que eres ordenado. Kanban: Por hacer, Haciendo, Hecho.
    Android Studio: El IDE que ama consumir 16GB de RAM para un "Hola Mundo".

🔧 PASO 0: Pre-requisitos antes de llorar

    Instala Git: git --version
    Instala Android Studio (versión Koala o superior) con SDK Android 14+
    Crea cuenta en Trello y únete al tablero del equipo
    Tener café o energética. Mucha.

🚀 PASO 1: Clonando tu repo (GitHub)

Abre tu terminal / Git Bash y pega esto:
bash

# 1. Clona tu repo (cambia la URL por la tuya)
git clone https://github.com/TU_USUARIO/DSY1105-002-INICIALNOMBREAPELLIDO.git

# 2. Entra a la carpeta
cd DSY1105-002-INICIALNOMBREAPELLIDO

# 3. Crea tu rama de trabajo - NUNCA trabajes en main directo
git checkout -b desarrollo

# 4. Crea tu estructura base
mkdir -p src/semana1 src/semana2 docs
echo "# Mi repo DSY1105" > README.md

Regla de oro Duoc: Un commit al día mantiene al profe alejado del 1.0
bash

git add .
git commit -m "feat: inicio semana 1 - hola mundo en Kotlin"
git push origin desarrollo

    Después haz un Pull Request de desarrollo -> main. Así se ve pro.

Tu .gitignore salvavidas: Asegúrate de que tu repo tenga un .gitignore para Android. Si no, vas a subir 2GB de archivos basura.

.idea/
.gradle/
build/
*.iml
local.properties

📋 PASO 2: Trello - Para que no te digan "¿y tú qué hiciste?"

Así trabajamos, modo Duoc pro:

    Crea 3 listas: 📝 Por Hacer / 💻 En Progreso / ✅ Hecho
    Cada tarea es una tarjeta. Ej: Crear login en Kotlin
    En cada tarjeta pon: Descripción, checklist, fecha y link al commit de GitHub cuando la termines.

Ejemplo de tarjeta:

    Título: Ejercicio 1 - Variables en Kotlin
    Checklist: [ ] crear archivo [ ] probar val/var [ ] subir a GitHub
    Link: github.com/.../commit/abc123

Pro tip: Si tu Trello está vacío, tu nota también.
🤖 PASO 3: Android Studio - Tu primer proyecto sin explotar el PC

    Abre Android Studio > New Project > Empty Activity
    Configura así:
        Name: DSY1105App
        Package: cl.duoc.dsy1105.tunombre
        Language: Kotlin (¡OJO! No Java)
        Minimum SDK: API 24
    Espera a que sincronice Gradle. Sí, se demora. Ve a buscar pan.
    Corre en el emulador. Si ves "Hello Android!", ganaste.

💜 PASO 4: Kotlin 101 - Para los que vienen de Python y están confundidos

Kotlin no muerde. Solo es medio especial con los nulos.
kotlin

// 1. Variables: val = no cambia (como tu nota si no estudias), var = si cambia
val nombre: String = "Victor"
var edad: Int = 23
edad = 24 // se puede

// 2. Funciones: fun es tu nuevo mejor amigo
fun saludar(nombre: String): String {
    return "Hola $nombre, ¿cachai Kotlin?"
}
println(saludar("Duoc"))

// 3. El famoso IF y WHEN (el switch con esteroides)
val nota = 6.5
if (nota >= 4.0) {
    println("Pasaste, crack")
} else {
    println("A repetir :(")
}

// WHEN es más bacán
val dia = 2
when(dia) {
    1 -> println("Lunes, con sueño")
    2 -> println("Martes, aún con sueño")
    else -> println("Viernes al fin!")
}

// 4. Loops y listas
val ramos = listOf("DSY1105", "PGY4121", "ASY...")
for (ramo in ramos) {
    println("Estudiando $ramo")
}

// 5. El temido NULL SAFETY (por esto Kotlin te ama)
var apellido: String? = null // el ? dice "puede ser nulo, tranqui"
println(apellido?.length) // si es nulo, no explota. Usa ?. siempre.

// 6. Tu primera clase (POO sin tanto drama)
class Alumno(val nombre: String, val carrera: String) {
    fun presentarse() = "Soy $nombre de $carrera y ya no duermo"
}
val yo = Alumno("Victor", "Analista Programador")
println(yo.presentarse())

Tarea express semana 1:
Crea un archivo HolaMundo.kt en src/semana1/ que pida tu nombre y tu carrera y lo imprima.
📦 Estructura final de tu repo (para que el profe no llore)

DSY1105-002-VPinochet/
├── README.md (este archivo hermoso)
├── docs/
│   ├── trello_link.txt
│   └── capturas/
├── src/
│   ├── semana1/ -> HolaMundo.kt, Variables.kt
│   ├── semana2/ -> Funciones, Condicionales
│   └── proyecto/ -> Tu app de Android Studio
└── .gitignore

✅ Checklist de entrega (antes de decir "profe, terminé")

    ¿Tu repo se llama bien? DSY1105-002-TU_NOMBRE
    ¿Tu código está en la rama desarrollo y con PR a main?
    ¿Tu Trello tiene todo en ✅ Hecho con links a commits?
    ¿Tu app compila? (Build > Make Project sin rojo)
    ¿Borraste los println("prueba") y // no tocar?
    ¿Subiste el link del repo a AVA?

🆘 Comandos que te salvarán la vida
bash

git status -> ¿qué la cagué?
git log --oneline -> historial bonito
git pull origin main -> actualizar antes de empezar
# Si Android Studio dice "Gradle sync failed": File > Invalidate Caches / Restart

📚 Recursos para no googlear "como se hace un if en kotlin"

    Kotlin Playground: https://play.kotlinlang.org/
    Android Developers en Español
    Canal de YouTube: MoureDev - Kotlin desde cero

Hecho con 💻, ☕ y pánico por un alumno de Duoc para alumnos de Duoc.

    Si este README te sirvió, deja una ⭐ en tu propio repo. Si no, igual déjala, pa' que se vea bonito.

¿Dudas? Abre un Issue en GitHub, no me hables a las 2 AM por WhatsApp.

// TODO: Aprobar DSY1105 sin volverse loco
