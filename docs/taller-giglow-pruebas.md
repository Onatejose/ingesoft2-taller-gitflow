# Documento de Pruebas

## 1. Descripcion del Sistema
- el sistema debe permitir que los estudiantes se pueda registrar mediante un codigo del estudiante


## 2. Requerimientos a Evaluar

La Plataforma de Gestión de Eventos Universitarios permite registrar estudiantes, validar su código estudiantil e inscribirlos en eventos. El sistema solo acepta estudiantes entre 16 y 65 años. El código estudiantil debe tener 8 caracteres, iniciar con "E" y los 7 restantes ser numéricos. Un estudiante solo puede inscribirse a eventos si está registrado, hay cupos disponibles y no está previamente inscrito. Si alguna condición no se cumple, la inscripción no se permite.

## 2. Requerimientos a Evaluar
 RF02
-Debe tener exactamente 8 caracteres.
-El primer carácter debe ser la letra “E”.
-Los 7 caracteres restantes deben ser numéricos (0-9).
-El sistema debe aceptar el registro únicamente si el código cumple todas las condiciones.
-Si el código no cumple alguna de las reglas, el sistema debe rechazar el registro y mostrar un mensaje de error indicando que el código es inválido.


## RF-03 Inscripción a Evento

Un estudiante podrá inscribirse a un evento solo si:

- Está registrado.
- El evento tiene cupos disponibles.
- No está previamente inscrito.

si alguna condicion no se cumple, el sistema no debe permitir la inscripcion.
---

# 2. Tecnica de prueba seleccionada

Para este requerimiento se usaran las siguientes tecnicas:

- **Análisis de valores límite**

---

# 3. Justificacion

Esta tecnica se selecciona porque el requerimiento define **un rango numérico válido (16–65)**.Por lo que **Valores límite** permite verificar los valores cercanos a los bordes del rango, donde suelen aparecer errores en las validaciones.

---

# 4. Casos de prueba – Análisis de Valores Límite

Rango permitido para la edad:

16 ≤ edad ≤ 65

| Edad | Rango |
|-----|------|
| 15 | Fuera del rango |
| 16 | Dentro del rango |
| 17 | Dentro del rango |
| 64 | Dentro del rango |
| 65 | Dentro del rango |
| 66 | Fuera del rango |

# 5. Validación de cobertura.

La cobertura de pruebas es adecuada porque:

- Se prueban los valores límite críticos:
  - límite inferior
  - límite superior
  - valores inmediatamente antes y después de cada límite.

Esto garantiza que el comportamiento del sistema sea correcto en todo el rango de entrada definido por el requerimiento.

## 3. Tecnicas de Prueba Aplicadas
RF02
Tecnica- Particion de equivalencia
-se usa particion de equivalencia, por que hace que el sistema implemente nuevas reglas como en este caso, son 8 caracteres que necesita como minimo

---
## RF-03 Inscripción a Evento

**Tecnica seleccionada:** Tabla de decisión

**Justificación:** Este tipo de tecnica es la mejor ya que nos permite comparar varias condiciones y acciones para analizar como estas diferentes combinaciones nos pueden llevar a varios resultados y asi ayudandonos para el caso de prueba.

---

## 4. Casos de Prueba Diseñados
RF02
| Criterio |clases validas(V) | Clases invalidas(I) |
|----|------------|----------|
| longitud de caracter | solamente 8 caracteres | menos o mas de 8 caracteres |
|iniciar con la lera E|debe iniciar con la letra E|inicia con cualquier letra menos E|
|7 caracter restantes numericos|los ultimos 7  son numericos|los ultimos no son numericos|


## RF-03 Inscripción a Evento

**Diseño de casos de prueba:**

- **CP-05:** En este caso de prueba se asume que la persona está registrado, el evento tiene cupos disponibles y la persona esta previamente inscrita, por ende el resultado es que se registra exitosamente en el evento. 


| ¿Está registrado? | ¿El evento tiene cupos disponibles? | ¿Está previamente inscrito? | ¿Se registra en el evento? |
|------------------|-----------------------|----------------------|----------------------|
| Sí               | Sí                    | No                   | Sí                   |


- **CP-06:** En este caso de prueba se asume que la persona NO está registrado, el evento tiene cupos disponibles y la persona esta previamente inscrita, por ende el resultado es que se NO registra en el evento. 


| ¿Está registrado? | ¿El evento tiene cupos disponibles? | ¿Está previamente inscrito? | ¿Se registra en el evento? |
|------------------|-----------------------|----------------------|----------------------|
| No               | Si                   | Si                   | No                   |









## 5. Trazabilidad


## 5. Trazabilidad
## 6. Gestion de Versiones (GitFlow)
