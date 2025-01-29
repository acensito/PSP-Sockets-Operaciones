# 📌 Descripción de la Práctica  
Desarrollarás un **servidor concurrente** en **Java** que escuche en el **puerto 6000 (TCP)** y procese operaciones matemáticas de **suma y resta**.  

Cada cliente podrá elegir entre dos modos de uso:  

1. **Modo manual**: Introduce una operación y recibe el resultado.  
2. **Modo automático**: Genera **X operaciones aleatorias**, las envía al servidor y recibe los resultados.  

---

# 🖥️ Requisitos Técnicos  

## Servidor (Concurrente)  
- Escucha conexiones en el **puerto 6000** usando `ServerSocket`.  
- Crea un **hilo** por cada cliente conectado.  
- **Analiza** la cadena recibida:  
  - Si es una operación válida (`"A+B"` o `"A-B"`), calcula y envía el resultado.  
  - Si es inválida, responde con un **mensaje de error** y **cierra la conexión**.  
- **Maneja múltiples clientes** simultáneamente con hilos.  

## Cliente (Interfaz de Elección)  
- Se conecta al **servidor en el puerto 6000**.  
- Muestra un **menú** con dos opciones:  
  1. **Modo manual** → Permite introducir una operación y recibir el resultado.  
  2. **Modo automático** → Genera **X operaciones aleatorias** (`A op B`) y muestra sus resultados.  
- Envía la operación al servidor y recibe la respuesta.  
- **Maneja errores**, como servidor no disponible o respuesta incorrecta.  

---

# 🚀 Extras Opcionales  
Si quieres hacer la práctica más completa:  
- [ ] **Soporte de espacios en la operación** (`"10 + 5"` en vez de `"10+5"`). 
- [ ] **Extender operaciones** a multiplicación y división (`*`, `/`).  
- [ ] **Evitar división por cero**.  
- [ ] **Registro de conexiones** en el servidor con logs.  
- [ ] **Soporte para varios clientes simultáneos** y manejo de desconexiones.
