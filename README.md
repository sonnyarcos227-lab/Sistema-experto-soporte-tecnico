# SE-DIAG · Sistema Experto para Diagnóstico de Fallas en Computadores

Sistema experto interactivo para el diagnóstico de fallas comunes en computadores de escritorio y portátiles, desarrollado como proyecto de la asignatura **Sistemas Expertos** en el **Instituto Tecnológico del Putumayo (ITP)**.

🔗 **Demo en vivo:** [_agrega aquí la URL una vez publicada (Netlify / GitHub Pages)_](https://sonnyarcos227-lab.github.io/Sistema-experto-soporte-tecnico/)

---

## 📌 Descripción

El proyecto simula el funcionamiento de un sistema experto real de soporte técnico de primer nivel: el usuario describe una falla (o la selecciona de una lista), y el motor de inferencia la compara contra una base de conocimiento de **30 reglas de producción** (`SI síntoma ENTONCES diagnóstico`) para entregar una conclusión y una solución recomendada, siguiendo un encadenamiento hacia adelante (*forward chaining*).

La interfaz visualiza en tiempo real las 4 componentes clásicas de la arquitectura de un sistema experto y cómo interactúan entre sí durante una consulta.

## 🧠 Arquitectura implementada

| Componente | Implementación en el proyecto |
| --- | --- |
| **Base de conocimiento** | 30 reglas SI → ENTONCES sobre fallas de Hardware, Software/SO, Red, Periféricos y Otros, cada una con su solución recomendada. |
| **Base de hechos** | El síntoma ingresado por el usuario en cada consulta, junto con el historial de la sesión. |
| **Motor de inferencia** | Algoritmo de coincidencia por palabras clave que compara el hecho ingresado contra las 30 reglas y determina la de mayor coincidencia (encadenamiento hacia adelante). |
| **Interfaz de usuario** | Dashboard web: campo de texto libre, lista de fallas filtrable por categoría, y panel de resultado con la regla aplicada y la solución. |

## ✨ Características

- Diagnóstico por **texto libre** (describir el síntoma con tus propias palabras) o por **selección directa** de una de las 30 fallas conocidas.
- Filtro por categoría: Hardware, Software/SO, Red, Periféricos, Otros.
- Animación de la arquitectura del sistema experto mostrando el flujo de datos entre sus 4 componentes en cada consulta.
- Indicador de nivel de coincidencia por diagnóstico.
- Bitácora de la base de hechos con el historial de consultas de la sesión.
- Interfaz de una sola página (HTML/CSS/JS puro), sin dependencias externas de backend.

## 🛠️ Tecnologías

- HTML5 / CSS3 / JavaScript (vanilla, sin frameworks)
- Sin backend ni base de datos: toda la base de conocimiento vive en el propio archivo, lista para desplegarse como sitio estático

## 🚀 Cómo ejecutarlo localmente

1. Clona este repositorio o descarga `index.html`.
2. Ábrelo directamente en cualquier navegador (doble clic sobre el archivo).

No requiere instalación, servidor ni dependencias.

## 🌐 Publicación

El sitio está pensado para desplegarse como página estática en:
- **GitHub Pages** (Settings → Pages → Branch `main` → carpeta `/`)
- **Netlify** (arrastrando `index.html` a [Netlify Drop](https://app.netlify.com/drop))

## 📋 Base de conocimiento

Las 30 reglas se agrupan en cinco categorías:

- **Hardware** (10 reglas): fuentes de poder, RAM, discos, sobrecalentamiento, tarjeta madre, batería CMOS, puertos USB, entre otras.
- **Software / Sistema Operativo** (10 reglas): pantallas azules (BSOD), boot loops, lentitud, malware, ransomware, drivers de video.
- **Red** (4 reglas): DHCP, Wi-Fi, velocidad de conexión, Ethernet.
- **Periféricos** (5 reglas): teclado, mouse, impresora, monitor, audio.
- **Otros** (1 regla): fallas tras actualización de BIOS.

## ⚠️ Uso educativo

Este sistema experto fue desarrollado con fines académicos para ilustrar la arquitectura y el funcionamiento de un motor de inferencia por reglas. No reemplaza la evaluación de un técnico certificado. Ante riesgo eléctrico, olor a quemado o daño físico visible, desconecta el equipo y busca soporte especializado.

## 👤 Autor

**Sonny Ferney Arcos Duarte**
Instituto Tecnológico del Putumayo (ITP) — Asignatura: Sistemas Expertos
