
# X5 LoRa Coverage Service

**X5 LoRa Coverage Service** es una aplicación web desarrollada con Flask que permite simular la cobertura de redes LoRa utilizando la API de [CloudRF](https://cloudrf.com/). El usuario puede ingresar parámetros de transmisión y visualizar la cobertura en un mapa interactivo basado en Leaflet.

![Cobertura simulada](static/coverage.png)

---

## 🛠️ Tecnologías utilizadas

- **Python 3.12+**
- **Flask** - Framework web
- **CloudRF API** - Motor de simulación de cobertura
- **HTML + Bootstrap** - Interfaz del usuario
- **Leaflet.js** - Visualización de mapas
- **OpenStreetMap** - Capa base del mapa

---

## 🚀 Instalación y ejecución

### 1. Clona el repositorio

```bash
git clone https://github.com/tu_usuario/x5_lcs.git
cd x5_lcs
```

### 2. Crea un entorno virtual (opcional pero recomendado)

```bash
python -m venv venv
source venv/bin/activate  # En Linux/Mac
venv\Scripts\activate     # En Windows
```

### 3. Instala dependencias

```bash
pip install Flask requests
```

### 4. Ejecuta la aplicación

```bash
python app.py
```

La aplicación se iniciará en [http://localhost:5000](http://localhost:5000)

---

## 🖼️ Cómo usar

1. Ingresa los parámetros del transmisor:
   - Latitud / Longitud
   - Altura de la antena
   - Frecuencia y potencia
   - Ancho de banda
   - Altura del receptor
   - Radio de simulación y resolución

2. Presiona **Simular cobertura**.

3. La imagen generada será renderizada sobre el mapa, mostrando la cobertura estimada.

---

## 📂 Estructura del proyecto

```
├── app.py                # Backend Flask
├── cloudrf_client.py     # Cliente para la API de CloudRF
├── static/
│   └── coverage.png      # Imagen generada de cobertura
├── templates/
│   └── index.html        # Interfaz del usuario
```

---

## 🔒 Seguridad

Este proyecto incluye una clave de API de CloudRF para propósitos de prueba. **No olvides ocultarla o almacenarla de forma segura (por ejemplo, en variables de entorno) si vas a desplegar la app públicamente.**

---

## 📜 Licencia

MIT License. Desarrollado por el equipo de **Mettatec**.

---

## 🙌 Agradecimientos

- [CloudRF](https://cloudrf.com/) por su API de simulación.
- [OpenStreetMap](https://www.openstreetmap.org) y [Leaflet](https://leafletjs.com) por la visualización de mapas.
