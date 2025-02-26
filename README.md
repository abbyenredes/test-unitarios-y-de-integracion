# Vamos a crear nuestros propios test unitarios y de integración

## Acerca del proyecto
Vamos a crear test que nos ayuden a pulir y optimizar nuestro código.

## Mis herramientas
* Ciclo de vida del software con efoque ágil: [desarrolo de software](https://www.canvia.com/ciclo-vida-desarrollo-software/)
* Desarrollo de software paso a paso: [desarrolla paso a paso](https://www.red-tic.unam.mx/desarrollo-de-software)
* Claves de un buen testing: [Testing](https://www.linkedin.com/pulse/por-qu%C3%A9-el-testing-es-clave-en-desarrollo-de-software-cristian/)
* ¿Por qué? buenas practicas: [puebas unitarias](https://yeeply.com/blog/tendencias-habilidades/que-son-pruebas-unitarias/)
* Diferencia entre test unitarios y de integración: [test unitarios vs test integracion](https://hackernoon.com/lang/es/la-diferencia-entre-pruebas-unitarias-y-pruebas-de-integraci%C3%B3n)
* Tipos de test en python: [herramientas de test](https://openwebinars.net/blog/herramientas-de-testing-en-python/)
* Documentación de Unittest: [documentación Unittest](https://docs.python.org/3/library/unittest.html)

## ¿Por qué realizar test?
La fase de testing es un pilar fundamental del ciclo de vida útil del desarrollo de software:

![ciclo de vida](https://www.canvia.com/wp-content/uploads/2024/08/canvia-infos-mesa-de-trabajo-1-copia-9-1200x1131.png)

### Importancia del Testing en el Desarrollo de Software  

El testing es una etapa crucial en el desarrollo de software, ya que garantiza que el software funcione correctamente y cumpla con los requisitos del usuario. Su correcta implementación ayuda a:  

- **Detectar errores temprano**, reduciendo costos y tiempo de desarrollo.  
- **Asegurar la calidad del software**, mejorando la experiencia del usuario.  
- **Mejorar la seguridad**, identificando vulnerabilidades y evitando riesgos.  

### Buenas Prácticas para un Testing Efectivo  

1. **Planificación y diseño**: Definir objetivos, requisitos y criterios de aceptación.  
2. **Automatización**: Ahorra tiempo y mejora la precisión de las pruebas.  
3. **Pruebas en todas las etapas**: Desde el diseño hasta la implementación.  
4. **Documentación**: Registrar errores y soluciones para futuras referencias.  

---

## Comparación entre Pruebas Unitarias y Pruebas de Integración

| **Característica**        | **Pruebas Unitarias**                                                                                   | **Pruebas de Integración**                                                                 |
|---------------------------|--------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------|
| **Definición**            | Validan un componente individual del software, como una función o método.                            | Verifican la interacción entre múltiples componentes y su integración con el entorno.     |
| **Objetivo**              | Asegurar que cada unidad funcione correctamente de manera aislada.                                   | Garantizar que los módulos trabajen juntos sin errores.                                   |
| **Alcance**               | Se enfocan en una única unidad de código.                                                            | Involucran múltiples módulos y sus interacciones.                                         |
| **Automatización**        | Altamente automatizables, facilitando pruebas de regresión.                                         | Pueden ser automatizadas, pero requieren configuraciones más complejas.                   |
| **Uso de dependencias**   | Se usan mocks o stubs para simular dependencias externas.                                           | Requieren conexión con bases de datos, APIs u otros sistemas externos.                    |
| **Complejidad**           | Baja, son simples de escribir y ejecutar.                                                           | Mayor, ya que incluyen múltiples componentes y su configuración.                          |
| **Velocidad de ejecución**| Rápidas, debido a la falta de dependencias externas.                                               | Más lentas, ya que dependen de la interacción entre módulos y recursos externos.          |
| **Cuándo aplicarlas**     | Durante el desarrollo, antes de la integración del sistema completo.                               | Después de las pruebas unitarias, al integrar los componentes del sistema.                |

---

## Comparativa de Herramientas de Testing en Python

| **Herramienta**     | **Tipo de Prueba**              | **Pros** | **Contras** |
|---------------------|--------------------------------|----------|-------------|
| **unittest**       | Unitarias                      | Incluido en la biblioteca estándar. <br> Amplia documentación y comunidad. | Sintaxis más detallada que otras herramientas. |
| **pytest**         | Unitarias e integración        | Sintaxis sencilla y fácil de usar. <br> Soporte para fixtures y plugins. | Requiere instalación adicional. |
| **nose2**          | Unitarias e integración        | Extiende funcionalidades de unittest. <br> Soporte para plugins. | Menos popular que unittest y pytest. |
| **doctest**        | Unitarias                      | Permite escribir pruebas en docstrings. <br> Fácil de usar en pequeños módulos. | Menos adecuado para pruebas complejas. |
| **Hypothesis**     | Pruebas basadas en propiedades | Genera datos de prueba automáticamente. <br> Detecta casos límite inesperados. | Puede ser más complejo de configurar. |
| **Schemathesis**   | Pruebas de API                 | Pruebas automáticas para APIs OpenAPI/Swagger. <br> Detecta errores de contrato. | Requiere documentación OpenAPI bien definida. |
| **Playwright**     | Pruebas de UI/E2E              | Soporta múltiples navegadores. <br> Rápido y confiable para pruebas front-end. | Puede ser más complejo de configurar en proyectos grandes. |
| **Robot Framework**| Pruebas de aceptación/E2E      | Sintaxis basada en palabras clave fácil de leer. <br> Soporte para Selenium, API y más. | Menos flexible para pruebas unitarias. |
| **Locust**         | Pruebas de carga               | Pruebas de rendimiento con Python. <br> Fácil de escalar y simular miles de usuarios. | No adecuado para pruebas funcionales o unitarias. |

---

## 🏗️ Estructura de un Test Unitario  

Los tests unitarios siguen la estructura **AAA (Arrange, Act, Assert)**:  

1. **Arrange (Organizar)**: Se preparan los datos y el entorno necesarios para la prueba.  
2. **Act (Actuar)**: Se ejecuta la función o método que se quiere probar.  
3. **Assert (Afirmar)**: Se verifica si los resultados obtenidos coinciden con los esperados.  

---

## 🏗️ Estructura de un Test de Integración  

Los tests de integración siguen la estructura **SEVT (Setup, Execute, Verify, Teardown)**:  

1. **Setup (Configurar)**: Se preparan los sistemas externos (bases de datos, APIs, etc.).  
2. **Execute (Ejecutar)**: Se realiza la operación que involucra múltiples módulos.  
3. **Verify (Verificar)**: Se comprueba que los datos fluyan correctamente entre los módulos.  
4. **Teardown (Limpiar)**: Se cierran conexiones y se eliminan recursos usados.  

---

### 🏆 Buenas Prácticas para los Tests Unitarios  

Para escribir pruebas unitarias efectivas, es recomendable seguir estas buenas prácticas:  

✔️ **Independencia**: Cada prueba debe ser autónoma y no verse afectada por cambios en otros módulos.  
✔️ **Prueba una sola cosa a la vez**: Un test debe validar una única unidad de código.  
✔️ **Estructura y nombres claros**: Usa un esquema ordenado y nombres consistentes para las pruebas.  
✔️ **Validación obligatoria**: Cualquier cambio en el código debe pasar las pruebas antes de implementarse.  
✔️ **Corrige los errores de inmediato**: No avances sin solucionar los bugs detectados en las pruebas.  
✔️ **Prueba regularmente**: Realiza tests con frecuencia para evitar la acumulación de errores.  

Seguir estas prácticas mejora la calidad del software y facilita su mantenimiento. 🚀  

---

## 💡 Conclusión  

El **testing** es una parte esencial del desarrollo de software. Las **pruebas unitarias** permiten detectar errores de forma rápida y sencilla, mientras que las **pruebas de integración** garantizan que los módulos funcionen correctamente en conjunto.  

➡️ **Priorizar las pruebas unitarias** por su velocidad y facilidad de ejecución, pero sin descuidar las pruebas de integración.  
➡️ **Aplicar la estructura AAA** en los tests unitarios y **SEVT** en los tests de integración.  
➡️ **Seguir buenas prácticas** para mantener un código fiable y fácil de mantener.  

¡Un buen testing asegura software de alta calidad y libre de errores! ✅  

# Vamos a realizar un test unitario paso a paso usando unittest

Para ello primero descargate este repositorio:

```textplain
git clone git@github.com:abbyenredes/test-unitarios-y-de-integracion.git
```
Ingresa en la carpeta:

```textplain
cd test-unitarios-y-de-integracion/
```
Vas a encontrar el archivo calculadora.py que tiene cuatro operaciones básicas. En este ejemplo usaremos la suma, sin embargo te ánimo a que pruebes y realices test de las otras operaciones poniendo en práctica todo lo que te he enseñado.

Empecemos creando nuestro primer archivo al que llamaremos test1_suma.py

> [!TIP]
> Si estas en visual studio code simplemente crea tu archivo desde  la barra de herramientas.

```textplain
touch test1_suma.py
```
Para este ejemplo estaré aplicando la estructura AAA, en nuestro archivo importa la librería unittest, importa el módulo que quieres probar en este caso calculadora y de calculadora queremos probar la función suma
tu código debe verse tal que así:

```python
import unittest
from calculadora import suma
```
Ahora crearemos una clase que va a heredar el método `TestCase` de unittest y dentro de esta clase creamos tantas pruebas como necesitemos, cabe recalcar que todas las funciones que realices deben empezar con la palabra `test` de lo contrario unittest no las detectará, en nuestro caso vamos a usar en método `assertEqual` para la suma de números positivos.

Te dejo un ejemplo de las pruebas que podemos hacer y te invito a revisar la [documentación de unittest](https://docs.python.org/3/library/unittest.html) para conocer todo lo que puedes hacer:

| Método                   | Verifica que                | Ejemplo                     |
|--------------------------|----------------------------|-----------------------------|
| `assertEqual(a, b)`      | `a == b`                   | `assertEqual(5, 5) ✅`      |
| `assertNotEqual(a, b)`   | `a != b`                   | `assertNotEqual(5, 3) ✅`   |
| `assertTrue(x)`          | `bool(x) is True`          | `assertTrue(3 > 2) ✅`      |
| `assertFalse(x)`         | `bool(x) is False`         | `assertFalse(3 < 2) ✅`     |
| `assertIs(a, b)`         | `a is b`                   | `assertIs(obj1, obj1) ✅`   |
| `assertIsNot(a, b)`      | `a is not b`               | `assertIsNot(obj1, obj2) ✅`|
| `assertIsNone(x)`        | `x is None`                | `assertIsNone(None) ✅`     |
| `assertIsNotNone(x)`     | `x is not None`            | `assertIsNotNone(5) ✅`     |
| `assertIn(a, b)`         | `a in b`                   | `assertIn(3, [1,2,3]) ✅`   |
| `assertNotIn(a, b)`      | `a not in b`               | `assertNotIn(4, [1,2,3]) ✅`|
| `assertIsInstance(a, b)` | `isinstance(a, b)`         | `assertIsInstance(5, int) ✅` |
| `assertNotIsInstance(a, b)` | `not isinstance(a, b)` | `assertNotIsInstance(5, str) ✅` |

> [!IMPORTANT]
> Al final de cada test debemos usar la siguiente variable global `if __name__ == '__main__':
    unittest.main()` ya que de no hacerlo nuestro test no se ejecutará.


```python
class TestSuma(unittest.TestCase):

    def test_suma_numeros_positivos(self):
        # Arrange (Preparación)
        num1 = 3
        num2 = 2
        resultado_esperado = 5

        # Act (Ejecución)
        resultado_obtenido = suma(num1, num2)

        # Assert (Verificación)
        self.assertEqual(resultado_obtenido, resultado_esperado)

if __name__ == '__main__':
    unittest.main()
    
```

Ejecutamos la prueba:

Linux o Mac:

```textplain
python3 -m unittest test_suma.py
```
Windows:

```textplain
python -m unittest test_suma.py
```
En este caso le samos Q para finalizar la fase input:
![](https://github.com/abbyenredes/Bootcamp-IA-F5/blob/main/Taller_django/img/unittest-ok.gif)

Te has preguntado que pasaria si el resultado esperado fuera uno nada lógico:

```python
class TestSuma(unittest.TestCase):

    def test_suma_numeros_positivos(self):
        # Arrange (Preparación)
        num1 = 3
        num2 = -2
        resultado_esperado = 5

        # Act (Ejecución)
        resultado_obtenido = suma(num1, num2)

        # Assert (Verificación)
        self.assertEqual(resultado_obtenido, resultado_esperado)

if __name__ == '__main__':
    unittest.main()
    
```

![](https://github.com/abbyenredes/Bootcamp-IA-F5/blob/main/Taller_django/img/unittest-ko.gif)

Ahora te toca a ti, diviértete rompiendo este código de las formas más originales posibles y explora todo lo que unittest tiene para ofrecer.

![](https://liveimages.algoworks.com/new-algoworks/wp-content/uploads/2022/05/10153127/testing-manual-testing.gif)
