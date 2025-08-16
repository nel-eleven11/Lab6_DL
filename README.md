# Lab6_DL

---

# Respuestas a preguntas

## Parte 1:

- Describa en una frase la diferencia entre los modelos discriminativos y los generativos
  
  R// Un modelo discriminativo aprende la probabilidad P(y | x) y se especializa en distinguir o clasificar muestras por ejemplo, decir “esta imagen es un 5”, mientras que un modelo generativo aprende la distribución conjunta P(x) (o P(x | y)) y puede muestrear nuevos datos que se parezcan a los reales.

- Explique como el concepto de MinMax se aplica a los GAN
  
  R// En las GAN se plantea un juego de suma cero entre dos redes: el discriminador D trata de maximizar su habilidad para asignar 1 a muestras reales y 0 a las generadas, mientras que el generador G trata de minimizar esa misma habilidad de D es decir, maximizar la probabilidad de que D clasifique sus muestras como reales.
  
- Describa lo que se está observando en la imagen GIF que se generó
  
  R// El GIF despliega, época a época, cómo las muestras que genera G (puntos coloreados) van pasando de una nube completamente desordenada a distribuirse progresivamente sobre la curva (x₁, sin(x₁)), imitando la forma de los datos reales. Al principio son aleatorias; hacia las últimas épocas van “alineándose” a la senoidal.

- ¿Cree que se ha creado un buen modelo? ¿Por qué?
  
  R// En términos cualitativos, sí: las muestras finales cubren razonablemente bien la forma senoidal original, lo que significa que G ha aprendido la distribución subyacente.
  Sin embargo, aún hay zonas poco cubiertas (p.ej. alrededor de los extremos de la curva) y cierta dispersión, lo que sugiere que podría mejorarse ajustando hiperparámetros (arquitectura, tasa de aprendizaje, balance de entrenamiento D vs. G) para obtener una cobertura más uniforme y reducir el ruido en la generación.

## Parte 2:

- ¿Qué diferencias hay entre los modelos usados en la primera parte y los usados en esta parte?
- ¿Qué tan bien se han creado las imagenes esperadas?
- ¿Cómo mejoraría los modelos?
- Observe el GIF creado, y describa la evolución que va viendo al pasar de las epocas
