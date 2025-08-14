# promptImg

> Generador **local** de *prompts* para imagen y video con **presets integrados** y filtros.  
> 100% en el navegador — sin backend, sin registro, sin telemetría.

---

## ✨ Características

- **Local y privado:** todo ocurre en tu navegador (HTML + JS).
- **Presets listos para usar:** biblioteca homogénea por categorías en imagen y video.
- **Filtro rápido por texto** y selector de categorías.
- **Modo oscuro/claro** conmutables.
- **Atajos de teclado** que aceleran el flujo.
- **Importar / Exportar presets** en JSON.
- **Responsive:** UX cuidada en escritorio y móvil (el subtítulo de marca se oculta en pantallas pequeñas).

> **Marca:** `promptImg` (título con acento visual en “Img”).

---

## 📦 Instalación / uso rápido

1. Clona o descarga este repositorio.
2. Abre el archivo **`index.html`** directamente en el navegador.
3. ¡Listo! No necesitas Node, ni build, ni dependencias.

> Si vas a editar el archivo con frecuencia, puedes usar cualquier servidor estático local (opcional).

```bash
# Ejemplo con Python 3
python -m http.server 8080
# Abre: http://localhost:8080/index.html
```

---

## 🧭 Uso

- Explora las **categorías** desde el selector.
- Filtra con el **buscador** (en vivo).
- Pulsa un **preset** para ver/copiar sus detalles o **aplicarlo** a tu flujo.

### Atajos de teclado

- `Ctrl / Cmd + Enter` → ejecutar acción principal (generación).
- `Shift + Enter` → salto de línea (en campos de texto).
- `/` → enfocar el buscador.

> Los atajos están pensados para no interferir con la edición de texto. Si un campo tiene foco, se prioriza tu escritura.

---

## 🔁 Importar / Exportar presets

- **Exportar**: genera un JSON con tus presets personalizados.
- **Importar**: selecciona un JSON previamente exportado para cargarlos.

### Formato de ejemplo

```json
{
  "version": "1.0",
  "customImg": [
    {
      "id": 9991,
      "nombre": "Retrato: realismo suave",
      "descripcion": "Realismo fotográfico, luz suave, plano medio",
      "categoria": "Retrato",
      "estilo": "Realismo fotográfico",
      "iluminacion": "Luz suave difusa",
      "encuadre": "Plano medio",
      "formato": "3:2 · 2048×1365"
    }
  ],
  "customVid": []
}
```

> Las propiedades pueden variar ligeramente según el preset. La app mantiene la compatibilidad durante la importación.

---

## 🛠 Personalización

- **Marca / Cabecera:** el título principal usa `brand-title` y `brand-accent`.  
  Ajusta tipografía y colores en CSS (respetando variables como `--accent` y `--border`).
- **Subtítulo:** se oculta automáticamente en móvil (`@media (max-width: 600px)`).
- **Estilos:** se emplea CSS moderno con *clamp()* y `prefers-reduced-motion` para accesibilidad.

---

## 🗂 Estructura mínima del repo

```
.
├─ index.html   # App (single-file)
└─ LICENSE
```

---

## 🗺️ Hoja de ruta (sugerencias)

- Contador opcional `(N)` en el selector de categorías.
- Normalización/agrupado de categorías (p. ej., “Fantasía”, “Ciencia ficción”, “Otros”).
- Mejoras de accesibilidad (navegación por teclado ampliada, etiquetas ARIA adicionales).
- Exportación de presets con metadatos extendidos.
- Favicon / logo SVG.

---

## 🤝 Contribuir

1. Abre un *issue* con la propuesta/bug.
2. *Fork* → rama (`feat/...` o `fix/...`).
3. Pull Request con una descripción clara y capturas si aplica.

> Mantén la app en **un solo archivo** cuando sea posible (principio del proyecto).

---

## 🧾 Licencia

Este proyecto se publica bajo la licencia **MIT**. Consulta el archivo `LICENSE` para más detalles.

---

## ❓FAQ

**¿Funciona sin conexión?**  
Sí. Es un HTML estático; puedes abrirlo localmente o servirlo desde cualquier hosting estático.

**¿Mis datos salen de mi equipo?**  
No. Todo sucede en tu navegador.

**¿Puedo añadir mis propios presets?**  
Sí. Úsalos desde la UI y **expórtalos** en JSON para respaldarlos o compartirlos.

**¿Dónde reporto fallos o ideas?**  
En la pestaña **Issues** del repositorio.

---

Hecho con ❤️ para acelerar tu flujo creativo.
