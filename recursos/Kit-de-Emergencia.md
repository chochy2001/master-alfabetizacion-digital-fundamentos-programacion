# Kit de Emergencia - Guia de Primeros Auxilios

> Consulta este documento cuando tengas problemas. No lo leas completo, busca tu problema especifico.

---

## Indice Rapido

1. [Mi codigo no funciona](#1-mi-codigo-no-funciona)
2. [No entiendo el mensaje de error](#2-no-entiendo-el-mensaje-de-error)
3. [Estoy completamente atascado](#3-estoy-completamente-atascado)
4. [Se me olvido todo lo que aprendi](#4-se-me-olvido-todo-lo-que-aprendi)
5. [Problemas con el IDE](#5-problemas-con-el-ide)
6. [Problemas con la Terminal](#6-problemas-con-la-terminal)
7. [Problemas con Git](#7-problemas-con-git)
8. [Donde buscar ayuda](#8-donde-buscar-ayuda)
9. [Como hacer buenas preguntas](#9-como-hacer-buenas-preguntas)

---

## 1. Mi codigo no funciona

### Checklist de Debugging (sigue en orden)

- [ ] **Paso 1: Respira.** Frustrado no piensas bien.

- [ ] **Paso 2: Lee el error completo.** No solo la primera linea. Todo.

- [ ] **Paso 3: Revisa la linea que indica el error.** El numero de linea esta en el mensaje.

- [ ] **Paso 4: Busca errores tipicos:**
  - Falta punto y coma o coma
  - Parentesis o llaves sin cerrar
  - Variable mal escrita (mayusculas/minusculas importan)
  - Falta declarar una variable
  - Usar `=` en lugar de `==` para comparar

- [ ] **Paso 5: Comenta codigo.** Comenta partes hasta encontrar la que falla.

- [ ] **Paso 6: Agrega prints.** Imprime valores de variables para ver que contienen.

- [ ] **Paso 7: Compara con codigo que funciona.** Busca ejemplos similares.

- [ ] **Paso 8: Toma un descanso.** 5-10 minutos. El cerebro sigue trabajando.

- [ ] **Paso 9: Explica el problema en voz alta.** A alguien o a un objeto (Rubber Duck Debugging).

- [ ] **Paso 10: Pide ayuda.** Si llevas 30+ minutos, es hora de preguntar.

---

## 2. No entiendo el mensaje de error

### Anatomia de un mensaje de error

```
Exception in thread "main" java.lang.NullPointerException
    at com.example.Main.calcular(Main.kt:25)
    at com.example.Main.main(Main.kt:10)
```

**Partes importantes:**

| Parte | Que significa |
|-------|---------------|
| `NullPointerException` | Tipo de error (buscalo en Google) |
| `Main.kt:25` | Archivo y linea donde ocurrio |
| `calcular` | Funcion donde esta el problema |

### Errores comunes y que significan

| Error | Significado | Solucion |
|-------|-------------|----------|
| `Unresolved reference: x` | `x` no existe o esta mal escrito | Revisa el nombre de la variable |
| `Type mismatch` | Tipo de dato incorrecto | Convierte el tipo o usa el correcto |
| `NullPointerException` | Intentas usar algo que es null | Verifica que el valor no sea null |
| `IndexOutOfBoundsException` | Accedes a una posicion que no existe | Revisa los indices del array |
| `Syntax error` | Algo esta mal escrito | Revisa puntuacion y estructura |
| `Cannot find symbol` | No encuentra una clase o metodo | Importa la clase o revisa el nombre |

### Como buscar errores en Google

**Buena busqueda:**
```
kotlin "Type mismatch" String Int
```

**Mala busqueda:**
```
mi codigo no funciona ayuda
```

**Tips:**
- Copia el tipo de error exacto
- Agrega el lenguaje (kotlin, java, etc.)
- Usa comillas para frases exactas
- Ignora las partes especificas de tu codigo

---

## 3. Estoy completamente atascado

### La regla de los 30 minutos

Si llevas **30 minutos** sin avanzar, haz lo siguiente:

1. **Escribe exactamente que intentas hacer** (1 parrafo)
2. **Escribe que esperabas que pasara**
3. **Escribe que esta pasando en realidad**
4. **Lista 3 cosas que ya intentaste**

Muchas veces, al escribir esto, encuentras la solucion.

Si no, ahora tienes una buena pregunta para hacer.

### Tecnica del patito de hule (Rubber Duck)

1. Consigue un objeto (patito, figura, lo que sea)
2. Explicale tu codigo linea por linea
3. Explicale que deberia hacer cada parte
4. A menudo encontraras el error al explicarlo

(Suena tonto. Funciona.)

### Cuando es momento de dejarlo por hoy

- Llevas mas de 2 horas con el mismo problema
- Estas frustrado y ya no piensas claro
- Es tarde y tienes sueno

**Accion:** Deja una nota para tu yo del futuro:
```
DONDE ESTABA:
- Intentando hacer X
- El error es Y
- Ya intente A, B, C
- Manana probar D
```

---

## 4. Se me olvido todo lo que aprendi

### Es normal

El olvido es parte del aprendizaje. No significa que eres tonto.

### Tecnicas de repaso

**1. Espaciado (Spaced Repetition)**
- Repasa al dia siguiente
- Repasa a los 3 dias
- Repasa a la semana
- Repasa al mes

**2. Practica activa**
- No solo veas videos, escribe codigo
- Intenta resolver ejercicios sin ver la solucion primero
- Modifica ejemplos para ver que pasa

**3. Ensena a otros**
- Explica conceptos a un amigo
- Escribe notas con tus propias palabras
- Responde preguntas de otros estudiantes

**4. Crea proyectos pequenos**
- Aplica lo aprendido en algo personal
- Un proyecto propio se recuerda mejor

### Cheatsheets rapidos

*(Se agregaran conforme avance el curso)*

- Sintaxis basica de Kotlin
- Comandos de terminal
- Comandos de Git
- Atajos de IDE

---

## 5. Problemas con el IDE

### IntelliJ IDEA no abre

1. Cierra completamente (incluyendo procesos en segundo plano)
2. Reinicia tu computadora
3. Verifica que tienes suficiente RAM libre
4. Intenta invalidar caches: `File > Invalidate Caches`

### El codigo no se ejecuta

- [ ] Verifica que el archivo tiene funcion `main`
- [ ] Verifica que no hay errores de compilacion (marcas rojas)
- [ ] Click derecho en el archivo > Run

### Autocompletado no funciona

1. Espera unos segundos, a veces tarda en indexar
2. `File > Invalidate Caches / Restart`
3. Verifica que el archivo esta en la carpeta correcta (`src`)

### El IDE esta muy lento

- Cierra otros programas
- Aumenta la memoria del IDE (si sabes como)
- Desactiva plugins que no uses

---

## 6. Problemas con la Terminal

### Comando no encontrado

```
command not found: kotlin
```

**Significa:** El programa no esta instalado o no esta en el PATH.

**Solucion:**
1. Verifica que esta instalado
2. Reinicia la terminal
3. Verifica el PATH (busca "agregar al PATH" + tu sistema operativo)

### Permiso denegado

```
Permission denied
```

**En Mac/Linux:** Agrega `sudo` al inicio (te pedira contrasena)
**En Windows:** Abre terminal como administrador

### Estoy perdido en carpetas

- `pwd` - Donde estoy
- `ls` (Mac/Linux) o `dir` (Windows) - Que hay aqui
- `cd ..` - Ir a carpeta padre
- `cd ~` - Ir a mi carpeta de usuario

---

## 7. Problemas con Git

### "No tengo permisos para hacer push"

1. Verifica que clonaste con tu cuenta
2. Verifica que tienes acceso al repositorio
3. Configura tus credenciales:
   ```
   git config --global user.email "tu@email.com"
   git config --global user.name "Tu Nombre"
   ```

### "Tengo conflictos de merge"

1. Abre los archivos marcados con conflicto
2. Busca las marcas `<<<<<<<`, `=======`, `>>>>>>>`
3. Decide que codigo quieres mantener
4. Elimina las marcas
5. `git add .` y `git commit`

### "Commit accidental - quiero deshacerlo"

**Si aun no hiciste push:**
```
git reset --soft HEAD~1
```

**Si ya hiciste push:** Mejor no tocar. Haz un nuevo commit que corrija.

### "Estoy en la rama equivocada"

```
git stash          # Guardar cambios temporalmente
git checkout main  # Ir a main
git checkout -b rama-correcta  # Crear rama correcta
git stash pop      # Recuperar cambios
```

---

## 8. Donde buscar ayuda

### Recursos oficiales

| Recurso | Para que |
|---------|----------|
| [Documentacion oficial de Kotlin](https://kotlinlang.org/docs/) | Referencia del lenguaje |
| [Stack Overflow](https://stackoverflow.com/) | Preguntas y respuestas |
| [GitHub Discussions](https://github.com/) | Proyectos open source |

### Comunidades en espanol

*(Se actualizara con comunidades recomendadas)*

- Discord del curso (si aplica)
- Reddit r/programacion
- Grupos de Telegram/Discord de Kotlin

### Orden recomendado para buscar ayuda

1. **Google/documentacion** - 5 min
2. **Stack Overflow** - Buscar si alguien pregunto lo mismo
3. **Q&A del curso** - Buscar si otro estudiante pregunto
4. **Q&A del curso** - Hacer tu pregunta
5. **Comunidades** - Si el Q&A no responde

---

## 9. Como hacer buenas preguntas

### Plantilla para preguntas

```
**Que intento hacer:**
[Describe tu objetivo en 1-2 oraciones]

**Que esperaba que pasara:**
[El comportamiento que esperabas]

**Que paso en realidad:**
[El error o comportamiento incorrecto]

**Mi codigo:**
[Pega el codigo relevante]

**Mensaje de error completo:**
[Copia y pega el error]

**Lo que ya intente:**
- [Intento 1]
- [Intento 2]
- [Intento 3]

**Mi entorno:**
- Sistema operativo: [Windows/Mac/Linux]
- Version de Kotlin: [X.X]
- IDE: [IntelliJ IDEA/otro]
```

### Malas preguntas (evita esto)

- "No funciona, ayuda"
- "Por que mi codigo esta mal"
- [Pegar 200 lineas de codigo sin explicacion]
- "Es urgente!!!"

### Buenas preguntas (haz esto)

- Especifica y concreta
- Incluye codigo minimo que reproduce el problema
- Muestra que ya intentaste resolverlo
- Es respetuosa del tiempo de otros

---

## Notas finales

> Este documento se actualizara conforme avance el curso con mas soluciones a problemas comunes.

> Si encuentras un problema que no esta aqui y lo resuelves, consideralo para agregar.

---

**Recuerda:** Todos los programadores, incluso los expertos, consultan documentacion y buscan en Google constantemente. No es senal de debilidad, es parte del trabajo.
