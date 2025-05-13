# Cripto-Tarea-Rainbow
Link al repositorio-->  https://github.com/josean9/Cripto-Tarea-Rainbow.git

## 📝 Resumen de la Tarea

### 🎯 Objetivo
El objetivo de esta práctica es aplicar un ataque de precomputación mediante **Rainbow Tables** para invertir funciones hash, en este caso el algoritmo **MD5**, sobre un espacio reducido de contraseñas de 4 dígitos (`"0000"` a `"9999"`).

---

### 🔧 ¿Qué hemos hecho?

1. **Construcción de la Rainbow Table**  
   Se generaron todas las contraseñas posibles de 4 cifras y se aplicaron 4 pasos de transformación (hash + reducción) para obtener un `endpoint`. Se almacenó una tabla `{endpoint: contraseña_inicial}` con 3.157 entradas únicas, descartando colisiones.

2. **Ataque a una contraseña real**  
   Se eligió la contraseña `"1234"` y se calculó su `endpoint`. Ese endpoint fue buscado en la tabla y permitió recuperar correctamente la contraseña original.

3. **Análisis**  
   Se observaron **colisiones** (ya que no se almacenaron las 10.000 posibles contraseñas) y se comprobó que el ataque fue exitoso al recuperar el hash objetivo. Se discutieron los posibles **falsos positivos** que pueden aparecer en este tipo de ataque.

---
