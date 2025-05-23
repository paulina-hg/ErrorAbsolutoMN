

## Apuntes Teóricos

### 1. Error Absoluto
El error absoluto mide la diferencia entre el valor real y el valor medido o estimado:

\[
Error\ Absoluto = |Valor\ Real - Valor\ Medido|
\]

Este tipo de error da la magnitud del error sin importar el signo.

---

### 2. Error Relativo
El error relativo representa el error absoluto en proporción al valor real, usualmente expresado en porcentaje:

\[
Error\ Relativo = \frac{|Valor\ Real - Valor\ Medido|}{|Valor\ Real|} \times 100\%
\]

Es útil para comparar la precisión de mediciones en distintas escalas.

---

### 3. Error de Redondeo
El error de redondeo se genera al ajustar un número a una cantidad finita de cifras decimales o cifras significativas. Se calcula como:

\[
Error\ Redondeo = |Valor\ Original - Valor\ Redondeado|
\]

Este error depende de cómo y a cuántas cifras se redondea el valor original.

---

### 4. Error de Truncamiento
El error de truncamiento ocurre cuando se elimina información después de cierto punto decimal sin redondear, es decir, cortando simplemente:

\[
Error\ Truncamiento = |Valor\ Original - Valor\ Truncado|
\]

Generalmente es menor o igual al error de redondeo para la misma cantidad de cifras consideradas.

---

### 5. Errores de Propagación
Los errores de propagación indican cómo las incertidumbres individuales afectan el resultado de operaciones combinadas:

- Para suma y resta: los errores se suman directamente  
- Para multiplicación y división: se calcula usando la fórmula:

\[
Error = |Resultado| \times \sqrt{\left(\frac{Error_1}{Valor_1}\right)^2 + \left(\frac{Error_2}{Valor_2}\right)^2}
\]

Ejemplo: Cálculo de resistencia equivalente en paralelo considerando errores de medición en las resistencias individuales.

---

### 6. Precisión en Mediciones
La precisión mide la diferencia entre un valor medido y el valor reportado o calculado, indicando la exactitud del instrumento o método.

Para áreas, como la de un círculo:

\[
Precisión\ Área = |Área\ Real - Área\ Reportada|
\]

---

## Uso

Cada módulo implementa una clase con métodos estáticos para calcular cada tipo de error o precisión. Se puede importar la clase deseada y utilizar los métodos `calcular` para obtener los resultados.

---

## Ejemplo

```python
from error_absoluto import ErrorAbsoluto

error = ErrorAbsoluto.calcular(2.50, 2.45)
print(f"Error absoluto: {error}")
