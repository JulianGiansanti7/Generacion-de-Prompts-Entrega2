# 🌿 GreenBot – Asistente Virtual de Jardinería  
> **Segunda Entrega** – Generación de Prompts  

![Banner](https://img.shields.io/badge/Estado-En%20Desarrollo-yellow)
![Python](https://img.shields.io/badge/Python-3.10-blue)
![IA](https://img.shields.io/badge/IA-Prompt%20Engineering-green)

---

## 📝 Introducción  

**GreenBot** es un asistente virtual diseñado para **automatizar la generación de presupuestos** y la **gestión de la agenda** de un jardinero, utilizando técnicas de **prompt engineering** e **inteligencia artificial**.  

El proyecto busca optimizar la comunicación entre clientes y jardineros, ofreciendo respuestas rápidas, claras y precisas sobre presupuestos, disponibilidad y horarios.

---

## ❗ Presentación del problema  

Los jardineros independientes suelen gestionar de forma **manual** la solicitud de trabajos, los presupuestos y la agenda. Esto trae varios inconvenientes:  

- Demoras en responder a los clientes.  
- Falta de organización en los horarios.  
- Presupuestos inconsistentes o poco claros.  
- Mala experiencia para el cliente.  

**Relevancia del proyecto:**  
Un asistente virtual permite **automatizar** estas tareas, mejorando la **eficiencia**, reduciendo **errores humanos** y brindando **mayor comodidad** tanto para el cliente como para el jardinero.  

---

## 💡 Propuesta de solución  

La solución consiste en desarrollar un **asistente virtual inteligente** que:  

- Reciba **datos del cliente**: nombre, tipo de trabajo, tamaño del terreno y fecha disponible.  
- Genere un **presupuesto estimado** en base al tipo de trabajo y tamaño del área.  
- Verifique la **disponibilidad del jardinero** en la fecha solicitada.  
- Proponga un **horario adecuado** para realizar el trabajo.  
- Devuelva una **respuesta clara, cordial y personalizada**.  

---

## 🤖 Relación con la IA y uso de Prompts  

El proyecto se basa en el uso de **técnicas de prompting** para interactuar con un modelo de **IA generativa**.  

**Prompt base propuesto:** 

Eres un Asistente de Jardinería. Recibirás mensajes de clientes con: nombre, dirección, teléfono, problema a resolver, fecha y horario disponible. Genera un presupuesto basado en estos precios:

### Corte de pasto:

- Corte: $100/m²

- Recolección de restos: $20/m² (opcional)

### Poda de arbustos:

- Pequeños: $5.000

- Medianos: $8.000

- Grandes: $12.000

### Poda de árboles:

- Normales: $30.000

- Grandes (>8m): $45.000

- Palmeras: $10.000

- Recolección de ramas: $15.000 (opcional)

### Extracción de árboles:

- 2–4m: $100.000

- 4–8m: $140.000

- 8–15m (grúa): $200.000

- más de 15m (grúa): $300.000

- Recolección de ramas: $50.000

##### Nota: Si se necesita grúa o volquete, agregar el costo extra que cobre la empresa de alquiler.

### Costos adicionales por alquiler:
- Grúa: $250.000 (agregar si el trabajo requiere)
- Volquete: $75.000 (agregar si el cliente lo necesita)

## Salida esperada:

Nombre Cliente: [Nombre]  
Dirección: [Dirección]  
Número de teléfono: [Teléfono]  
Fecha Disponible: [DD/MM/AAAA] (hora)  

Tipo de Trabajo: [Descripción con medidas y categoría]  
Presupuesto: [Detalle de costos, incluyendo opcionales]  
Total: [Suma total]

Un jardinero se pondra en contacto contigo en las proximas 24hs! 

#### saludos!


***Ejemplo de entrada:*** 

"Hola, me llamo Julian Giansanti, necesito podar un árbol de 10m que bloquea el sol en mi quincho. Vivo en Manuel Belgrano 999, estoy disponible este viernes 12 de septiembre a partir de las 12 del mediodía, mi número es 341-1234-567."

***Ejemplo de salida:***

Nombre Cliente: Julian Giansanti  
Dirección: Manuel Belgrano 999  
Número de teléfono: 341-1234-567  
Fecha Disponible: 12/09/2025 (a partir de las 12:00 hs)  

Tipo de Trabajo: Poda de árbol de 10 metros (Grande)  
Presupuesto: Poda de árbol grande: $45.000 + Recolección (opcional) $15.000  
Total: $60.000

Un jardinero se pondra en contacto contigo en las proximas 24hs! 

#### saludos!

**FIN DE EJEMPLOS**

ahora cuando un cliente deje una nota, genera esa nueva nota: 
{user_input}

---


## ✅ Justificación de la viabilidad  

El proyecto es **viable** porque:  

- Los modelos de IA (como GPT-5) ya están entrenados, por lo que solo se requiere diseñar buenos prompts.  
- No se necesitan grandes recursos, basta con un entorno de desarrollo local.  
- La agenda del jardinero puede gestionarse inicialmente en **JSON** o una **base de datos ligera**.  
- El prototipo puede construirse en un tiempo razonable utilizando **Python** y librerías simples.  

---

## 🎯 Objetivos  

### **Objetivo general**  
Crear un asistente virtual que automatice presupuestos y gestione la agenda de jardinería.  

### **Objetivos específicos**  
- Diseñar prompts efectivos para interpretar datos del cliente.  
- Calcular presupuestos de manera automática.  
- Verificar disponibilidad del jardinero.  
- Mejorar la experiencia de comunicación con el cliente.  

---

## 🛠️ Metodología  

El proyecto se desarrollará en **seis etapas**:  

1. **Relevamiento de requerimientos** → definir qué datos necesita el asistente.  
2. **Diseño de prompts** → probar diferentes estructuras para obtener respuestas claras.  
3. **Desarrollo del prototipo** → implementar el asistente básico.  
4. **Integración de agenda y tarifas** → cargar precios y horarios disponibles.  
5. **Pruebas y mejoras** → verificar exactitud y coherencia de respuestas.  
6. **Documentación final** → preparar la entrega y README.  
