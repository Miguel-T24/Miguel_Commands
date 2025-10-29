# 📌 Comandos básicos de Pixi que hemos usado

## Instalación y versión
- Ver la versión instalada de Pixi:
  ```bash
  pixi --version
  ```

## Crear y gestionar proyectos
- Inicializar un nuevo proyecto con Pixi:
  ```bash
  pixi init
  ```
- Instalar dependencias declaradas en `pixi.toml` (o desde el lock):
  ```bash
  pixi install
  pixi install --locked
  ```

  ## Usar el entorno
- Entrar en la shell del entorno (ahí todo apunta a lo que definiste en Pixi):
  ```bash
  pixi shell
  ```

## Buscar dependendias
```bash
pixi search python
pixi search rust
```

## Añadir / quitar dependencias
- Añadir una dependencia (ejemplo: Rust 1.89.0):
  ```bash
  pixi add rust=1.89.0
  ```
- Eliminar una dependencia:
  ```bash
  pixi remove rust
  ```

## Listar dependencias instaladas
- Ver lo que está en el entorno actual:
  ```bash
  pixi list
  ```

- Ejecutar un comando puntual dentro del entorno, sin entrar en shell:
  ```bash
  pixi run <comando>
  ```
  Ejemplos:
  ```bash
  pixi run rustc --version
  pixi run cargo --version
  pixi run cargo build
  pixi run cargo run
  ```

## Información útil
- Ver en qué ruta se instaló un binario (ej. dentro de `pixi shell`):
  ```bash
  which rustc      # Linux/Mac
  where rustc      # Windows (CMD)
  Get-Command      # Windows (Powershell)
  ```

## Añadir el kernel a jupyter
```bash
pixi add ipykernel
python -m ipykernel install --user --name=pixi-analisis --display-name "<Nombre del Kernel>"
```
