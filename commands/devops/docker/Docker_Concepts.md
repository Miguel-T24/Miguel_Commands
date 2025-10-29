# 📋 Conceptos Fundamentales de Docker

| Concepto              | Definición |
|------------------------|------------|
| **Imagen (Image)**     | Plantilla inmutable que contiene el sistema operativo, dependencias y la aplicación a ejecutar. Es como una "foto" de un entorno listo para usar. |
| **Contenedor (Container)** | Instancia en ejecución de una imagen. Es ligero, aislado y contiene todo lo necesario para que la aplicación funcione. |
| **Dockerfile**         | Archivo de texto con instrucciones para construir una imagen personalizada (qué base usar, qué paquetes instalar, qué comandos ejecutar). |
| **Docker Hub**         | Repositorio público en la nube donde se almacenan y comparten imágenes Docker, similar a GitHub pero para contenedores. |
| **Volumen (Volume)**   | Mecanismo para almacenar datos persistentes fuera del ciclo de vida del contenedor (ya que los contenedores son efímeros). |
| **Red (Network)**      | Sistema de comunicación que conecta contenedores entre sí y con el host. Docker ofrece drivers de red como `bridge`, `host`, `overlay`. |
| **Registro (Registry)**| Servidor donde se guardan imágenes Docker (ejemplo: Docker Hub, GitLab Registry, Amazon ECR). |
| **Orquestador**        | Herramienta que gestiona múltiples contenedores y su escalabilidad. Ejemplos: **Docker Swarm** y **Kubernetes**. |
| **Docker Compose**     | Herramienta para definir y ejecutar aplicaciones multi-contenedor mediante un archivo `docker-compose.yml`. |
| **Capas (Layers)**     | Cada instrucción en un Dockerfile genera una capa inmutable. Docker reutiliza estas capas para optimizar la construcción y ahorrar espacio. |
| **Daemon (dockerd)**   | Proceso principal que ejecuta en segundo plano y gestiona contenedores, imágenes y redes. |
| **Cliente (CLI)**      | Interfaz de línea de comandos (`docker`) que permite al usuario interactuar con el daemon para crear, ejecutar y administrar contenedores. |

# Herramientas para balanceo de carga y Failover
- Failover automático: **Patroni**
- Balanceador de conexiones: **HAProxy**

# Herramientas para balanceo de carga con kubernets / Docker
- KV8
- Zalando Postgres Operator