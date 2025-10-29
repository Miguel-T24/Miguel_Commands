# 🧠 Guía rápida de comandos `uv`


### 💡 Ejemplos rápidos de comandos mas usados

```bash
# Crear proyecto y entorno
uv init mi_app
cd mi_app
```

### Entrar al entorno virtual
```bash
# linux
source .venv/bin/activate
```

```bash
#Windows
.\.venv\Scripts\Activate
```

### Instalar dependencias
```bash
uv add requests rich
```
### Ejecutar la aplicación
```bash
# Dentro del entorno virtual
python main.py
```
```bash
# Fuera del entorno virtual
uv run python main.py
```
### Exportar a requirements.txt para usuarios con virtualenv
```bash
uv export --format requirements-txt > requirements.txt
```
### Reinstalar entorno idéntico (cualquier sistema operativo)
```bash
uv sync --frozen
```
---


Lista completa de comandos útiles de **uv**, con descripción corta y ejemplos prácticos.  
Compatible con Windows, Linux y macOS.

---

## 🔧 Inicialización y entorno

**Comando:** `uv init`  
**Descripción:** Crea un nuevo proyecto con `pyproject.toml` y entorno virtual listo.  
**Ejemplo:**  
```bash
uv init mi_proyecto
```

**Comando:** `uv venv`  
**Descripción:** Crea manualmente un entorno virtual en `.venv/`.  
**Ejemplo:**  
```bash
uv venv
```

**Comando:** `uv run <comando>`  
**Descripción:** Ejecuta un comando dentro del entorno sin activarlo.  
**Ejemplo:**  
```bash
uv run python main.py
```

**Comando:** `uv python`  
**Descripción:** Muestra la ruta del intérprete de Python usado por uv.  
**Ejemplo:**  
```bash
uv python
```

---

## 📦 Manejo de dependencias

**Comando:** `uv add <paquete>`  
**Descripción:** Instala dependencias desde PyPI y actualiza `pyproject.toml` y `uv.lock`.  
**Ejemplo:**  
```bash
uv add fastapi uvicorn[standard]
```

**Comando:** `uv remove <paquete>`  
**Descripción:** Elimina un paquete del entorno y de los archivos de dependencias.  
**Ejemplo:**  
```bash
uv remove fastapi
```

**Comando:** `uv sync`  
**Descripción:** Instala todas las dependencias listadas en `pyproject.toml` o `uv.lock`.  
**Ejemplo:**  
```bash
uv sync
```

**Comando:** `uv sync --frozen`  
**Descripción:** Instala dependencias usando las versiones exactas del `uv.lock` (reproducible en cualquier SO).  
**Ejemplo:**  
```bash
uv sync --frozen
```

**Comando:** `uv lock`  
**Descripción:** Genera o actualiza el archivo `uv.lock` (bloquea versiones exactas).  
**Ejemplo:**  
```bash
uv lock
```

---

## 📂 Exportar e interoperar con pip/virtualenv

**Comando:** `uv export --format requirements-txt > requirements.txt`  
**Descripción:** Exporta las dependencias a un `requirements.txt` compatible con `pip install -r`.  
**Ejemplo:**  
```bash
uv export --format requirements-txt > requirements.txt
```

---

## 🧰 Herramientas de inspección y limpieza

**Comando:** `uv tree`  
**Descripción:** Muestra un árbol de dependencias instaladas.  
**Ejemplo:**  
```bash
uv tree
```

**Comando:** `uv pip <subcomando>`  
**Descripción:** Permite usar comandos pip dentro del entorno (como `list`, `install`, etc.).  
**Ejemplo:**  
```bash
uv pip list
```

**Comando:** `uv clean`  
**Descripción:** Limpia archivos temporales y el entorno virtual.  
**Ejemplo:**  
```bash
uv clean
```

**Comando:** `uv cache list`  
**Descripción:** Muestra los paquetes almacenados en caché local.  
**Ejemplo:**  
```bash
uv cache list
```

**Comando:** `uv cache clean`  
**Descripción:** Elimina toda la caché de paquetes.  
**Ejemplo:**  
```bash
uv cache clean
```

---


## ✅ Archivos importantes

| Archivo | Descripción |
|----------|-------------|
| `pyproject.toml` | Define dependencias del proyecto |
| `uv.lock` | Bloquea versiones exactas para reproducibilidad |
| `requirements.txt` | Compatible con `pip install -r` |

---
