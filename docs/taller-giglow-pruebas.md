# Documento de Pruebas

## 1. Descripcion del Sistema

## 2. Requerimientos a Evaluar

# RF01 – Registro de estudiantes por edad

#1 Analisis del requerimiento

- Edad minima permitida: **16**
- Edad maxima permitida: **65**
- Si la edad es **menor a 16**, el registro debe ser **rechazado**.
- Si la edad es **mayor a 65**, el registro debe ser **rechazado**.

Dominio de entrada: **edad del estudiante**.

---

## 3. Tecnicas de Prueba Aplicadas

-Tecnica de prueba seleccionada

Para este requerimiento se usaran las siguientes tecnicas:

- **Análisis de valores límite**

---

-Justificacion

Esta tecnica se selecciona porque el requerimiento define **un rango numérico válido (16–65)**.Por lo que **Valores límite** permite verificar los valores cercanos a los bordes del rango, donde suelen aparecer errores en las validaciones.

---

## 4. Casos de Prueba Diseñados


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

-Validación de cobertura.

La cobertura de pruebas es adecuada porque:

- Se prueban los valores límite críticos:
  - límite inferior
  - límite superior
  - valores inmediatamente antes y después de cada límite.

Esto garantiza que el comportamiento del sistema sea correcto en todo el rango de entrada definido por el requerimiento.

## 5. Trazabilidad

## 6. Gestion de Versiones (GitFlow)
