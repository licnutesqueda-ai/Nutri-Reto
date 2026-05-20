# 🍎 NutriReto DIF Irapuato

Juego educativo interactivo sobre nutrición y hábitos saludables, desarrollado para la DIF Irapuato.

## 🎮 Características

### 📚 Tres Niveles de Dificultad

| Nivel | Tiempo | Puntos | Características |
|-------|--------|--------|------------------|
| 🟢 **Fácil** | 15 segundos | 10 pts | Preguntas básicas, más tiempo para responder |
| 🟡 **Normal** | 12 segundos | 15 pts | Preguntas intermedias, mayor desafío |
| 🔴 **Difícil** | 8 segundos | 20 pts | Preguntas avanzadas, muy desafiante |

### ✨ Funcionalidades

- ✅ **45 preguntas** categorizadas por dificultad (15 por nivel)
- 🎵 **Música y efectos de sonido** durante el juego
- 🎉 **Animación de confeti** al responder correctamente
- 🏆 **Sistema de ranking** con persistencia local
- 📱 **Diseño responsive** para móviles y desktop
- ⏱️ **Barra de tiempo visual** con alertas de color
- 💾 **Guardado automático** de resultados
- 🎯 **Selector de dificultad** antes de empezar
- 🔀 **Preguntas aleatorizadas** cada partida

## 🚀 Cómo Usar

### Opción 1: En Línea (Más Fácil)
1. Abre el archivo `index.html` directamente en tu navegador
2. Selecciona tu nivel de dificultad (🟢 Fácil, 🟡 Normal, 🔴 Difícil)
3. ¡Responde las preguntas sobre nutrición!
4. Visualiza tu posición en el ranking al finalizar

### Opción 2: Servidor Local

**Con Python 3:**
```bash
python -m http.server 8000
```

**Con Node.js (http-server):**
```bash
npm install -g http-server
http-server
```

Luego abre: `http://localhost:8000`

## 📋 Preguntas por Dificultad

### 🟢 Nivel Fácil (15 preguntas)
- Conceptos básicos de nutrición
- Combinaciones saludables
- Beneficios del agua
- Alternativas saludables vs ultraprocesados
- Grupos de alimentos

### 🟡 Nivel Normal (15 preguntas)
- Vitaminas y minerales específicos
- Función de nutrientes
- Carbohidratos complejos
- Grasas saludables (Omega-3)
- Nutrición en grupos especiales (adultos mayores)
- Presupuesto saludable

### 🔴 Nivel Difícil (15 preguntas)
- Índice glucémico
- Aminoácidos esenciales
- Antioxidantes (Glutatión, Polifenoles)
- Biodisponibilidad de nutrientes
- Síndrome metabólico
- Microbioma intestinal
- Inflamación crónica

## 💾 Almacenamiento

El juego guarda automáticamente:
- ⭐ Puntuaciones finales
- 🎯 Nivel alcanzado
- 🟢🟡🔴 Dificultad jugada
- 📅 Fecha de la partida
- 👤 Nombre del jugador

**Datos almacenados en:** `localStorage` del navegador (sin conexión a internet)

## 🛠️ Técnica

### Tecnologías Usadas
- **HTML5** - Estructura semántica
- **CSS3** - Estilos responsive y animaciones fluidas
- **JavaScript Vanilla** - Lógica del juego sin dependencias
- **localStorage** - Persistencia de datos en el cliente

### Estructura del Código

```javascript
// Base de preguntas por dificultad
questionsByDifficulty = {
  easy: [[pregunta, [opciones], índiceCorrecta], ...],
  normal: [...],
  hard: [...]
}

// Configuración de cada dificultad
difficultySettings = {
  easy: { time: 15, multiplier: 1, label: "🟢 FÁCIL" },
  normal: { time: 12, multiplier: 1.5, label: "🟡 NORMAL" },
  hard: { time: 8, multiplier: 2, label: "🔴 DIFÍCIL" }
}
```

## 📊 Sistema de Puntos

- **Fácil**: 10 puntos × 1 = **10 puntos por respuesta**
- **Normal**: 10 puntos × 1.5 = **15 puntos por respuesta**
- **Difícil**: 10 puntos × 2 = **20 puntos por respuesta**

*Puntos multiplicados automáticamente según la dificultad seleccionada*

## 🎨 Personalización

### Cambiar Colores de Dificultad

```css
/* En la sección <style> */
.difficulty-btn.easy { background: #27ae60; }    /* Verde */
.difficulty-btn.normal { background: #f39c12; }  /* Naranja */
.difficulty-btn.hard { background: #e74c3c; }    /* Rojo */
```

### Agregar Nuevas Preguntas

```javascript
easy: [
  ["Tu pregunta aquí?", ["Opción 1", "Opción 2", "Opción 3"], 0],
  // 0 = índice de respuesta correcta (primera opción)
  // 1 = segunda opción, etc.
]
```

### Modificar Tiempo y Puntos

```javascript
difficultySettings = {
  easy: { time: 15, multiplier: 1, label: "🟢 FÁCIL" },
  normal: { time: 12, multiplier: 1.5, label: "🟡 NORMAL" },
  hard: { time: 8, multiplier: 2, label: "🔴 DIFÍCIL" }
}
```

## 🐛 Solución de Problemas

### El audio no se reproduce
- Verifica tu conexión a internet (usa URLs externas de Mixkit y Bensound)
- Algunos navegadores requieren interacción del usuario antes de reproducir audio
- Intenta hacer clic en el juego primero

### El ranking no se guarda
- Asegúrate de que localStorage está habilitado en tu navegador
- Prueba en modo normal (no incógnito)
- Verifica que JavaScript esté habilitado

### Las preguntas no aparecen
- Abre la consola del navegador (F12 o Ctrl+Shift+I)
- Revisa si hay errores en la sección "Console"
- Verifica que JavaScript esté habilitado

### El juego va muy lento
- Cierra otras pestañas/aplicaciones
- Limpia el cache del navegador
- Intenta en otro navegador

## 📱 Compatibilidad

✅ **Navegadores:** Chrome, Firefox, Safari, Edge (versiones modernas)  
✅ **Dispositivos:** Móviles (iOS, Android), Tablets, Desktop  
✅ **Sistemas Operativos:** Windows, macOS, Linux  

## 👨‍🏫 Facilitador

**Guillermo Alberto Mosiño Esqueda**

DIF Irapuato - Programa de Nutrición y Salud

## 📝 Licencia

Libre para uso educativo y no comercial. Puede ser modificado y compartido respetando la autoría.

## 🌱 Mensaje

> "La nutrición es clave para una vida digna y saludable. ¡Aplica lo aprendido!"

---

**Última actualización:** Mayo 2025  
**Versión:** 2.0 (Con dificultad variable)  
**Estado:** ✅ Funcional y Optimizado